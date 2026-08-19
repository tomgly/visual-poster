# Visual Poster — Project Instructions

Use the project source files as the canonical definitions for presets, modes, defaults, and prompt construction.

## Workflow

For each request:

1. Identify the input.
2. Resolve the requested or implied style preset.
3. Resolve the output mode and optional variations.
4. Apply user overrides.
5. Load the selected style definition.
6. Compile a complete prompt using `sources/03_prompt_compiler.md`.

Explicit user instructions take precedence over defaults and preset rules.

## Image Generation

Generate or edit an image only when the user explicitly asks for generation or editing.

If the user asks for a prompt, prompt optimization, style conversion, or prompt variation, return the completed prompt rather than generating an image.

## Source Images

When an uploaded image is used as reference:

- Preserve recognizable identity and defining subject characteristics according to the preservation settings.
- Preserve important pose, structure, spatial relationships, materials, and atmosphere unless the user requests otherwise.
- Do not stretch or distort the main subject to fit the canvas.
- Extend surrounding environment naturally when reframing is necessary.
- Treat multiple uploaded photos independently unless the user explicitly requests a combined composition.

## Output Modes

Output mode overrides historical layout instructions contained in the original source material.

For example, a style originally designed for a split comparison poster must become a full-canvas composition when `generated-only` is selected.

Use `sources/02_input_output_modes.md` as the canonical mode definition.

## Style Presets

Use the selected preset from `sources/styles/`.

Preserve its defining:

- transformation logic
- composition
- color system
- material or rendering method
- typography
- mood
- negative constraints

Do not combine multiple presets unless explicitly requested.

## Prompt Construction

Use `sources/01_prompt_schema.md` to resolve defaults and variables.

Use `sources/03_prompt_compiler.md` to build the final prompt.

Remove redundant instructions and resolve contradictions before returning or using the prompt.

## Response Behavior

When the user requests a prompt, return only the completed prompt unless they ask for explanation or alternatives.

When the user explicitly requests image generation or editing, compile the settings and proceed without asking them to paste the original preset prompt again.
