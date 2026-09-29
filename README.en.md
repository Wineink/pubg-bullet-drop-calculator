# PUBG Bullet Drop Calculator

Live demo: **https://wineink.github.io/pubg-bullet-drop-calculator/**

A fully offline manual ballistics calculator for PUBG (Steam) bullet drop. Open the page and use it directly — it does NOT read game memory/screen and does NOT hook into or scrape any third-party software.

## Features

- 12 bolt-action / DMR rifles: AWM, M24, Kar98k, Mosin, Lynx, Mini14, SKS, SLR, Mk14, Mk12, Dragunov, VSS
- Weapon category filter: All / Bolt-action SR / DMR (the other category is dimmed)
- Optics: 4x (3 switchable reticle variants: chevron / cross / circle), Hybrid Scope (reuses the 8x high-power reticle), 6x, 8x (6x/8x with adjustable zeroing)
- **Real in-game reticles**: the 4x variants, 6x and 8x reticles are actual reticles cut out from in-game screenshots (inline transparent PNGs) — no housing/fill background, reticle only, enlarged display
- **8x holdover calibration**: calibrated from live testing (AWM at 300 m lands on the first mil dot), so the red dot matches the real in-game ticks
- **Customizable red dot**: size (1.5–8 px radius) and color (8 choices)
- **Reticle center adjustment**: ±30 fine-tune on X / Y to align the dot with the reticle center
- Range shortcut buttons 100–800 m (every 50 m); mouse wheel on the input field adjusts ±5 m per notch, or paste a distance measured by third-party tools
- Two aiming modes: "holdover" (直接抬枪) and "zeroing" (归零后)
- Lateral lead for stationary / walking / running targets (in mil & body lengths)
- Real-time bullet drop, time-of-flight, holdover mils, plus a drop curve chart

## Data Basis

Muzzle velocity uses official/community values; drop and mil readings come from in-match telemetry (Aug–Sep 2026 window, derived from ½gt², g=9.8), monotone cubic interpolation for 0–600 m, model extrapolation above 600 m; telemetry has sampling variance. Holdover is computed relative to the 100 m zero (milAt(R) = telemetry mil(R) − mil(100)).

## Reticle Assets

Reticles are cut out from in-game screenshots as transparent-background PNGs, keeping the real reticle plus a thin black ring:

- `瞄准镜_带黑圈/` — real reticle + thin black outline circle
- `瞄准镜_纯分划/` — reticle only (no ring)

Coverage: 3x, 4x (chevron / cross / circle), 6x, 8x, 15x. The page currently enables the 4x variants, 6x and 8x (Hybrid Scope reuses the 8x high-power reticle).

## Scope of Use

This tool is a fully offline manual calculator: it does not read game memory/screen, does not integrate with or scrape tools such as LeiShen (雷神), and distances must be entered or pasted manually. For live matches, always verify with in-game Training Ground tests.

## Run / Update

Download `index.html` and open it in any browser — it is a single self-contained file with no external dependencies.

To update the live site: overwrite `index.html` with the latest version and push to the `main` branch; GitHub Pages updates automatically in about a minute.
