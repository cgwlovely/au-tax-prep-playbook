# Rental income and expense reconciliation

*English · [中文](zh/rental-reconciliation.md)*

## The core principle

Lodgment generally requires reporting **gross rent** and then itemising the deductible expenses. What the agent transfers to your bank is usually a net amount — after management fees, repairs, levies and any withheld balance — and cannot be treated as gross rent.

Before the annual summary arrives, a net-cash estimate is acceptable as an interim figure, provided it obeys:

> net agent transfers received + eligible expenses the owner paid directly; expenses the agent already paid out of rent are never added again.

## Three layers of checking

### 1. Agent statements

Record, for every period:

- Money In;
- Money Out;
- You Received;
- balance brought forward / withheld;
- non-ordinary credits such as rent, refunds and bond claims;
- management fees, letting fees, repairs, water, council rates and levies.

Balances on consecutive statements must join up. `Payment withheld` usually just means the agent is holding rent to pay a bill — it is not a payment by the owner to the agent.

Build a statement control sheet recording, per period: statement number, date range, opening balance, Money In, Money Out, You Received and closing balance. If a number is missing, a date range is broken, or balances do not join, the year is not reconciled.

### 2. Bank records

Match `You Received` against the agent's transfers, one by one. Then look separately for:

- loan interest;
- landlord insurance;
- body corporate / DEFT;
- council rates, water, repairs;
- direct payments to the agent or a supplier.

Equal amounts are not the same expense. Confirm with the account number, property address, DEFT reference, invoice number and payment date.

### 3. The annual financial summary

Once the annual summary arrives, rebuild on the gross basis:

```text
gross rent and other rental income
- agent fees and commissions
- council and water
- body corporate deductible levies
- insurance
- interest
- repairs and maintenance
- other eligible expenses
= rental profit or loss
```

Compare that with the net-cash figure. The difference usually comes from the balance withheld at year end, bonds and refunds, owner-paid items, or a missing statement.

First verify the annual summary's own identity:

```text
Money In - Money Out = annual net movement
```

Then build a bridge:

```text
annual net movement
+ opening agent balance
- closing agent balance
+/- bond, refund and owner contribution adjustments
= transfers received in the owner's bank account
```

Keep any unexplained difference and set an explicit tolerance. Never push a difference into "other expenses" to make it balance.

## Comparing across years

Water, council rates and levies should be compared by the period the bill covers, not by the month the bank paid it. Record, for each:

- the billing period and the payment date;
- whether the agent or the owner paid;
- the total, the deductible part and the capital part;
- the change against the previous one and two years;
- any missing quarter or duplicated bill.

Where last financial year prepaid a levy, premium or other cost covering the next period, list it separately as a cross-period item and have the tax agent confirm the year it is deductible.

## Body corporate

- Ordinary administration fund and general-purpose sinking fund contributions are usually immediately deductible.
- A special levy raised for a specific capital improvement is usually not immediately deductible in full; it may become capital works once the project completes.
- Where one levy covers both admin and the general sinking fund, keep the notice and statement as evidence of its character.
- Levies the agent paid are already reflected in a lower net transfer. Only levies the owner paid directly can be added on top in a net-cash interim estimate.

## Joint ownership

Rental income and expenses are generally apportioned by legal interest. Treat the percentage as an annual input rather than carrying last year's forward, and re-confirm it whenever title or interest changes.

## Recurring errors

- Using the agent's net transfer as income while also deducting the agent's Money Out.
- Mixing together the home's and the rental's council and water bills when the amounts are similar.
- Treating a bond, cleaning refund or tenant reimbursement as an owner contribution.
- Deducting loan principal along with interest.
- Treating a special capital levy as an ordinary quarterly levy.
- Reading only the bank merchant name without checking the address or customer reference.
- Adding invoice totals on top of a net agent figure that already includes those same items, such as water.
- Carrying summary values forward from an earlier workbook without independently recomputing the detail, the net figure and the ownership split.

## Independent check formulas

A workbook should carry at least three automatic checks:

1. Itemised income minus itemised expenses equals the rental net result.
2. The co-owners' shares sum to the property total.
3. Agent-paid expenses, owner-paid expenses and the net bank receipt contain no double-count between them.
