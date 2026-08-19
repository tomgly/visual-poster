# Input, Output, and Variation Modes

Modes define how input material is used and how the selected style is presented.

Style presets must not redefine these rules.

# Input Modes

## `source-photo`

Use an uploaded image as the primary reference.

Preserve defining identity, structure, pose, spatial relationships, materials, and atmosphere according to the active preservation settings.

Do not stretch or distort the main subject to fit the canvas.

Natural environmental extension is allowed when reframing is necessary.

## `theme`

Use a written subject, place, concept, address, coordinates, or narrative as the primary input.

Build a coherent interpretation from the supplied information.

When real-world accuracy matters, do not invent precise location-specific details.

## `hybrid`

Use both an uploaded image and written context.

The image controls visible subject identity unless the user specifies otherwise.

Written context may control narrative, place, time, mood, or transformation emphasis.

# Output Modes

## `generated-only`

Create only the transformed result.

When a source image is present:

- use it as visual reference;
- do not display the original photograph as a separate panel;
- adapt the selected preset to the full canvas.

Do not inherit split-layout instructions from the historical source prompt.

Default aspect ratio:

```text
3:4
```

## `compare-split`

Create a vertical comparison composition divided into two equal sections.

```text
Aspect ratio: 3:4
Upper section: exactly 50%
Lower section: exactly 50%
```

With `source-photo` or `hybrid` input:

- the upper section preserves the source photograph;
- apply only restrained editorial color refinement;
- natural environmental extension is allowed when required;
- the lower section applies the selected style.

With `theme` input:

- the upper section presents a coherent realistic interpretation of the theme;
- the lower section translates that scene into the selected style.

The two sections should remain visually related through subject, structure, pose, color, symbols, or spatial relationships.

## `retouch-only`

Preserve the photograph without illustration or conceptual reinterpretation.

Apply restrained editorial or fine-art photographic refinement.

Preserve subject identity, pose, structure, materials, and environment.

Natural environmental extension is allowed when necessary.

Avoid aggressive reconstruction or beauty retouching unless explicitly requested.

# Independent Variations

When `VARIATION_MODE = independent`:

- every result must remain separate;
- never combine variations into a collage by default;
- variations may use different presets or different overrides;
- if no output mode is specified, use `generated-only`.
