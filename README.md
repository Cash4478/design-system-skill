# Design System Generator — Claude Code Skill

A Claude Code skill that generates comprehensive design system documentation from any reference materials.

## What it does

Upload images, PDFs, links, or describe your design — this skill generates 3 production-ready markdown files:

| File | Contents |
|------|----------|
| `design.md` | Token reference: colors, typography, shape, elevation, states, layout, motion |
| `design-guidelines.md` | Accessibility requirements, gestures, content design, do's & don'ts |
| `design-components.md` | Full component specs organized by workflow category |

## Usage

```
/design-system
```

Then provide your design references:
- Screenshots or mockups (drag & drop images)
- PDF brand guidelines
- Links to design system docs or live websites
- Text descriptions of the design language
- Existing CSS/theme files

## Installation

Add this skill to your Claude Code project:

```bash
# Clone into your .claude/skills directory
git clone https://github.com/albertzhangz10/design-system-skill.git .claude/skills/design-system
```

Or copy the `SKILL.md` file into your project's `.claude/skills/design-system/` directory.

## Output Format

The generated files follow the same structure used by major design systems (Material Design 3, Apple iOS, Microsoft Fluent 2). Each file:

- Starts with an H1 title and cross-references to the other 2 files
- Uses markdown tables for token values and component specs
- Includes specific measurements (dp/sp/px), hex colors, and CSS values
- Organizes do's/don'ts by category (Color, Shape, Elevation, Typography, etc.)
- Groups components by workflow (Actions, Input, Navigation, Containment, Feedback)

## Examples

See the `/examples` directory for sample output generated from real design systems.

## License

MIT
