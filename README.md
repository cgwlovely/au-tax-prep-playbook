# AU Tax Prep Playbook

*English · [中文](README.zh.md)*

A reusable method library for preparing an Australian individual tax return where one household holds both a home and a jointly-owned rental property.

The aim is to turn the parts that repeat every year — collecting source documents, classifying bank transactions, reconciling against the managing agent, carrying depreciation forward, and chasing missing evidence — into a process rather than an annual scramble.

It is written for people who prepare their own working papers, whether they lodge through myTax or hand the result to a registered tax agent.

## What this is not

This repository contains **methods only**. It is not tax advice, and it contains no one's actual financial data.

Never commit:

- bank statements, payslips, TFNs, identity documents or loan contracts;
- original emails, invoices or private health insurance records;
- names, addresses, account numbers, customer references or real transaction amounts;
- a complete tax workbook or anything lodged with the ATO.

Keep real material in a local encrypted folder or a controlled document system. The `.gitignore` here blocks the common financial file types, but check by hand before every commit.

## The workflow in outline

1. Create a folder for the financial year and keep originals read-only.
2. Consolidate every bank and credit card account into one normalised transaction set.
3. Search email for payslips, agent statements, body corporate levies, water, council rates, insurance, education, equipment and subscriptions.
4. Reconcile the rental property on a **gross** basis as well as net cash, so that expenses the agent already paid out of rent are never deducted twice.
5. For bills that could belong to either property — council rates, water, insurance, repairs — establish attribution by customer reference or by cross-eliminating what the agent paid.
6. Review last year's depreciation schedule, borrowing expenses, capital works and the tax agent fee actually paid. Screen construction dates before paying for a depreciation schedule.
7. Mark every item `confirmed`, `conditional`, `excluded` or `missing-evidence`, and keep a separate list of items **assessed and closed**.
8. Produce an estimate and an outstanding-items list, then lodge or hand over.

## Method documents

| Document | What it solves |
| --- | --- |
| [Annual workflow](docs/annual-workflow.md) | The order to do things in each year |
| [Income and household cash flow](docs/income-and-cashflow-reconciliation.md) | Salary, transfers, household spending; deriving gross income from net pay |
| [Rental reconciliation](docs/rental-reconciliation.md) | Agent statements, bank records and the annual summary, checked against each other |
| [Three traps in bank data](docs/bank-data-pitfalls.md) | Posting dates, overseas batching, merchant names; how classification rules go wrong |
| [Expense attribution](docs/expense-attribution.md) | Separating bills that could belong to either property |
| [Repairs, improvements and depreciation](docs/repairs-vs-capital.md) | Deductible now or capitalised; screening Div 43 and Div 40 eligibility |
| [Substantiating work use](docs/substantiating-work-use.md) | Proving equipment work-use percentage and working-from-home hours |
| [Handover checklist](docs/handover.md) | What to check before handing the file to an agent |

## Year rules

`rules/YYYY-YY/` records what the rule actually is for a given year, with its ATO source, the date it was last verified, and a `low` / `needs-review` risk flag. Annually indexed figures live here; legislated and structurally stable ones stay in the method documents. Values that have not been verified are left **blank** rather than guessed — see [rules/README.md](rules/README.md).

| File | Covers |
| --- | --- |
| [Work expenses](rules/2025-26/work-expenses.md) | WFH fixed rate and both methods' record requirements, car |
| [Rental](rules/2025-26/rental.md) | Gross reporting, insurance, borrowing expenses, recoupments, travel, levies |
| [Depreciation](rules/2025-26/depreciation.md) | Div 43 dates and rates, TR 97/25, s40-27, pool thresholds, start time |
| [Medicare and rates](rules/2025-26/medicare-and-rates.md) | Tax scale, levy, surcharge tiers, PAYG schedules, study loans |

## Templates

| Template | Use |
| --- | --- |
| [Annual summary](templates/annual-summary-template.md) | Financial-year result and open items |
| [Transaction review](templates/transaction-review-template.md) | Line-by-line classification |
| [myTax rental field map](templates/mytax-rental-field-map.md) | Field-by-field while lodging |

## Layout

```text
docs/          method and handover documents (English)
docs/zh/       Chinese translations
templates/     blank templates to copy into a new financial year (English)
templates/zh/  Chinese translations
rules/         per-year rules with sources and verification dates (bilingual, single source of truth)
```

## Disclaimer

This project supports document preparation and estimation. It is **not** tax advice, and it is not an automated lodgment tool or a tax rules engine — it contains no code. What it provides is an auditable chain: source documents → transaction classification → evidence → tax treatment → reconciliation → handover. Any lodgment must rest on the ATO rules current for that year and on complete substantiation, confirmed by a registered tax agent where appropriate.
