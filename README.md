# Production & Industrialisation Readiness Dashboard

A single-file, zero-install readiness control tower for production and
industrialisation projects.

**Live:** https://hm4ri.github.io/readiness-dashboard/

## What it is

`index.html` is the whole application — no build step, no server, no database,
no external requests. Open it directly in any modern browser (double-click on a
PC, or open the Pages link on a phone) and it works offline.

## What it shows

- Overall weighted readiness gauge and gate health (G0–G6)
- Readiness by category with the exact hanging process (category → stage → sub-process)
- "Where are we hanging?" bottleneck view and hanging-process table
- Category detail pages, documents register and owners
- Cycle time vs takt, capacity readiness, trend, risk quadrant and pareto
- Management summary and the next five actions

## Readiness maths

Weighted across criteria: `Σ(weight × effective %) / Σ(weight × 100)`

| Status | Effective % |
| --- | --- |
| Completed | 100 |
| In Progress | actual % |
| Not Started | 0 |
| Blocked | 0 |
| N/A | excluded from the denominator |

## Editing the data

Data lives in the browser session. Use the admin area to edit projects,
categories, sections, criteria, documents, owners and gates, then **Export JSON**
to keep a copy. **Import JSON** loads it back on any device.
