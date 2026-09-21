# Pulse demo script — Durkin Pharmacy Group

Four pharmacies in Sligo Town, €5.5M turnover, 34 staff, run on Google Sheets and WhatsApp.
Pat Durkin can drive the business when he is standing in a shop. This is what he reads when he is not.

## Start and stop

1. Double-click **Start Demo.command**. Chrome opens at **http://pulse.localhost:8080**.
2. Close that Terminal window when you're done. That stops the demo.

The first time, macOS may ask whether Terminal can access your Downloads folder: click **Allow**.
No internet needed; React and the fonts are bundled in `vendor/`.

## The five screens, in order

| Pain | Screen | The number |
|---|---|---|
| "I can drive it when I'm there. When I'm not, I can't." | **Home**, then **Dashboard › Overview** | Group KPIs, then drill to any of the four shops |
| No uniform pricing across the four shops | **Pricing › Variance** | 212 of 1,480 lines, widest gap €4.60, €118,000 a year |
| Gross margin two to three points light | **Dashboard › Margin** | 22.4% against a 25.1% benchmark — 2.7 points, €148,500 a year |
| Paid on rostered hours, not hours worked | **Work › Rosters**, then **Work › Hours** | 3 uncovered shifts; 612 rostered against 587 worked, €8,160 a year |
| No proof the philosophy is alive in every shop | **Dashboard › Service Standard** | 94 interactions logged, 6 customers left with nothing agreed |

## Questions Helios answers

Type these on Home, or click the matching suggestion. The wording can change; Helios listens for the key words.

| Ask | Helios shows | Key words it listens for |
|---|---|---|
| Where are the four shops priced differently? | 212 lines, €118,000 a year, the three widest gaps | price, priced, pricing, variance, cheaper, dearer, gap |
| Why is margin 22.4%? | 22.4% against 25.1%, each shop against the benchmark | margin, benchmark, gross, profit, ebitda |
| Rostered against worked hours | 612 against 587, the 25-hour gap by shop | hours, roster, rostered, worked, shifts, cover, wages |
| How did service score this week? | 94 logged, 6 flagged, three of them at Eden Quay | service, standard, customers, interactions, counter |
| How did the PCRS claims land? | 14 rejected of 11,200 items, and why | pcrs, claims, rejected, dispensing, scheme, gms |
| Set one price across the four | A write tool: drafts it and waits for your yes | set, write, one price, align, fix the prices |

Anything else gets: "Everything I reach goes through a registered tool with a declared permission, and none of them covers that question yet." It then offers buttons for the questions above, so click one and carry on.

## Watch out for

- **Set one price:** stop at the **NEEDS YOUR YES** card, which is the point to make. Writing prices to Touchstore is an external tool, so it never runs on its own.
- **Both themes work.** The accent is the same stone in dark and the same deep green in light; there is no leftover colour from the template.
- **Old link:** `localhost:8080/Pulse%20v4%20Glass.dc.html` no longer works. Use http://pulse.localhost:8080.

## Where the numbers come from

Every figure on every screen derives from one block at the top of the logic script in
`Pulse v4 Glass.dc.html`: `F` (the headline facts), `SHOPS`, and the generators built on
them (`SKUS`, `VARIANCE`, `STAFF`, `HOURS`, `ROSTER`, `SERVICE_SHOPS`, `DISPENSING`).
Change a number there and the badge, the rows behind it and what Helios says all move together.
