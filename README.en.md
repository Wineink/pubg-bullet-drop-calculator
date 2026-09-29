# PUBG Bullet Drop Calculator

Live demo: **https://wineink.github.io/pubg-bullet-drop-calculator/**

A fully offline manual ballistics calculator for PUBG (Steam) bullet drop. Open the page and use it directly — it does NOT read game memory/screen and does NOT hook into or scrape any third-party software.

## Features

- 12 bolt-action / DMR rifles: AWM, M24, Kar98k, Mosin, Lynx, Mini14, SKS, SLR, Mk14, Mk12, Dragunov, VSS
- Optics: 4x (3 switchable reticle variants), Hybrid Scope, 6x, 8x (6x/8x with adjustable zeroing)
- Range shortcut buttons 100–450 m, or paste a distance measured by third-party tools
- Two aiming modes: "holdover" (直接抬枪) and "zeroing" (归零后)
- Lateral lead for stationary / walking / running targets (in mil & body lengths)
- Real-time bullet drop, time-of-flight, holdover mils, plus a drop curve chart

## Data Basis

Muzzle velocity uses official/community values; drop and mil readings come from in-match telemetry (Aug–Sep 2026 window, derived from ½gt², g=9.8), monotone cubic interpolation for 0–600 m, model extrapolation above 600 m; telemetry has sampling variance.

## Scope of Use

This tool is a fully offline manual calculator: it does not read game memory/screen, does not integrate with or scrape tools such as LeiShen (雷神), and distances must be entered or pasted manually. For live matches, always verify with in-game Training Ground tests.

## Run / Update

Download `index.html` and open it in any browser — it is a single self-contained file with no external dependencies.

To update the live site: overwrite `index.html` with the latest version and push to the `main` branch; GitHub Pages updates automatically in about a minute.
