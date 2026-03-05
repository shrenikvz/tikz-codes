# TikZ Figure Library for Research

This repository is a curated collection of reusable TikZ/LaTeX figures developed for research.  
The goal is to provide publication-ready visual templates that are easy to modify, extend, and reuse across papers and projects.

## Repository Goals

- Keep research figure source code centralized and version-controlled.
- Make customization straightforward for other researchers.
- Follow clean, maintainable LaTeX/TikZ engineering practices.

## Current Figure Catalog

| File | Figure Type | What to Edit First |
|---|---|---|
| `box_plot.tex` | Comparative box plots for two methods | Method names/colors, sample labels, CSV blocks |
| `heat_map.tex` | 2D heatmap with colorbar | Title/axis labels, colormap, `z` values in CSV |
| `neuron.tex` | Single-neuron computation diagram | Input/output labels, equation terms, sizing |
| `neural_network.tex` | Fully connected feed-forward network | `\LayerSizes`, layer labels, node colors/spacing |
| `rnn.tex` | Stacked RNN layer/time-step layout | Time labels, layer names, spacing and colors |

## Figure Design Convention

Each `.tex` file follows the same structure:

1. **Customization block at the top** for labels, colors, spacing, and data.
2. **Drawing logic below** that should rarely need edits.
3. **Standalone compilation** (`standalone` class) for easy export and reuse.

This allows users to adapt figures quickly by modifying configuration values without rewriting TikZ geometry.

## How to Compile

Compile any figure directly (example):

```bash
pdflatex box_plot.tex
```

Or use your preferred LaTeX workflow (e.g., `latexmk`) for iterative builds.

## Maintenance Workflow

As new Overleaf figure code is added:

1. The figure is integrated into this repository.
2. The source is refactored for clarity and easy customization.
3. `README.md` is updated with new entries and usage guidance.

## Long-Term Vision

This repository is intended to become a practical figure toolkit for researchers who want to:

- bootstrap high-quality visuals quickly,
- tailor existing diagrams to new experiments,
- and share reproducible, editable figure sources with collaborators.
