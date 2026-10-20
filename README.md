# SuccessLabs Ideation Dashboard

**Client-agnostic Ideation-to-Value Command Center** — a working, static-first innovation portfolio MVP for enterprise transformation and SuccessLabs Academy learning simulations.

## [Open the dashboard (after enabling GitHub Pages)](https://nbnayak88.github.io/successlabs-ideation-dashboard/)

> **Status:** MVP source published. The live Pages site needs repository Pages deployment configuration before its URL is operational.

### Features
- Responsive innovation portfolio with KPI cards, lifecycle distribution and searchable/filterable register
- Business Line (BL), Enterprise Architecture Office (EAO), Value Realization (VR), Implementation Arm (IA) domain definitions
- Idea details, synthetic financial opportunity estimates, prioritization scoring, and CSV export
- Idea-intake form with local browser storage; stage/budget edits create simulated copies of seeded ideas
- Academy Studio: 11 sector challenges and 12 architecture perspectives
- Client-agnostic role-based identities and fictional data only

**No Power BI or SAP LeanIX.** No dependencies, build step, server, paid hosting or proprietary enterprise integration.

## Run locally
Serve the repository directory using a local HTTP server (ES module imports do not reliably work via `file://`):

```bash
python -m http.server 8000
```

Open http://localhost:8000

## Publish free on GitHub Pages
Repository **Settings → Pages → Build and deployment → Deploy from a branch → main → / (root) → Save**. Wait for Pages deployment, then visit the URL above. This is a user-admin configuration step, not a claim of an existing live deployment.

## Data & security constraints
All records bundled in `src/data.js` are synthetic. Valuations are illustrative, not forecasts or realized benefits. New ideas and edits persist only in your own browser via `localStorage`, are not authenticated or shared, and must not contain sensitive information. The CSV export downloads filtered records locally. Do not use this frontend-only release for confidential production data.

## Architecture
- `index.html`: accessible entry point
- `styles.css`: responsive interface
- `src/data.js`: fictional scenarios
- `src/app.js`: portfolio UI, filters, intake, scoring and local persistence
- `docs/`: product vision, governance and extensibility
- `tests/`: lightweight module/data consistency check

### Roadmap
1. Phase 1: Static-first dashboard and learning simulation (**current**).
2. Phase 2: Authenticated role-based workflows, server-side validation, audit logs and persistence.
3. Phase 3: Secure GitHub issue integrations and optional Notion knowledge export using explicit API permissions.
4. Phase 4: AI-assisted idea shaping and architecture review with grounded evidence and human sign-off.

Ideas flow through **Discover → Evaluate → Architect → Experiment → Deliver → Realize**. The full enterprise-grade workflow is a roadmap, not included in the local demonstration.

## SuccessLabs alignment
Six engines: Knowledge, Attention, Revenue, Transformation, Operating, Leadership.
12 architecture streams × 11 GICS sectors × 20 labs, allowing ideas to become traceable design experiments and learning evidence.

See [Product Vision](docs/product-vision.md), [Domain Model](docs/domain-model.md) and [Roadmap](docs/roadmap.md).
