# Three traps in bank data

*English · [中文](zh/bank-data-pitfalls.md)*

An exported bank file looks like raw data. It has in fact been through three layers of processing, and conclusions drawn without recognising them are wrong in systematic, predictable ways.

## Trap 1: the posting date is not the spending date

The date in an export is the **posting date**, not the date the card was used.

### Measuring the lag

Some banks embed the real transaction time inside the description, in forms like `Date 17 Mar 2023` or `In <location> Date <date>`. Where they do, the lag for that account can be measured directly:

```text
lag in days = posting date - real date from the description
```

In practice, accounts that carry a real date stamp lag 1–3 days. Accounts without one have to be validated indirectly (below).

### Which conclusions get contaminated

| Conclusion | Affected? |
| --- | --- |
| Monthly and financial-year totals | Largely safe — the lag rarely crosses a month |
| Which financial year a transaction falls in | Late-June transactions can post in July; check these separately |
| **Day-of-week distribution** | **Badly distorted** |
| **Trip duration** | **Badly distorted** (see trap 2) |

Day-of-week breaks because weekend transactions are batched onto the next business day. The test is simple: count transactions by weekday. If Monday is inflated and the weekend is depressed, that account's dates cannot be used for behavioural analysis.

### Alternative sources of the real date

- Date stamps embedded in the description.
- Merchant receipts, such as exported supermarket e-receipts.
- Public transport card travel history.
- Device or application session logs.

When cross-validating this way, report the sample size. Do not extend a conclusion from a small sample to the whole dataset.

## Trap 2: overseas transactions post in batches

Compression is far worse abroad than at home. One batch can collapse several days across several cities onto a single posting date.

The test:

```text
compression ratio = transactions on the trip ÷ distinct posting dates
```

The higher the ratio, the less reliable the posting span is as a measure of trip length. Where the ratio is high, take the duration from:

- accounts that carry a real date stamp;
- the start and end dates on flights, accommodation and travel insurance;
- the traveller.

**Never use the span between the first and last posting date as the trip length.** This error inflates duration several-fold, which in turn turns any "average per day" figure into nonsense.

## Trap 3: the merchant name does not establish attribution

The same merchant name can cover different properties, different purposes, even different people.

Common misreadings:

- **Council rates and water** — bills for two properties carry an identical merchant name.
- **Insurance** — landlord, home contents and motor policies from one insurer share a merchant name.
- **Service stations and convenience stores** — could be fuel, an ATM withdrawal, or snacks.
- **Payment gateways** (PayPal, Square and similar) — the merchant name is the gateway or its registered city, not where the shop actually is.

For how to resolve attribution, see [Expense attribution](expense-attribution.md).

## How keyword rules go wrong

When classifying in bulk with keyword matching, the same few failures recur:

- **Unnormalised punctuation.** `JB HI-FI` will not match `JB HI FI`; `7-ELEVEN` will not match `7 ELEVEN`; `IG.COM` will not match `IG COM`. Replace every non-alphanumeric character with a space before matching.
- **Substring collisions.** `MOBIL` (the service station) matches `MOBILE BANKING`. `PASSPORT` matches `FITNESS PASSPORT`. `LEMON` (a dishwasher tablet scent) matches a fruit rule. Add word boundaries, or reorder the rules.
- **Rule order.** Flavoured yoghurt is captured by the fruit rule before it reaches the dairy rule. Put specific categories ahead of broad ones.

After every change to the rules, print the unclassified tail and check it by hand, until the residue is explainable.
