# Dehumidifier sizing table (ENERGY STAR, current DOE rating basis)

A machine-readable copy of the dehumidifier sizing table published by ENERGY STAR, plus the
one fact that makes two sizing charts disagree while both are honest.

## What this is

ENERGY STAR publishes a sizing table that maps **how damp a space is** and **how big it is**
to a **recommended capacity range in pints per day**. This repository is that table as a CSV,
with the source wording kept intact, so it can be loaded into a spreadsheet, a script, or a
calculator without retyping it from a screenshot.

`data/dehumidifier-sizing-table.csv`

| condition without dehumidification | RH | room band | recommended capacity (pints/day) |
|---|---|---|---|
| Slightly to Moderately Damp | 50–75% | Small-medium (under 2,000 sq ft) | 20–30 |
| Very Damp | 75–90% | Small-medium (under 2,000 sq ft) | 25–40 |
| Wet | 90–100% | Small-medium (under 2,000 sq ft) | 30–50 |
| Slightly to Moderately Damp | 50–75% | Large (over 2,000 sq ft) | 30+ |
| Very Damp | 75–90% | Large (over 2,000 sq ft) | 40+ |
| Wet | 90–100% | Large (over 2,000 sq ft) | 50+ |

The three condition descriptions are ENERGY STAR's own wording, and the RH bands are theirs.
The `suggested_size_pints_per_day` column is **not** published — it is a single number derived
from each range, and the `how_the_suggestion_is_derived` column states the rule used, so you
can ignore it and work from the published range alone.

## Why a chart you found elsewhere may disagree with this one

The US Department of Energy changed the test procedure for portable dehumidifiers. They are
now tested at **65 °F** rather than **80 °F**, to reflect a basement rather than a lab. In
ENERGY STAR's words:

> The new test procedure specifies that portable dehumidifiers are tested at 65 °F, rather
> than 80 °F, to more accurately reflect expected performance in a basement setting. This
> 15 °F reduction in testing temperature means that a dehumidifier tested to the new
> procedure will likely report a smaller capacity than when tested to the old procedure.

The hardware did not change; the number on the label did. A unit sold years ago as a 60-pint
machine is a much smaller machine on today's labels. So when you compare a listing against an
older chart, check which rating basis each side is on first — otherwise you are comparing two
different measurements and will conclude one of them is wrong.

## Two things this table does not cover

- **A whole house or a sealed crawlspace.** Those need a ducted whole-home unit sized from a
  moisture-load calculation, not a portable unit sized from a room chart.
- **Spaces that run cold.** ENERGY STAR notes that if the space typically falls below 65 °F,
  frost can form on the condensing coils and the unit may cycle without removing moisture.
  A unit specified for lower temperatures is the right choice there.

## Source

The table, the condition descriptions and the 65 °F note are from ENERGY STAR's dehumidifier
buying guidance and its page on dehumidifier testing and capacity (energystar.gov). The
underlying test procedure is 10 CFR 430 Appendix X1. Retrieved 2026-10-10.

If you want this table as an interactive calculator rather than a CSV, there is one here:
<https://goodsreviewlab.com/dehumidifier-calculator> — same published values, with the cell
the answer came from shown next to the result.

## Licence

The table is a US government publication. This CSV transcription and the derivation column
are released under CC0 — use them for anything.
