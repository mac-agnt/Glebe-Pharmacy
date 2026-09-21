# Project notes

## Source of truth
Pulse is an attached local codebase folder (`Pulse/`), not a GitHub repo. Browse with the
`local_*` tools (`local_ls`, `local_read`, `local_grep`). Key docs:

- `Pulse/docs/ARCHITECTURE.md` — layers, record spine, module contract, permissions, Helios chain
- `Pulse/docs/HELIOS.md` — tools, effects (read/write/external), confirmation hashes, channels
- `Pulse/packages/core/src/domain/core-module.ts` — core routes + navigation (sections: primary, work, data, admin)
- `Pulse/apps/demo/pulse.config.ts` — client config: branding, terminology, modules, home widgets, features
- `Pulse/packages/modules/site-visits` — the reusable module fixture

## Mockup files
- `Pulse v4 Glass.dc.html` — the Durkin Pharmacy Group build: dark liquid glass, deep green
  brand (#1E5B4A) with warm stone accent (#C9A96A), icon rail with hover labels, Home = Helios
  chat + right rail. Modules in the sidebar, pages in the top bar:
  Home · Agents · Dashboard (Overview, Margin, Service Standard) · Pricing (Price Book, Variance,
  Margin by Category, Suppliers) · Work (Tasks, Approvals, Rosters, Hours, Workflows, Schedules) ·
  Records (Contacts, Dispensing, Files, Ontology) · Activity · Settings.
  Every number comes from the `F` facts block and the `SHOPS` list at the top of the logic script,
  so a badge and the rows behind it cannot drift apart. See DEMO-SCRIPT.md.
- `Pulse v2.dc.html`, `Pulse v3 Apple.dc.html`, `Pulse v3 Console.dc.html`, `Pulse Home.dc.html` — earlier directions, keep.

## Running the demo
- `python3 serve.py` (or double-click `Start Demo.command`) serves `Pulse v4 Glass.dc.html` at
  http://pulse.localhost:8080, plus only the files it needs. The preview pane's launcher can't read
  ~/Downloads (macOS privacy), so start the server from the shell and attach the pane via `.claude/launch.json`.
- `vendor/` holds React 18.3.1 and the fonts so the demo runs offline; the page loads them before `support.js`.
- Upcoming dates in the mockup data are computed from today (helpers at the top of the logic script).
- `DEMO-SCRIPT.md` lists the questions Helios has real answers for.

## Conventions the mockups should keep
- Helios never executes write/external tools; it proposes and waits for a confirmation bound to hashed arguments.
- The action inbox answers three things per item: what happened, why it matters, what I can do.
- Metrics, nav, pages and Helios tools all come from the registry — module contributions are labelled as the module's.
