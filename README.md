# Visual Poster

[![English](https://img.shields.io/badge/lang-English-2f6feb)](README.md)
[![日本語](https://img.shields.io/badge/lang-日本語-6f42c1)](README.ja.md)
[![Styles](https://img.shields.io/badge/styles-9-238636)](sources/00_style_index.md)
[![ChatGPT Project](https://img.shields.io/badge/ChatGPT_Project-ready-10a37f)](PROJECT_INSTRUCTIONS.md)
[![Prompts](https://img.shields.io/badge/prompts-English-555555)](sources/03_prompt_compiler.md)

A reusable prompt system for transforming photos or themes into distinct editorial poster styles with short instructions.

## Styles

| # | Style | Description |
|---|---|---|
| 1 | `retro-naive-editorial` | Soft retro editorial illustration with mixed-media warmth |
| 2 | `playful-naive-editorial` | Naive art, Bauhaus composition, fashion sketching, and playful visual metaphors |
| 3 | `conceptual-tension-linework` | Minimal black linework expressing tension, connection, restraint, and release |
| 4 | `place-narrative-linework` | Realistic places or themes translated into refined architectural linework |
| 5 | `storybook-printmaking` | Storybook printmaking with bold structural fields and narrative color accents |
| 6 | `poetic-paper-cover` | Small subjects, large negative space, restrained color, and paper texture |
| 7 | `observational-field-notes` | Hand-drawn visual notes, fragments, annotations, and observational details |
| 8 | `pastel-impossible-geometry` | Clean pastel 3D geometry and poetic impossible spaces |
| 9 | `archival-halftone-minimalism` | Silkscreen, halftone, large negative space, and archival editorial typography |
| 10 | `minimal-geometric-editorial` | Recognizable contours, concise geometry, flat color fields, thin linework, and generous negative space |

See [`sources/00_style_index.md`](sources/00_style_index.md) for the full style index.

## ChatGPT Project Setup

1. Create a new ChatGPT Project.
2. Copy [`PROJECT_INSTRUCTIONS.md`](PROJECT_INSTRUCTIONS.md) into **Project Instructions**.
3. Upload all Markdown files inside [`sources/`](sources/) to **Project Sources**.
4. Upload a photo or provide a theme, then specify a style and output mode.

## Usage

Short instructions are enough:

```text
archival-halftone-minimalism, generated only, no text
```

```text
playful-naive-editorial, compare split, minimal text
```

```text
place-narrative-linework
Theme: Yanaka, Tokyo
Mode: compare-split
```

Multiple independent variations:

```text
Create separate variations using:
- retro-naive-editorial
- poetic-paper-cover
- archival-halftone-minimalism
```

## Output Modes

- `generated-only` — Use the source as reference and generate only the transformed result.
- `compare-split` — Show the source and transformed result in a 50/50 vertical composition.
- `retouch-only` — Preserve the photograph and apply only photographic treatment.

For multiple separate outputs, use independent variations rather than a collage.

## Repository Structure

```text
visual-poster/
├── README.md
├── README.ja.md
├── PROJECT_INSTRUCTIONS.md
└── sources/
    ├── 00_style_index.md
    ├── 01_prompt_schema.md
    ├── 02_input_output_modes.md
    ├── 03_prompt_compiler.md
    └── styles/
        ├── 10_retro-naive-editorial.md
        ├── 11_playful-naive-editorial.md
        ├── 12_conceptual-tension-linework.md
        ├── 13_place-narrative-linework.md
        ├── 14_storybook-printmaking.md
        ├── 15_poetic-paper-cover.md
        ├── 16_observational-field-notes.md
        ├── 17_pastel-impossible-geometry.md
        └── 18_archival-halftone-minimalism.md
```
