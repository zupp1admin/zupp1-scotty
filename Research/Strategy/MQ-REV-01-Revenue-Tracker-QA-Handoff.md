# MQ-REV-01 Revenue Tracking Dashboard — Build & QA Handoff

**Output file:** `/home/user/workspace/zupp1-scotty-retention/Research/Strategy/MQ-REV-01-Zupp1-Revenue-Tracking-Dashboard.xlsx`
**Source plan:** MQ-REV-01 — 30-Day Revenue and Six-Month Reinvestment Plan (`MQ-REV-01-30-Day-Revenue-and-Six-Month-Reinvestment-Plan.pplx.md`)
**Builder script (reproducible):** `/home/user/workspace/build_zupp1_tracker.py`
**Print/PDF QA artefacts:** `/home/user/workspace/zupp1-tracker-pdf-qa/MQ-REV-01-Zupp1-Revenue-Tracking-Dashboard.pdf` and page renders `pg-1.png` … `pg-9.png`
**Last revision:** layout/print pass (formulas and logic unchanged — 946 formulas before and after)

## Sheets (in required order)
1. `Executive Dashboard`
2. `Daily Input`
3. `Weekly Summary`
4. `Six-Month Reinvestment`
5. `Definitions & Rules`

## Key cell references

### Executive Dashboard
- KPI cards row 7–10: `B8` Month Spend vs R$600 ceiling, `D8` Settled Revenue, `F8` Marketing Profit, `H8` Blended ROAS vs break-even, `J8` Reinvestment Wallet (each with a live sub-note in row 10).
- Bridge table `B13:H27` — Spend (14), Settled Revenue (15), Fulfilled Orders (16), AOV (17), Verified Margin (18), Contribution (19), CPA (20), Max Allowable CAC (21), ROAS (22), Marketing Profit (23), Reinvestment Wallet (24), Largest Bottleneck (25), Decision (26), Status (27). All cells are green cross-sheet links to `Weekly Summary`.
- Break-even explanation in `B5`; intelligence-gap note in `B30`.
- Clustered column chart (Spend / Settled Revenue / Contribution by period) anchored at `B32`, sized to fit the single printed page.

### Daily Input
- Print layout note: the printed range is the ledger grid only (`A5:AM37`); the sheet title and assumption strip are carried by a page header so they cannot be clipped on horizontal continuation pages.
- Assumptions (blue): `C3` campaign start date (default 17/08/2026), `E3` default contribution margin 10%, `G3` daily cap R$20, `I3` 30-day ceiling R$600.
- Header row 5; 30 data rows `6:35`; raw month totals row 37 (`=SUM(...)`, weighted margin in `T37`).
- Inputs B–Y (blue where editable); formula columns Z–AM: CTR, CPC, LPV Rate, Product View Rate, ATC Rate, Checkout Rate, Purchase CVR, AOV, Contribution, CPA, Max Allowable CAC, ROAS, Marketing Profit, Reinvestment Wallet — all guarded with `IF(N(...)=0,"",IFERROR(...))`, so no #DIV/0.
- Week bucket `C6`: `=IF($B6="","",IF($B6-$C$3+1>28,"Closeout","Week "&ROUNDUP(($B6-$C$3+1)/7,0)))`.
- Dropdowns on Tracking Status (V), Checkout Status (W), Product Availability (X); numeric validation on Spend (H) and Margin (T).
- Freeze `D6`, autofilter `B5:AM35`, landscape fit-to-width, repeating header row.

### Weekly Summary
- Period criteria keys in row 6 (`Week 1`…`Closeout`), Month Total column H = `SUM` of raw daily ranges (not averages of averages).
- Core economics rows 8–23; funnel diagnostics rows 26–39; hard-stop counter row 40; Largest Funnel Bottleneck row 41 (`MIN`/`MATCH`/`CHOOSE` over rates 35:39); Diagnostic Flag row 42 (50 LPV / 10 ATC / 5 checkout heuristics); Recommended Decision row 43; Status row 44.
- Decision ladder (row 43): hard stop logged → STOP; no spend → HOLD / INSUFFICIENT DATA; month spend ≥ ceiling with zero fulfilled orders → STOP; profit > 0 and ≥ 2 fulfilled orders → CONTINUE; ≥ 1 fulfilled order → CHANGE ONE VARIABLE; spend ≥ MAX(path-stop floor, 2 × max allowable CAC) → CHANGE ONE VARIABLE; else HOLD.
- WoW variance block rows 47–54 (Δ and % for Spend, Settled Revenue, Fulfilled Orders, CPA, Marketing Profit; Closeout excluded as a 2-day period).

### Six-Month Reinvestment
- Assumptions: `C6` opening principal R$600 (blue), `C7` margin 10% (blue), `C8` default excluded variable costs (blue, explicit 0 placeholder with comment), `C9` Month 1 settled revenue linked to `Weekly Summary!H11` (green).
- Loop rows 14–19: `I` Marketing Profit `=G−C−N(H)`; `J` Next Available Budget `=IF(I<0,"",C+I)`; `K` status (STOP / HOLD / REINVEST). `C15` chains from `J14`, so a negative month halts the loop automatically.
- Cumulative totals row 20; available budget after Month 6 in `C21`.
- Illustrative scenarios rows 26–34 at 8.0x / 10.0x / 12.0x (blue ROAS inputs `C27:E27`), reproducing the plan exactly: 12x → 600, 720, 864, 1,036.80, 1,244.16, 1,492.99, 1,791.59; 10x → flat 600; 8x → STOP from Month 2. Labelled illustrative arithmetic, not a forecast (`B25`, `B10`, `B36`).

### Definitions & Rules
- Metric definitions, FACT / ASSESSMENT / RECOMMENDATION / INTELLIGENCE GAP labels, immediate hard stops, economic stops, diagnostic heuristics, scaling rules, decision-value glossary, daily data-entry checklist, outstanding intelligence gaps, colour convention.
- Clickable official Meta sources: Meta Pixel conversion tracking, website purchase ads, learning-phase guidance.

## Formatting conventions
Calibri throughout; teal `#1B474D` / `#20808D` headers with neutral banding; blue font = user inputs, black = same-sheet formulas, green = cross-sheet formulas. Currency `"R$" #,##0.00` (zeros display as `–`), percentages `0.0%`, ROAS `0.0"x"`, dates `dd/mm/yyyy`. Decision, status, ROAS, profit, CPA-vs-CAC, hard-stop and scenario STOP cells use conditional-formatting rules (no static fills). Freeze panes, autofilter, print areas and fit-to-width page setup on every sheet; cell comments on start date, margin, spend cap, settled revenue, excluded costs, reinvestment wallet, path-stop floor and SUMIFS keys.

## Layout / print revisions (second pass)

All changes are formatting-only. No formula, range, conditional-formatting rule, validation or decision-logic change was made; the recalculated formula count is identical (946) and the recalculated values are unchanged.

**1. Executive Dashboard now prints on one landscape page.** Chart height reduced 9.5 → 7.2 cm and re-anchored `B33` → `B32`; print area tightened `A1:K52` → `A1:K46`; `fitToHeight=1` with `horizontallyCentered`. Core tables kept at full size — only the chart was shrunk. Confirmed: page 1 of the PDF holds the KPI cards, the full 14-line bridge and the chart, with nothing spilling to page 2.

**2. Clipped labels fixed.**
- Daily Input assumption labels (`B3` campaign start date, `D3` default contribution margin, `F3` daily budget cap, `H3` 30-day spend ceiling) now wrap, with row 3 height 34; all four display in full.
- Daily Input month-total banner: label merged across `B37:G37`, left-aligned, and reworded to "MONTH TOTAL (raw aggregation of all 30 days)" — previously clipped to "ONTH TOTAL (raw".
- Daily Input columns O and P (Attributed / Fulfilled Orders) widened 12 → 14 so the headers are not cut.
- Weekly Summary "Stated contribution margin" was outside the print area (value sat in `I3`, print area ends at H). Label moved to merged `E2:G2` with the value in `H2` (green cross-sheet link to `'Daily Input'!$E$3`, `0.0%`) — the pair now prints. `I3` is gone; nothing referenced it.
- Weekly Summary section headers (`CORE ECONOMICS`, `FUNNEL DIAGNOSTICS`, `WEEK-OVER-WEEK VARIANCE …`) are merged `B:H` with fixed 18 pt height, so long titles no longer clip.
- Six-Month Reinvestment: columns C–J widened 17 → 18 and header row 13 raised 44 → 50 pt, so "Marketing Profit P(t) (R$)" and "Next Available Budget A(t+1) (R$)" render fully; column B widened to 48.
- Definitions & Rules: the colour-convention note and the closing amber intelligence-gap note are merged `B:C` with `wrap_text`, top alignment and explicit row heights (18 / 32 pt); source-link rows raised to 28 pt. Nothing is cut at the right edge.

**3. Daily Input print layout is legible instead of compressed.** `fitToPage` is off; the sheet prints at 62 % scale across three horizontal landscape pages, with header row 5 repeated (`print_title_rows`) and the Date/Week identifier columns repeated on every page (`print_title_cols="$B:$C"`). The on-screen workbook view is unchanged and remains the primary experience (freeze `D6`, autofilter `B5:AM35`).

**4. Definitions & Rules stays clean across its two pages** (portrait, fit-to-width, page break falls between the decision-value glossary and the data-entry checklist; no clipped cells, sources still clickable).

**5. Page footers added** to every sheet (`Sheet name · page &P of &N`) plus a Daily Input page header. Margins widened slightly on all sheets to accommodate them.

**Resulting PDF:** 9 pages — 1 Executive Dashboard, 2–4 Daily Input (three horizontal pages), 5–6 Weekly Summary, 7 Six-Month Reinvestment, 8–9 Definitions & Rules. All nine pages were rendered at 95 dpi and inspected.

## QA result
- LibreOffice recalculation after the layout pass: **946 formulas, 0 errors** (`status: success`, empty error summary).
- Delivered workbook ships empty of invented results: all observation cells blank, only dates, default assumptions and formulas populated; blanks render as `–` or stay empty rather than showing 0.
- Live-logic smoke test on a throwaway copy (`/tmp/smoke.xlsx`, not the deliverable) with synthetic data recalculated with 0 errors and produced correct behaviour: Week 1 `CHANGE ONE VARIABLE` + "50+ LPVs, 0 ATC" flag; Week 2 `CONTINUE` / `PROFITABLE`; Week 3 `STOP` after a "Missing" tracking entry; Month Total CPA 21.43 computed from raw sums (not the mean of weekly CPAs); WoW deltas and Six-Month Month 1 reinvestment (`REINVEST`, next budget R$630) all correct.
