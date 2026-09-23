# Income and household cash flow reconciliation

*English · [中文](zh/income-and-cashflow-reconciliation.md)*

This process serves both tax substantiation and household cash-flow analysis, but the two use different definitions and must be kept apart. Tax classifies by tax character; household cash flow classifies by real inflow, real consumption, asset transfer and internal transfer.

## Coverage

Build an account inventory recording, for each: holder alias, institution, account type, dates covered, opening balance and closing balance. Where a bank PDF contains several sub-accounts, register each one separately. If an account or a month is missing, mark the summary conclusions incomplete.

## Standard fields

```text
date | owner | source | account | description | merchant
amount | flow_type | category | subcategory | tax_status
evidence | counterparty | transfer_match | notes
```

`flow_type` should cover at least:

- `income` — salary, rent, interest and other external inflows;
- `expense` — final consumption of goods or services;
- `internal-transfer` — between your own or the household's accounts;
- `investment-or-debt` — securities funding, loan principal, movements into savings;
- `refund-or-reversal` — merchant refunds and reversals;
- `unresolved` — character not yet determined.

## Salary income

1. Identify every recurring salary credit and normalise the employer name.
2. Check for missing months, one-off bonuses, termination payments and a second employer.
3. Confirm gross income and PAYG withheld per employer from the ATO income statement.
4. Net salary received is for cash-flow and completeness checking only. It is not the income figure to lodge.

## Net-pay sanity check: estimating gross income

> **This is a cash-flow sanity check, not a tax calculation.** It exists to spot a missing month, an unrecorded employer or a wrong ownership assumption before the real figures arrive. It never substitutes for the ATO income statement or a payslip, and no amount derived this way should be lodged.

Before the income statement is available, the bank shows only the net amount. Solving the year's rate scale backwards gives an approximate gross and an indicative marginal rate:

```text
find G such that:  G - income tax(G) - Medicare(G) ≈ total net received for the year
```

Income tax is the progressive scale for that year; Medicare is a fixed proportion. Bisection over a plausible range solves it.

### Why the result is approximate

The solve treats PAYG withheld as if it equalled the annual liability. It does not. PAYG is calculated per pay period from the ATO's withholding schedules, which the ATO publishes separately each year, and it diverges from the annual assessment because of:

- rounding within the schedules, and pay frequency;
- bonuses and back payments, withheld under their own schedule;
- part-year employment, or a change of employer mid-year;
- the tax-free threshold claimed with more than one employer, or with none;
- a study or training support loan, withheld at its own rate;
- salary sacrifice and other pre-tax deductions, which the bank never sees.

The gap between withholding and liability is exactly what produces a refund or a bill at assessment. A method that assumes the gap is zero cannot also measure it.

### The assumptions, and which way the error runs

Assumed: the tax-free threshold is claimed, with one employer; no study or training loan; no salary sacrifice; no other pre-tax withholding.

Where withholding is **higher** than the standard annual liability — a study loan, or a second employer where the threshold was not claimed — the same net receipts imply a **higher** gross, possibly a bracket higher. With multiple employers the derived figure is therefore **conservative**. With salary sacrifice, the total package exceeds the taxable income derived this way.

### Validating against a payslip

One payslip settles it, and should be obtained rather than relied on as a cross-check of last resort:

```text
annual base salary = monthly base × 12
less: unpaid leave (hours × hourly rate)
= gross per the payslip
```

Where the assumptions hold, this has agreed with the solved figure to within about one percent — but treat the payslip as the answer and the solve as the thing being checked, not the reverse. The payslip also confirms two assumptions directly: the tax scale code (whether the threshold was claimed) and whether there is a study loan deduction line.

### Two things to keep separate once the real figures arrive

These both need **actual** gross and PAYG from the income statement. Neither can be derived from the solve above, which assumes the two are equal by construction.

**Over-withholding is refundable regardless of deductions.** Where PAYG withheld for the year exceeds the annual liability on the assessed income, that excess was always coming back and has nothing to do with any deduction. Present it separately from the tax saved by deductions, so the two are not conflated.

**A deduction is worth its owner's marginal rate.** Where spouses sit in different brackets, the same dollar of deduction can differ in value by more than thirty percent. Where a deduction straddles a bracket, the effective rate is between the two:

```text
portion above the threshold × higher rate + remainder × lower rate
```

### The household total has its own effect

Combined income for surcharge purposes sets the Medicare Levy Surcharge tier. Where private hospital cover is held, calculate the surcharge avoided — the premium is not deductible, but at higher incomes the cover can still be worth it. This matters most when the household sits just below the next threshold. The tier thresholds are indexed; take them from `rules/` for the year, not from memory.

## Preventing double-counting

- Matching debits and credits on the same day between two household accounts should be paired as an internal transfer.
- A credit card or instalment account repayment is not a second act of consumption. Where the underlying purchases are already itemised, exclude the repayment.
- Broker funding and transfers into savings are asset movements, not living expenses.
- Pair merchant refunds with the original expense. Where they cannot be paired, list them separately rather than netting off a whole category.
- Cash withdrawals, vague transfers and payment-platform transactions stay `unresolved` until the ultimate payee is established.

## Household balance

Verify at account level first:

```text
opening balance + external inflows + internal inflows
- external outflows - internal outflows = closing balance
```

Then eliminate internal transfers at household level:

```text
external income - real expenses
- net investment/debt funding + refunds
= change in household cash, allowing for opening/closing timing
```

Report at minimum with salary and other income, housing, food, transport, health insurance, education, subscriptions, equipment, investment/debt, refunds and unidentified items shown separately. Do not let "other" conceal a large or recurring merchant.

## Merchant identification and evidence matching

Build a merchant alias dictionary from the raw descriptions first, then confirm using invoice date, amount, email recipient, order number and purpose. For utilities, insurance, council rates, levies and subscriptions, check the periods are complete; where a month is missing or an amount looks wrong, go back to the emailed bill or the relevant account.

## Output quality gates

- Every account and every month has a coverage status;
- the internal-transfer pairing rate and the unpaired amount are visible;
- unidentified transactions are listed separately;
- income is stated on both the bank-net basis and the ATO tax basis;
- every summary figure drills down to the original transaction and its evidence;
- tax candidates are kept strictly separate from ordinary household spending.
