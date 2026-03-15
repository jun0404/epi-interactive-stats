# Interactive Epidemiological Statistics

An interactive, browser-based tool for exploring epidemiological measures with real-time patient timeline manipulation.

## Features

- **Draggable patient timelines** — adjust follow-up day by dragging directly on the timeline
- **Full formula breakdowns** — every statistic shows per-patient numerator/denominator contributions
- **42-day prevalence/incidence cutoff** — adjustable via slider; reclassifies patients in real time
- **Ambiguous case handling** — patients without confirmed baseline TB-negative status are flagged and excluded
- **Responsive layout** — side-by-side on wide screens, stacked on portrait/mobile

## Statistics Computed

| Category | Measures |
|---|---|
| Prevalence | Point prevalence |
| Incidence | Cumulative incidence (risk), incidence rate (person-time) |
| Stratum-specific | CI and IR for exposed vs. unexposed |
| Association | Risk ratio, rate ratio, odds ratio, hazard ratio (approx.) |
| Impact | Risk difference, AFe, PAF, NNT/NNH |
| Relationship | P ≈ IR × D (steady-state approximation) |

## Deployment

This is a static single-page site. No build step required.

```bash
# Local preview
npx serve public

# Deploy to Vercel
vercel --prod
```

## Tech Stack

- Vanilla HTML/CSS/JS (no framework)
- [KaTeX](https://katex.org/) for math rendering
- [DM Sans](https://fonts.google.com/specimen/DM+Sans) + [Fraunces](https://fonts.google.com/specimen/Fraunces) + [DM Mono](https://fonts.google.com/specimen/DM+Mono) typography
