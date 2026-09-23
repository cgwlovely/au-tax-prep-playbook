# Substantiating work-use percentage and days at home

*English · [中文](zh/substantiating-work-use.md)*

The work-use percentage on equipment and the hours worked from home are both figures the taxpayer asserts. What the ATO requires is not that the number be small, but that it have a basis. A high percentage is not itself a problem; a poorly evidenced one is.

This document records several ways to build that basis out of records you already have, and the limits of each.

## 1. Work-use percentage on equipment

### Automatic records you already have

Development and AI tools generally write session records locally, each entry carrying a timestamp and a working directory:

```text
~/.claude/projects/**/*.jsonl        each line carries a timestamp and cwd
~/.codex/**/*.jsonl                  same
```

Merge those timestamps with a rule such as "gaps of 20 minutes or less belong to the same session" and you get a sequence of work sessions with start and end times. Then classify each as work or private by `cwd`, or by keywords in the session.

Supplementary evidence: file modification times under your work directories, which cover work done without the AI tools.

### What these records do prove

- They are timestamped, auditable, and not reconstructed after the fact.
- They establish directly that you were working during those periods.
- The nature of the work is identifiable (by project directory), rather than a vague claim that the machine was switched on.

### What they do not prove on their own

```text
work-use percentage = time spent working ÷ total time the device was used
```

Tool logs evidence the **numerator** very well. They do not capture the part of the **denominator** that happens outside those tools — web browsing, video, personal email.

So a log of this kind yields "the work share of time spent in these tools", not "the work share of total device use". Leave headroom below the logged figure when claiming.

### Two ways to fill in the denominator

1. **System usage data.** The macOS Screen Time database records foreground time per application, which covers browsers and video. It is protected by default and has to be authorised under Privacy & Security → Full Disk Access before it can be read. It typically retains only about four weeks, so export it early.
2. **A manual record.** Four consecutive weeks of rough daily private-use time is enough; the ATO accepts a reasonable estimate. Only the private side needs recording, since the logs already cover the work side.

### One detail that corroborates authenticity

Where gaps in the log line up with known absences — travel, leave — that shows the record reflects real use rather than being filled in. Point out those coincidences when writing it up.

## 2. Days worked from home

### Deriving them from commuting records

Public transport card travel history lists every journey with date, time and stop. It is a third-party record created at the time.

```text
days at home = working days in the year - public holidays - leave - commuting days
```

Define a commuting day explicitly — for example, "a journey starting from a stop near home, within the morning commute window".

Travel history also validates the pattern of work: if commuting days cluster heavily on two or three fixed weekdays, that is a regular hybrid arrangement, which is itself strong corroboration.

### The limit: it only proves you were in the office

A day with no tap-on could be working from home, annual leave, sick leave — or **driving in**. So days at home derived from travel history is an **upper bound**.

To test whether driving is happening, compare public transport spending against fuel spending across several years. Transport card spending falling sharply while fuel rises means commuting has shifted to the car, and the travel history covers proportionally less.

### More direct evidence

A work calendar (working-from-home markers in Outlook or Teams), timesheets and rosters are forms PCG 2023/1 accepts directly. Travel history is strong corroboration but is strictly an inference — keep both.

## 3. Choosing a home-office method

The two methods are mutually exclusive, and their record-keeping requirements differ:

| | Fixed rate | Actual cost |
| --- | --- | --- |
| Calculation | Hours worked at home for the year × that year's rate | Each actual cost × work-use percentage |
| Covers | Electricity, gas, internet, phone, stationery and consumables | Whatever is itemised |
| Claimable separately | Equipment depreciation | Equipment depreciation |
| **Records required** | **Actual hours for every occasion worked at home, for the whole year** (PCG 2023/1, from 2023-03-01; a four-week sample is not enough) | A four-week representative record of use, plus full-year bills, plus a dedicated work area |

Having chosen the fixed rate, you cannot also claim internet and phone separately.

Work out which is better by calculating both against the actual days at home and standard hours. Do not default to last year's choice. Where days at home are high, the fixed rate is usually better and carries a lighter evidentiary burden.

### Where standard hours come from

Take the monthly standard hours from a payslip and divide by working days in that month. Do not substitute an industry convention — employers differ by more than half an hour a day, which compounds into hundreds of dollars over a year.

```text
hourly rate          = amount of any hourly-paid line ÷ the hours it covers
monthly standard hrs = monthly base salary ÷ hourly rate
daily standard hrs   = monthly standard hours ÷ working days that month
```

## 4. When depreciation starts

Depreciation runs from the date an asset is **first used or installed ready for use** — not the date it was bought.

Equipment bought a few days before year end but not actually put to use until the next year gives a deduction of zero in the first year. The whole amount falls into the following year, and that year is year one.

Evidence for the first-use date: the initial system setup date, the earliest entry in a tool's logs, the first sign-in or activation record.
