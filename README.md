# Design System Generator — Claude Code Skill

### Generate design.md, design-guidelines.md, and design-components.md from any design references

**[🇨🇳 中文](README.zh-CN.md)** | **🇺🇸 English**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/Skill-blue?style=flat-square" alt="Skill">
  <img src="https://img.shields.io/github/license/albertzhangz10/design-system-skill?style=flat-square&color=green" alt="MIT License">
  <img src="https://img.shields.io/github/stars/albertzhangz10/design-system-skill?style=flat-square" alt="GitHub Stars">
</p>

> Stop manually documenting your design system. Upload any design reference and get 3 production-ready markdown files that AI coding tools (Cursor, Claude Code, Copilot) understand natively.

**[Or use the web version — no setup required](https://figmadesignmd.com/)**

A Claude Code skill that generates comprehensive design system documentation from any reference materials — images, PDFs, links, screenshots, brand guidelines, or existing code. Non-technical users (designers, PMs) can use the [web version](https://figmadesignmd.com/) directly.

## The Problem

Design systems live in Figma, brand PDFs, and scattered docs — but the documentation AI coding tools need lives nowhere. Every time you start a new project, you manually write token specs, component guidelines, and accessibility rules.

## The Solution

One command. Three documents. From any design reference.

```
/design-system
```

## What It Generates

| File | Contents | Auto |
|------|----------|:----:|
| **design.md** — colors, typography, shape, elevation, states, layout, motion | Token files, images, PDFs | ✅ |
| **design-guidelines.md** — accessibility, gestures, content design, do's & don'ts | References + inference | ✅ |
| **design-components.md** — 30+ components with variants, measurements, states | References + inference | ✅ |

## How It Works

```
Step 1  Provide any design references (images, PDFs, links, text, code)
Step 2  AI analyzes the design language across all materials
Step 3  Generate 3 structured markdown files
Step 4  Write files to your project directory
Step 5  Confirm with user before saving
```

### Accepted Inputs

| Type | Examples |
|------|----------|
| Images | Screenshots, mockups, design tool exports |
| PDFs | Brand guidelines, style guides, design specs |
| Links | Design system docs, component libraries, live websites |
| Text | Written descriptions of the design language |
| Code | CSS files, Tailwind configs, theme files, design tokens |

### Output Format

Each file:
- Starts with an H1 title and cross-references to the other 2 files
- Uses markdown tables for token values and component specs
- Includes specific measurements (dp/sp/px), hex colors, and CSS values
- Organizes do's/don'ts by category (Color, Shape, Elevation, Typography, etc.)
- Groups components by workflow (Actions, Input, Navigation, Containment, Feedback)

### Component Coverage

| Category | Components |
|----------|-----------|
| **Actions** | Button, Icon Button, FAB, Toolbar, Link |
| **Input** | Text Field, Checkbox, Radio, Switch, Slider, Dropdown, Combobox, Picker, Textarea |
| **Navigation** | Nav Bar/Rail/Drawer, Tabs, Breadcrumb, Menu, Search, App Bar |
| **Containment** | Card, Dialog, Bottom Sheet, Drawer, Popover, Accordion, Divider |
| **Data Display** | Avatar, Badge, List, Carousel, Icon, Image, Tag/Chip, Skeleton, Tooltip |
| **Feedback** | Progress Indicator, Spinner, Snackbar/Toast, Message Bar |

## Install

```bash
# Clone into your .claude/skills directory
git clone https://github.com/albertzhangz10/design-system-skill.git .claude/skills/design-system
```

Or copy the `SKILL.md` file into your project's `.claude/skills/design-system/` directory.

## Usage

```
/design-system                    # generates in current directory
/design-system ./docs/            # custom output path
```

Then provide your design references — drag & drop images, paste links, or describe the design language.

## Requirements

| Requirement | Required | Notes |
|-------------|:--------:|-------|
| Claude Code | ✅ | Latest version recommended |
| Design references | ✅ | Any combination of images, PDFs, links, text, or code |

## License

MIT License — see the [LICENSE](LICENSE) file for details.

## Credits

Built by [Albert Zhang](https://github.com/albertzhangz10).

Inspired by [Google Stitch design.md](https://stitch.withgoogle.com/docs/design-md/overview) — the `design.md` format and structure are based on their work.
