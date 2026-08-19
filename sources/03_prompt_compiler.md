# Prompt Compiler

Convert the normalized request and selected style preset into one coherent production prompt.

Do not output raw variables or a list of disconnected style tags.

## Compilation

### 1. Resolve Input

Determine:

```text
INPUT_MODE
STYLE_PRESET
OUTPUT_MODE
VARIATION_MODE
```

Apply defaults from `01_prompt_schema.md`.

### 2. Load the Preset

Load the selected style file from `styles/`.

Use its concrete visual instructions rather than relying only on the preset name.

### 3. Apply Output Mode

Adapt the preset to the selected output mode.

Historical split-layout language from the original source must never force a split layout when `generated-only` is active.

### 4. Apply Preservation

For source-photo and hybrid inputs, incorporate the requested identity, pose, composition, and structural preservation levels.

### 5. Apply Overrides

Apply explicit user changes to:

- aspect ratio
- abstraction
- subject scale
- color
- material
- typography
- text amount
- mood
- rendering
- negative space

Do not remove the defining identity of the preset unless explicitly requested.

### 6. Assemble the Prompt

Use this order when relevant:

```text
Task
Reference handling
Canvas and layout
Subject preservation
Style transformation
Composition
Color
Materials / rendering
Typography
Mood
Negative constraints
```

Write the result as a coherent instruction.

### 7. Independent Variations

When multiple independent results are requested, compile each one separately.

Do not merge separate presets into one prompt unless the user explicitly requests a hybrid style.

## Quality Check

Before returning or using the prompt, verify that:

- output mode and layout do not conflict;
- generated-only does not contain a source-photo comparison panel;
- multiple source images are not unintentionally collaged;
- subject recognizability matches the preservation settings;
- typography amount matches the selected text mode;
- color and rendering follow the selected preset;
- negative constraints target likely failure modes;
- duplicated instructions have been removed.
