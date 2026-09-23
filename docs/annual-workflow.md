# Annual workflow

*English · [中文](zh/annual-workflow.md)*

## 1. Establish scope

- Fix the financial year dates, the taxpayers, and the ownership percentage of each asset.
- Record what changed this year: a new job, a new course, new equipment, refinancing, a move, a change in rental status, securities sold.
- Not having sold shares does not mean there is no investment income. Interest, dividends, managed fund distributions, AMIT statements and foreign income all still apply.

## 2. File the source material

A workable local layout:

```text
tax-YYYY-YY/
  00-summary/
  01-bank/
  02-income/
  03-rental/
  04-work-expenses/
  05-education/
  06-investments/
  07-health-and-medicare/
  08-prior-year/
```

Keep originals read-only and put analysis in separate Markdown files or a workbook. Put the date, institution, item and amount in the filename — but never a TFN.

## 3. Normalise the bank data

One schema for every account:

| Field | Meaning |
| --- | --- |
| date | The real transaction date |
| account | Bank and account alias — never the full account number |
| owner | Account holder alias |
| amount | Positive for money in, negative for money out |
| description | The bank's raw description |
| merchant | Normalised payee |
| category | Rent, interest, insurance, education, equipment, subscription, etc. |
| tax_status | confirmed / conditional / excluded / missing-evidence |
| evidence | The matching document or email subject |
| notes | Address, purpose, work-use percentage — the basis for the call |

Aggregate by payee first, then look at large amounts, repeated amounts, recurring payments and vague descriptions. Credit card repayments, transfers between your own accounts and deposits into investment accounts are not expenses in themselves — trace back to the underlying transaction.

A single statement PDF often contains several sub-accounts. Identify the account heading and date range on every page; do not read only the first page's summary or the first transaction table. Once all accounts are normalised, check opening balance, inflows, outflows and closing balance per account **before** starting tax classification.

## 4. Search email in a fixed order

Restrict by financial-year dates, then search in turn:

- **Salary and PAYG**: payslip, income statement.
- **Rental**: property address, agent name, rental statement, levy, rates, water, insurance, repair.
- **Work expenses**: invoice, subscription, software, membership, registration, CPD.
- **Education**: institution name, student account, tax invoice, Commonwealth Assistance Notice.
- **Equipment**: Apple, JB Hi-Fi, your computer and phone models.
- **Tax administration**: tax agent, accountant, lodgment fee.

An email subject or a bank description is a lead, not a conclusion. Confirmation needs the date, amount, supplier, purpose and payer to agree with each other.

## 5. Reconcile income

- Salary credits in the bank tell you which employers exist, whether a month is missing, and whether there is a second job. They do not replace the ATO income statement.
- For each employer separately, reconcile the months credited, the ATO gross income and the PAYG withheld.
- The gap between net pay and gross income usually contains PAYG plus items outside super — packaging or other deductions. Do not back it out and lodge the result directly.
- Transfers between accounts in the same name, between spouses, or into savings are internal transfers, not household income.
- Again: no share sales does not mean no investment income. Check interest, dividends, distributions, AMIT and foreign income.

## 6. Classification rules

- `confirmed` — payment, evidence, purpose and financial year all agree.
- `conditional` — the transaction is real, but deductibility depends on the work connection, a use percentage, or the nature of a course.
- `excluded` — private spending, capital contributions, internal transfers, reimbursed or duplicated amounts.
- `missing-evidence` — the amount or payee looks relevant, but there is no invoice, address or itemisation.

## 7. Cross-year checks

Every year, go back to last year's workbook and final lodgment for:

- the adjustable value of computers, phones and other equipment;
- remaining years of borrowing expenses;
- capital works and any quantity surveyor schedule;
- the tax agent fee actually paid last year;
- carried-forward tax losses;
- prepayments spanning the year end;
- items paid but deferred last year for want of a date or evidence.

"Bought last year" does not mean "deductible this year". Check the depreciation schedule, the incurred and paid dates, and what was previously lodged.

## 8. Output

Deliver at least three things:

1. The current estimate and its assumptions.
2. The line-by-line transaction determination.
3. Missing items and open questions.

Every number should trace back to a source. Show the conservative confirmed total separately from high-confidence candidates.
