---
name: make-diagram
description: Produces a clear diagram from a described system, process, or concept — picks the right notation (Mermaid or standalone SVG), enforces layout discipline, and verifies the output renders. Use when asked to "draw a diagram", "visualize this architecture", "make a flowchart", "нарисуй схему", "диаграмма процесса".
---

# Make Diagram

## Overview

Description in, diagram out — as a rendered artifact, not ASCII art or prose pretending to be one. The discipline that separates a readable diagram from a hairball: fix the layout before drawing, and cap the element count.

## When to Use

- Architecture, data flows, process flows, sequences, state machines, org/concept maps, decision trees
- NOT for: data charts (bars, lines, plots — that's data visualization, different tooling), or pixel-perfect brand design work

## Process

1. **Extract the model first:** nodes (≤9 primary elements — more means grouping into subgraphs or splitting into two diagrams), groups/zones, directed relationships with their labels. Ask nothing unless the structure is genuinely ambiguous.
2. **Pick the format by destination:**
   - **Mermaid** (default) — renders natively in GitHub, GitLab, Notion, Obsidian, and most agent UIs; editable as text; diffable in git. Flowchart LR/TD, sequence, state, ER, or C4-style — whichever matches the model
   - **Standalone SVG in a single HTML file** — when the user needs polished visuals, custom layout, or the target has no Mermaid rendering. Inline everything: no external fonts, scripts, images, or network requests of any kind
3. **Pick the layout before drawing:** left-to-right for pipelines and request flows, top-down for hierarchies and decisions, swimlanes for multi-actor processes, hub-and-spoke for one-to-many. Flow direction is consistent — arrows that double back mean the layout is wrong, not the arrows.
4. **Drawing rules:**
   - Labels ≤3 words on nodes, ≤2 words on edges; the diagram shows structure, the surrounding text explains it
   - Color = meaning, sparingly: one accent for the critical path or risk zone beats six decorative colors. Same shape/color = same kind of thing, everywhere
   - Group related nodes into named containers (subgraphs/zones) instead of letting edges do all the work
   - Legend only when a symbol isn't self-evident
5. **Verify before delivering:** Mermaid — syntax-check it (render it, or run it through an available Mermaid parser; a diagram that doesn't compile is not delivered). SVG — open/parse the file; check no text overflows its box and nothing overlaps.
6. **Deliver** the source (fenced ```mermaid block or the .html file) plus a one-line reading hint ("read left to right; red path is the failure mode").

## Verification

- [ ] Primary element count ≤9 or grouped/split with reason
- [ ] Output actually renders — syntax verified, not assumed
- [ ] One consistent flow direction; no crossing spaghetti where a layout change would fix it
- [ ] SVG mode: zero external references (fonts, scripts, images, URLs)
