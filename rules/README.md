# Rules layer · 规则层

*The method documents in `docs/` explain **how to work**. This layer records **what the rule is for a given year**, where it came from, and when it was last checked.*

*`docs/` 说的是**怎么做**，这一层记的是**某个财年的规则是什么**、出处在哪、最后一次核对是什么时候。*

## The split · 分层依据

| Stays in `docs/` | Lives in `rules/YYYY-YY/` |
| --- | --- |
| Legislated and structurally stable — Div 43 commencement dates, the s40-27 date, the $300 and $1,000 thresholds, the 18.75% first-year pool rate, TR and case references | Annually indexed or administratively set — the WFH fixed rate, the tax scale, Medicare thresholds, MLS tiers, cents-per-kilometre |

A figure that has not moved since 1997 does not need a `last_verified` date; a figure the ATO reissues every year does. Mixing the two makes the stable ones look doubtful and the volatile ones look settled.

## Why these files are bilingual rather than mirrored

Every other document in this repository has an English original and a Chinese translation. This layer does not, deliberately: **a rate must exist in exactly one place.** Two language copies of `70 cents` will eventually disagree, and a rules layer that disagrees with itself is worse than no rules layer at all. So the value is stated once and the surrounding explanation carries both languages.

## Contract · 每条规则四要素

```text
Rule          what applies, stated so it can be acted on
Source        a specific ATO page or ruling, not "the ATO website"
Last verified an ISO date — a human opened the source and read it
Risk          low | needs-review
```

`low` — checked against the source on the date shown, and the source was unambiguous.
`needs-review` — not verified for this year, or the source is ambiguous, or the figure is indexed and may have moved. **Never use a `needs-review` value in a calculation without opening the source first.**

An unverified rule is left explicitly empty. It is not filled in from memory, from last year, or from a general-knowledge estimate — a plausible wrong number is more dangerous here than a blank.

## Annual maintenance · 年度维护

At the start of each financial year, copy the previous directory, set every `Risk` to `needs-review`, then verify downwards. What survives verification keeps its value; what has moved gets the new one; what cannot be confirmed stays blank.
