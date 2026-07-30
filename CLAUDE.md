# CLAUDE.md - Research Trajectory Presentation (Quarto/Reveal.js)

## Project Context
You are helping me build a 10-minute research trajectory presentation for a job talk/selection committee. The style must emulate a polished Apple Keynote presentation, using a horizontal timeline as the primary storytelling device.

## Core Requirements
- **Total Slides**: Exactly 10 slides.
- **Total Duration**: 10 minutes (1 minute per slide).
- **Output Format**: `revealjs` (HTML) for native auto-animate and CSS control.
- **Primary Visual**: A horizontal timeline that persists subtly across slides but "zooms in" on specific nodes using `data-auto-animate`.

## File Structure to Create
Create a single functional `.qmd` file (e.g., `index.qmd` or `slides.qmd`) with the following components:

1.  **YAML Header**: Configure `revealjs` with custom CSS, transition speed, and auto-animate settings.
2.  **Custom CSS**: Define the color palette (60/30/10 rule), fonts, and timeline styling.
3.  **Slide Content**: Exactly the 10 slides defined below.
4.  **Code Chunks**: Generate synthetic plots using `matplotlib` (Python) for the "Discovery" slides if I haven't provided actual data—use placeholders I can easily replace.

---

## Language and style

- The language of the slides should be in Spanish
- The style should look professional, minimalist and engaigin.

---

## Financiamiento en evaluación (2026)

Además de los proyectos ya adjudicados (ANID, +CLP 1.200 MM), este año se presentaron dos nuevas propuestas, cada una asociada a una de las dos líneas de origen de la trayectoria (sequía/ODES-Chile y riego deficitario/SatOri):

- **FONDECYT Regular (CLP 220 MM)** — *"Optimising crop transitions for water use efficiency under aridification: an integrated biophysical-ecological-economic framework for Mediterranean perennial orchards"*. Asociado a la línea ODES-Chile / sequía y aridificación.
- **Fondo de Innovación Agraria, FIA (CLP 90 MM)** — *"PsiSat: validación sistema de optimización de riego en cerezo basado en potencial hídrico"*. Asociado a la línea SatOri / riego deficitario.

Además, dos manuscritos en revisión/consideración, ambos asociados a la línea ODES-Chile / sequía:

- **En revisión, Journal of Hydrology** — *"Agricultural land-use composition modulates hydroclimatic coupling of cropland water use efficiency under prolonged aridification: sub-watershed evidence from Chile's megadrought"* (Zambrano, Fernández, Molinos-Senante). Preprint: https://doi.org/10.31223/X5QF59.
- **Bajo consideración, Nature Water** — *"Dams mark multi-year drought vulnerability rather than buffer it in Chile's megadrought"*. Enviado 04/07/2026, editor asignado 09/07/2026.

---

## 1. YAML Configuration
Use this specific header. It enables auto-animate for the "Magic Move" effect.

```yaml
---
title: "Research Trajectory"
author: "[Your Name Here]"
format:
  revealjs:
    theme: [default, custom.scss] # or use CSS directly
    transition: slide
    auto-animate: true
    auto-animate-unmatched: true
    auto-animate-duration: 0.8
    slide-number: true
    preview-links: auto
    code-overflow: wrap
    footer: "Trajectory Talk · 10 mins"
    css: styles.css
---

---

#3. The 10 Slides - Content Structure

Build the .qmd slides exactly as follows. Use ## for slide titles.

## Slide 1: Title & North Star

- Title: Your Name.
- Subtitle: [Your overarching research question/mission].
- Visual: A full-bleed abstract background image (placeholder).
- Timer: 0:45.

## Slide 2: The Grand Overview

- Title: "The Arc of Inquiry".
- Visual: A Mermaid.js diagram or a raw HTML/CSS horizontal line with 3 nodes: Past (Foundation) → Present (Deep-Dive) → Future (Vision).
- Timer: 0:45.

## Slide 3: The Origin Problem

- Title: "The Starting Challenge".
- Content: Left side = "The Problem" (one sentence). Right side = placeholder image of an obstacle (e.g., messy data, theoretical gap).
- Timer: 1:00.

## Slide 4: First Victory

- Title: "Building the First Framework".
- Content: A generated plot (e.g., matplotlib line chart showing improvement over baseline) with a single callout box: Key Insight: [Finding].
- Timer: 1:00.

## Slide 5: The Pivot (Auto-Animate Target)

- Title: "The Forced Question". Set data-auto-animate on this slide to zoom into the "Present" node of the timeline.
- Content: A large arrow turning 90 degrees. Text: "But this forced me to ask...".
- Timer: 0:30 (Fastest slide).

## Slide 6: Present - The Approach

- Title: "Tackling the New Frontier".
- Content: Workflow diagram (Input → Novel Method → Expected Output).
- Timer: 1:15.

## Slide 7: Present - The Breakthrough

- Title: "The Critical Result".
- Visual: A striking matplotlib plot (heatmap, complex scatter, or contour) showing your best current data.
- Text: A single bold sentence at the bottom: "This reveals that...".
- Timer: 1:15 (Climax).

## Slide 8: Synthesis (The Red Thread)

- Title: "Connecting the Dots".
- Visual: A Venn Diagram (CSS styled or generated) showing:
    - Circle 1: Skills from Past.
    - Circle 2: Knowledge from Present.
- Overlap: My Unique Niche.
- Timer: 1:00.

## Slide 9: The Future (3 Aims)

- Title: "Future Directions".
- Visual: 3 interlocking/stacked boxes.
    - Aim 1: [Idea].
    - Aim 2: [Idea].
    - Aim 3: [Idea].

Use fragment reveals to show them one by one.
- Timer: 1:00.

## Slide 10: Closing

- Title: "Thank You".
- Content: The "So What?" takeaway sentence. Logos of your mentors/lab. Acknowledgment line.
- Timer: 0:30.