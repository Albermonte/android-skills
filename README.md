# Android Skills

Material 3 Expressive design reference system for Android UI/UX.

## Overview

This repository provides AI agent skills and design references for **Material 3 Expressive (M3E)** — Google's expressive design language for Android. It contains comprehensive token specifications, component guidelines, and implementation examples for building emotionally resonant Android interfaces.

### What This Repository Provides

- **65 reference files** covering M3E components, tokens, and foundation systems
- **Component specifications** with design tokens for buttons, dialogs, sheets, navigation, and more
- **Foundation tokens** for color, typography, shape, motion, and elevation
- **Wear OS support** with dedicated expressive design guidance
- **Jetpack Compose examples** demonstrating expressive patterns
- **Automated weekly updates** from the official Material Design documentation

### When to Use

- Designing or reviewing Android UI with Material 3 Expressive
- Looking up component tokens (e.g., `md.comp.button.*`)
- Implementing expressive hierarchy, motion, color, or shape
- Building for phones, tablets, foldables, or Wear OS

### When NOT to Use

- Non-Android platforms (iOS, web, desktop)
- Non-UI Android tasks (networking, data layer)
- Implementation-only requests without design decisions

## Quick Start

1. **Load the skill** — The main entry point is `skills/material-3-expressive/SKILL.md`
2. **Check the index** — Start with `references/m3-expressive-specs-tokens-index.md` for token lookups
3. **Use the output template** — Follow `references/m3-component-token-output-template.md` for consistent guidance

### Basic Workflow

1. Confirm intensity level (Foundational, Excellent, or Transformative) and hero moments
2. Confirm device class and window size class
3. Load Tier 1 index and output template
4. Load component overview + token spec files as needed
5. For theming, load Tier 3 foundation tokens

## Project Structure

```
android-skills/
├── skills/material-3-expressive/
│   ├── SKILL.md                    # Main documentation and workflow
│   ├── agents/                     # AI agent configurations
│   │   └── openai.yaml
│   ├── assets/examples/
│   │   ├── ui/                     # Jetpack Compose examples
│   │   │   ├── ExpressiveHomeScreen.kt
│   │   │   ├── ExpressiveButtonComparison.kt
│   │   │   └── ExpressiveAntiPatterns.kt
│   │   └── ux/                     # UX templates
│   │       └── expressive-ux-brief-template.md
│   ├── references/                 # 65 M3E reference files
│   │   ├── m3-*-specs-tokens.md    # Component token specifications
│   │   ├── m3-*-foundation-tokens.md  # Foundation tokens
│   │   ├── m3-*.md                 # Component overviews
│   │   ├── wear-*.md               # Wear OS guidance
│   │   └── ...
│   └── scripts/
│       └── update_m3_expressive_refs.py  # Automated update script
└── .github/workflows/
    └── update-m3-expressive.yml    # Weekly CI/CD automation
```

## Reference Tiers

References are organized by loading priority:

### Tier 1: Index & Templates (Always Load First)
- Component token lookup index
- Output format template
- New/updated components list

### Tier 2: Component Specs & Tokens (43 files)
Component overviews and token specifications for:
- Buttons, Button Groups, Split Button
- FABs, Extended FAB, FAB Menu, Icon Buttons
- Dialogs, Bottom Sheets, Side Sheets
- Navigation Bar, Navigation Rail, App Bars, Toolbars
- Carousel, Progress Indicators, Loading Indicator

### Tier 3: Foundation Tokens
- Color system and color tokens
- Typography, fonts, and type scale
- Shape, corner radius scale, and shape morph
- Motion physics and motion tokens
- Elevation and state tokens

### Tier 4: Research & Evidence
- Expressive research findings
- Testing guidance
- Design articles and guidelines

### Tier 5: Wear OS Specific
- Expressive benefits for wearables
- Levels of expression
- Wear Compose Material3 guidance

## Automation

References are automatically updated weekly via GitHub Actions.

### Schedule
- **When**: Every Monday at 9:00 AM UTC
- **Branch**: `codex/m3-expressive-refresh`
- **Action**: Creates a PR with refreshed references

### Manual Update

```bash
# Install dependencies
python -m pip install playwright
python -m playwright install chromium

# Run update script
python skills/material-3-expressive/scripts/update_m3_expressive_refs.py
```

## Technologies

- **Python 3.11+** — Update script runtime
- **Playwright** — Web scraping for reference updates
- **Jetpack Compose** — Example implementations
- **Material 3** — Design system foundation
- **GitHub Actions** — CI/CD automation

## Search Tips

Find specific tokens using grep:

```bash
# Find button tokens
rg "md.comp.button" skills/material-3-expressive/references/m3-buttons-specs-tokens.md

# Find navigation tokens
rg "md.comp.navigation" skills/material-3-expressive/references/m3-.*navigation.*.md
```

## License

See individual reference files for source attribution. Component specifications and design tokens are derived from [Material Design](https://m3.material.io/).
