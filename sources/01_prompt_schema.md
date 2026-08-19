# Prompt Schema

Normalize each request using this schema before compiling the prompt.

Users do not need to specify every field.

## Core Fields

```text
STYLE_PRESET
INPUT_MODE
OUTPUT_MODE
```

## Defaults

```text
ASPECT_RATIO = 3:4
OUTPUT_MODE = generated-only
STYLE_STRENGTH = strong

IDENTITY_PRESERVATION = high
POSE_PRESERVATION = high
COMPOSITION_PRESERVATION = medium

TEXT_MODE = style-default
COLOR_MODE = style-default
ABSTRACTION_LEVEL = style-default

VARIATION_MODE = single
```

Infer `INPUT_MODE` automatically:

```text
uploaded image only          → source-photo
written theme only           → theme
image + meaningful context   → hybrid
```

## Input Modes

```text
source-photo
theme
hybrid
```

## Output Modes

```text
generated-only
compare-split
retouch-only
```

## Variation Mode

```text
single
independent
```

`independent` means every requested variation must be produced separately, never as a collage unless explicitly requested.

## Preservation Levels

```text
none
low
medium
high
strict
```

### IDENTITY_PRESERVATION

Controls recognizable identity and defining subject characteristics.

### POSE_PRESERVATION

Controls gesture, body orientation, object orientation, and characteristic stance.

### COMPOSITION_PRESERVATION

Controls viewpoint, subject placement, scale, and spatial relationships.

## Text Modes

```text
style-default
none
micro
minimal
editorial
annotated
```

`style-default` uses the typography behavior defined by the selected preset.

## Color Modes

```text
style-default
source-derived
source-temperature
custom
```

## Style Strength

```text
subtle
moderate
strong
maximal
```

## Abstraction Level

```text
style-default
low
medium
high
extreme
```

## Optional Overrides

```text
BACKGROUND
PALETTE
ACCENT_COLOR
MATERIALS
TYPOGRAPHY
TEXT_CONTENT
LOCATION
TIME
WEATHER
MOOD
SUBJECT_SCALE
NEGATIVE_SPACE
CAMERA_VIEW
RENDERING
```

## Precedence

Resolve conflicts in this order:

```text
1. Explicit user instruction
2. Output mode
3. User overrides
4. Selected style preset
5. Project defaults
```
