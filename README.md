# AquaSmart — Drone Water-Waste Detection Dashboard

A React + TypeScript + Vite **interactive hackathon MVP** for visualizing possible irrigation problems detected from drone imagery.

## Run locally

Requirements: Node.js 20.19+ or 22.12+ and npm.

```bash
npm install
npm run dev
```

Open the URL printed by Vite (usually http://localhost:5173).

To check a production build:

```bash
npm run build
npm run preview
```

## What works

- Responsive dashboard with water usage, cost estimates, detected problem areas and field status.
- Clickable example field heatmap and field details.
- Inspection workflow: add notes, mark alerts inspected, and persist in browser localStorage.
- Alerts, fields, scan history, trend chart and CSV report export.
- Upload a drone image and preview it beneath the example heatmap overlay (up to 12 MB).
- Adjustable example water rate and farm name saved locally.

## Important prototype limitations

**No AI or drone integration is connected.** Heatmap overlays and alerts are illustrative and are NOT inferred from uploaded images. Uploaded photos are stored only in memory for the current page session, while the scan name/history and inspection records persist locally. The example farm map is synthetic, not an actual aerial photograph, and its polygon boundaries are not georeferenced. Water consumption, costs, crop condition and weather are sample data. Never use the demo to make real irrigation decisions.

To make it production-capable, implement a FastAPI image processing endpoint, a trained and validated detection/segmentation model, geo-referenced image mapping, drone-image storage, authentication, a database, real water meter data and real weather API integration. A detected wet patch alone does not prove leakage.

## Stack

React 18, TypeScript, Vite, Lucide React, Recharts, CSS.
