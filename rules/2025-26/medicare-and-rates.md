# 2025–26 · Medicare, surcharge and the tax scale · Medicare、附加税与税率表

> **Everything in this file is indexed or legislated annually.** Most of it is deliberately left blank. A plausible-looking wrong threshold here would propagate into every downstream estimate, so a blank is the safer default — open the source and fill it in when you need it.
>
> **本文件内容逐年调整，多数刻意留空。** 这里填一个看似合理但错误的门槛，会污染下游全部估算；留空更安全 —— 要用的时候打开出处再填。

## RATE-01 — Resident individual tax scale · 居民个人税率表

**Rule** —

| Taxable income | Tax on this income |
| --- | --- |
| $0 – $18,200 | Nil |
| $18,201 – $45,000 | 16c for each $1 over $18,200 |
| $45,001 – $135,000 | $4,288 + 30c for each $1 over $45,000 |
| $135,001 – $190,000 | $31,288 + 37c for each $1 over $135,000 |
| $190,001 and over | $51,638 + 45c for each $1 over $190,000 |

Excludes the Medicare levy. From 1 July 2026 the 16% rate falls to 15% — that is a **2026-27** change and does not apply here.

**规则** — 见上表，不含 Medicare。2026-07-01 起 16% 降为 15%，属 **2026-27** 财年，本年不适用。

**Source** — https://www.ato.gov.au/tax-rates-and-codes/tax-rates-australian-residents
**Last verified** — 2026-10-08 · **Risk** — low

## RATE-02 — Medicare levy · Medicare 征税

**Rule** — 2% of taxable income for most residents. The low-income reduction and exemption thresholds are indexed annually and are **not** recorded here.

**规则** — 多数居民按应税收入的 2% 计。低收入减免与豁免门槛逐年指数化，**未**记录于此。

**Source** — https://www.ato.gov.au/individuals-and-families/medicare-and-private-health-insurance/medicare-levy
**Last verified** — 2026-09-23 · **Risk** — needs-review *(the 2% rate is low-risk; the low-income reduction thresholds remain unverified)*

## RATE-03 — Income tiers for the surcharge and the rebate · 附加税与返还的收入档位

**Rule** — The same income tiers govern both the Medicare levy surcharge and the private health insurance rebate:

| Tier | Single | Family |
| --- | --- | --- |
| Base | $101,000 or less | $202,000 or less |
| Tier 1 | $101,001 – $118,000 | $202,001 – $236,000 |
| Tier 2 | $118,001 – $158,000 | $236,001 – $316,000 |
| Tier 3 | $158,001 or more | $316,001 or more |

The family threshold rises by $1,500 for each dependent child after the first. The surcharge is payable only where an appropriate level of private **hospital** cover is absent — extras-only cover does not avoid it.

**Income for surcharge purposes is wider than taxable income**: it adds back net rental property loss, net financial investment loss, reportable fringe benefits and reportable employer super contributions. A couple is assessed on the combined figure.

The structural point that does not change year to year: the premium is not deductible, but at higher incomes the surcharge avoided can exceed it. Calculate this when the household sits near a tier boundary.

**规则** — 见上表；同一套档位同时决定 MLS 与私保返还。家庭门槛自第二个受抚养子女起每人加 $1,500。仅有 extras 险不能免附加税。**用于判定的收入口径宽于应税收入**：要加回出租房净亏损、净金融投资亏损、应报告附加福利与应报告雇主养老金供款；夫妻按合计数判定。

**Source** — https://www.ato.gov.au/individuals-and-families/medicare-and-private-health-insurance/private-health-insurance-rebate/income-thresholds-and-rates-for-the-private-health-insurance-rebate
**Last verified** — 2026-10-08 · **Risk** — low

## RATE-06 — Private health insurance rebate percentages · 私保返还比例

**Rule** — The rebate rate is re-set on 1 April, so an insurer's annual statement splits the year into two lines:

| Age of oldest person covered | Base | Tier 1 | Tier 2 | Tier 3 |
| --- | ---: | ---: | ---: | ---: |
| **1 July 2025 – 31 March 2026** | | | | |
| Under 65 | 24.288% | 16.192% | 8.095% | 0% |
| 65 – 69 | 28.337% | 20.240% | 12.143% | 0% |
| 70 and over | 32.385% | 24.288% | 16.192% | 0% |
| **1 April 2026 – 30 June 2026** | | | | |
| Under 65 | 24.118% | 16.079% | 8.038% | 0% |
| 65 – 69 | 28.139% | 20.098% | 12.058% | 0% |
| 70 and over | 32.158% | 24.118% | 16.079% | 0% |

Benefit codes pair with these periods — for the under-65 band, the July–March line and the April–June line. Insurers generally apply the **base tier** during the year because they cannot know a spouse's income, so a household above the base tier repays the difference on assessment.

**规则** — 返还比例每年 4 月 1 日重设，故保险公司年度声明分两行。保险公司年中通常按**基础档**给付（因其不知配偶收入），超过基础档的家庭在评税时退回差额。

**Source** — https://www.ato.gov.au/individuals-and-families/medicare-and-private-health-insurance/private-health-insurance-rebate/income-thresholds-and-rates-for-the-private-health-insurance-rebate
**Last verified** — 2026-10-08 · **Risk** — low

## RATE-07 — Lump sum in arrears offset threshold · 欠薪抵免门槛

**Rule** — The lump sum payment in arrears tax offset is available only where the eligible arrears amount is **10% or more** of threshold test income — broadly, taxable income for the year of receipt **less** the arrears amount itself (and less certain other amounts such as employment termination payments and net capital gains). Below that, the offset is nil.

Reporting the accrual year or years remains mandatory regardless; the figure simply drives no calculation when the test fails.

**规则** — 只有当合资格欠薪达到 threshold test income 的 **10% 以上**时才有抵免。threshold test income 大致为收款年度应税收入减去欠薪本身（及 ETP、净资本利得等若干项）。不足则抵免为零。**但归属年度仍必须申报**，只是该数字在测试不通过时不驱动任何计算。

**Source** — https://www.ato.gov.au/individuals-and-families/income-deductions-offsets-and-records/income-you-must-declare/lump-sum-payment-in-arrears
**Last verified** — 2026-10-08 · **Risk** — low

## RATE-04 — PAYG withholding schedules · PAYG 预扣表

**Rule** — PAYG withheld is calculated per pay period from the ATO's withholding schedules. It **approximates** the annual liability and routinely differs from it. That difference is what produces a refund or a bill at assessment.

Do not treat withholding as equal to the annual liability in any calculation intended to be relied on. See the caveats in [income-and-cashflow-reconciliation](../../docs/income-and-cashflow-reconciliation.md).

**规则** — PAYG 按发薪周期依 ATO 预扣表计算，只是年度应纳税额的**近似值**，二者常有差异 —— 这个差异正是评税时退税或补税的来源。任何需要被依赖的计算，都不得把预扣当作等于年度应纳税额。

**Source** — https://www.ato.gov.au/tax-rates-and-codes/payg-withholding-tax-tables
**Last verified** — 2026-09-23 · **Risk** — low *(principle; the schedules themselves are not reproduced here)*

## RATE-05 — Study and training support loan repayment · 学贷还款

**Rule** — *(not verified for 2025–26)* — repayment is assessed on repayment income and withheld through PAYG at its own rate, separately from income tax.

**Source** — https://www.ato.gov.au/tax-rates-and-codes/study-and-training-support-loans-rates-and-repayment-thresholds
**Last verified** — never · **Risk** — needs-review
