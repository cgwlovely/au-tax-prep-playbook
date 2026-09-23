# Expense attribution: separating two properties

*English · [中文](zh/expense-attribution.md)*

When you hold a home and a rental property at the same time, the council rates, water, insurance and trades bills arrive under the same merchant names for similar amounts. Getting attribution wrong fails in both directions: charging a home expense to the rental over-deducts, and missing a rental expense under-deducts.

The five methods below cross-check each other. None of them is sufficient on its own.

## Method 1: count the quarters

For anything billed quarterly — council rates, water — **one property should produce exactly four instalments a year**.

```text
payments for an item in a financial year ÷ 4 ≈ number of properties involved
```

Six council rates payments in a year means two properties, with one of them showing only two instalments — the other two were almost certainly paid by the agent. Eight means four instalments each.

Clustering by amount separates them further: consecutive quarters for one property are close in value and rise smoothly, while two different properties usually differ by a recognisable margin.

## Method 2: cross-eliminate what the agent paid

The Money Out column of the agent's annual summary itemises everything the agent paid on your behalf.

```text
total payable on the rental = paid by agent + paid directly by owner
```

Use that identity backwards. If the agent paid two quarters of council rates, then only two of the owner-paid instalments belong to the rental; the rest belong to the home.

**This is the strongest method**, because the agent's summary is a third-party document and is itemised.

## Method 3: separating insurance policies

Several policies with one insurer share a merchant name in the bank data, but three features tell them apart:

| Feature | How to use it |
| --- | --- |
| **Policy reference prefix** | Debits for one policy share a fixed prefix; different policies have different prefixes |
| **Start date** | Landlord cover starts when the property is first let; home contents when the home was bought; motor when the vehicle was insured |
| **Monthly amount** | Landlord cover on a unit or townhouse is usually well below contents cover on a house; motor sits between them |

Only treat it as settled when all three agree. **The start date carries the most weight** — a first landlord premium falling on the date the tenancy began is close to conclusive.

Track breaks and continuations too. One insurer stopping in a given month and another starting the next at a similar amount is usually the same risk with a new underwriter, not two separate policies.

## Method 4: check the customer reference on the bill

Water and council rates notices, paper or electronic, carry a customer reference number and the property address.

```text
register each property's customer reference once, then attribute every payment by reference
```

This is the most certain method, but it needs the original notices. Do it once when first establishing attribution, record the references in a control sheet, and afterwards only check new ones.

## Method 5: consistency of payment patterns

Across a full financial year, the holding costs for one property should **appear together**.

```text
if the owner paid four quarters of rates and four of water, those two sets very likely belong to the same property
```

Conversely, four rates but only two water instalments means the other two water quarters were paid by someone else — the agent.

## The determination sequence

```text
1. Count annual payments per item      → method 1, how many properties are involved
2. Pull the agent's annual summary     → method 2, subtract what the agent paid
3. Check customer references           → method 4, settle whatever you have originals for
4. Split insurance by prefix + start date + amount → method 3
5. Check instalment counts agree across items for one property → method 5, find gaps
6. Anything still open goes on the missing-items list, naming the document needed to settle it
```

## The two ways it goes wrong

**Over-deducting** — charging the home's rates, water, electrical work or contents insurance to the rental. These amounts are usually not small and are hard to explain under review.

**Under-deducting** — treating a rental expense as a home expense and not claiming it. Less common, but still a loss.

## One specific warning: water is not a home-office expense

Water at your home is neither a rental expense **nor** an ATO-recognised working-from-home running expense. The running expenses covered are electricity, gas, internet, phone, stationery and consumables.

Water misclassified as a home-office cost is one of the recorded failures behind this playbook — and once it happens it repeats every year, because the next year's figure gets carried forward from the last.
