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

### Importing from Excel

Under **Admin → Readiness criteria**, use **Download Excel template** to get a
spreadsheet with the expected columns (Category, Section, Title, Status,
% Complete, Weight, Owner, Gate, Risk, Due Date, …), fill it in, and use
**Import Excel…** to upload it back. Accepts `.xlsx`, `.xls` or `.csv`.
Categories, sections and owners that don't exist yet are created
automatically; a preview shows exactly what will change before anything is
written. Everything is parsed in your browser — the file is never uploaded
anywhere.
