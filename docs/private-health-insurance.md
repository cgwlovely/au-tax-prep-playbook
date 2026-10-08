# Private health insurance and the rebate reconciliation

*English · [中文](zh/private-health-insurance.md)*

The private health insurance section looks like data entry and is actually a reconciliation. The insurer gave you a rebate during the year based on an income tier it had to guess at. The return works out the tier you actually fell into and settles the difference.

## 1. Two statement lines are normal

The government rebate percentage is re-set on 1 April each year, so an insurer's annual statement splits the year in two:

| Line | Period | Benefit code (under 65) |
| --- | --- | ---: |
| 1 | 1 July – 31 March | 30 |
| 2 | 1 April – 30 June | 31 |

Higher age bands use their own code pairs. Two lines are not a duplicate record and must not be consolidated into one. If the insurer reports more lines than the form provides slots for, combine them **within the same benefit code**, never across codes.

## 2. Reverse-check which tier the insurer assumed

Before entering anything, divide:

```text
rebate received ÷ premiums eligible for rebate = the rate the insurer applied
```

Match that rate against the published rebate percentages for the year. It tells you immediately which tier the insurer assumed — almost always the base tier, because insurers do not know your spouse's income.

Then compute the tier you actually fall into and the difference becomes predictable:

```text
excess to repay ≈ premiums × (rate received − rate entitled)
```

Doing this before lodging means the liability that appears in the estimate is one you expected, not a surprise you have to investigate.

## 3. The tier test uses a wider income than taxable income

Income for surcharge and rebate purposes is **not** taxable income. It adds back, among other things:

- net rental property loss;
- net financial investment loss;
- reportable fringe benefits;
- reportable employer superannuation contributions.

A negatively geared household therefore sits in a higher tier than its taxable income suggests. For a couple the test uses the **combined** figure, so neither return can be finalised on its own — each needs the other's taxable income, and the rental loss is added back on both sides.

## 4. Claim codes must be complementary across both returns

The codes describe who claims whose share. The two returns have to agree:

| Situation | Person A | Person B |
| --- | --- | --- |
| Each claims their own share | C | C |
| A claims the whole policy | C, answering yes to claiming the spouse's share | E |
| Covered as a dependent | — | F |

**Both people using C while one also claims the spouse's share is a double claim.** Check the two returns against each other, not each in isolation.

## 5. Separate policies change the answer

Two different membership numbers mean two separate policies, not one family policy. There is then no spouse share to claim at all: each person reports their own policy with their own premiums, and both answer no to the spouse-share question.

Check the membership numbers before assuming a couple is on one policy. The surcharge test still looks at combined income and still requires **both** people to hold an appropriate level of hospital cover — the policies being separate does not change that.

## 6. Extras-only cover does not avoid the surcharge

Only an appropriate level of private patient **hospital** cover does. Where the return reports no surcharge liability, that is a computed result confirming the hospital-cover question was answered correctly — a useful check that it was.

## 7. What to keep

- the insurer's annual tax statement for each policy;
- a note of the tier you landed in and the combined income that put you there;
- the claim codes used on both returns, recorded together so next year starts from a consistent position.
