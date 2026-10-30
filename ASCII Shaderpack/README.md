# ASCII Shaderpack

Turn Minecraft into living ASCII art.

This shader pack builds the final frame from text characters: the world, HUD and UI are all rendered as ASCII characters directly in the final pass.

## What is inside

- ASCII rendering in `final.fsh`
- A built-in procedural monospace bitmap font (no external textures, no texture binding issues)
- A lot of settings: density, character set, color, background, brightness, contrast, inversion and scanlines

## Requirements

- Minecraft with shader support
- OptiFine or Iris
- A normal final-pass setup; this pack does not rely on heavy shadows

## Installation

1. Copy the `ASCII Shaderpack` folder or `ASCII Shaderpack.zip` into:
   `.minecraft/shaderpacks`
2. Open `Options -> Video Settings -> Shaders`
3. Select `ASCII Shaderpack`
4. Click `Shader Options...` if needed

## Settings

### Symbols

| Setting | Values | What it does |
|---|---|---|
| Symbol size | Very small / Small / Normal / Large / Very large | Changes cell size. Smaller cells mean denser ASCII. |
| Character set | All printable, Classic 10, Blocks, All letters, etc. | Changes which characters form the image. |

### Color

| Setting | Values | What it does |
|---|---|---|
| Glyph color | Source, Monochrome, Matrix, Amber, Cyan, Inverted, Sepia | Changes how the glyphs look. |
| Background | Black, Dark source, Source | How dark the empty space stays. |
| Brightness | 0.5 - 2.0 | Lifts or lowers the image. |
| Contrast | 0.5 - 2.0 | Strengthens or softens details. |

### Effects

| Setting | Values | What it does |
|---|---|---|
| Invert colors | On / Off | Swaps foreground and background. |
| Scanlines | On / Off | Adds a light CRT-style line pattern. |

## Quick presets

- **Readable ASCII:** normal size, source color, black background.
- **Matrix:** larger size, matrix green, black background and scanlines.
- **Monochrome:** monochrome glyphs and dark background. Looks like an old terminal.
- **Cinema:** amber or sepia with moderate contrast.

## Tips

- If the image looks too messy, raise contrast and use a larger symbol size.
- If characters blur together, use the classic 10-character set.
- Keeping source color makes the result look more like a game.
- ASCII is applied to UI and HUD too, so very small sizes can hurt readability.
- If settings do not appear, refresh the pack and check that `shaders/shaders.properties` exists.

## Troubleshooting

- **No settings in menu:** make sure you open `Shader Options...`, not the general OptiFine settings.
- **Weird characters in labels:** localization depends on game language and shader loader. Removing `shaders/lang/ru_RU.lang` leaves clean English labels.
- **Image too dark:** raise brightness / contrast or disable inversion.
- **Too dense:** choose a larger symbol size.

## Credits

- Made for OptiFine / Iris
- Final rendering pass: `final.fsh`
- Font: procedural mono bitmap font inside GLSL
- Pack name: `ASCII Shaderpack`
