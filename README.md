# Android Skills

Material 3 Expressive (M3E) skills and design references for Android UI/UX.

## Installation

```bash
npx skills add Albermonte/android-skills
```

Learn more at [skills.sh](https://skills.sh/).

## Overview

This repository packages an Agent Skills bundle for M3 Expressive. It includes component token specs, foundation tokens, and Compose examples to help design expressive Android interfaces.

What's included:
- 65 reference files covering M3E components and foundation systems
- Component token specifications for buttons, dialogs, sheets, navigation, and more
- Foundation tokens for color, typography, shape, motion, elevation
- Wear OS guidance and expressive patterns
- Jetpack Compose examples

When to use:
- Designing or reviewing Android UI with Material 3 Expressive
- Looking up component tokens (e.g. `md.comp.button.*`)
- Choosing expressive hierarchy, motion, color, or shape

When not to use:
- Non-Android platforms
- Non-UI Android tasks
- Implementation-only requests without design decisions

## Skills

| Skill | Description |
| ---- | ---- |
| **material-3-expressive** | Material 3 Expressive design reference system for Android UI/UX |

## Quick Start

1. Load the skill: `skills/material-3-expressive/SKILL.md`
2. Start with the index: `skills/material-3-expressive/references/m3-expressive-specs-tokens-index.md`
3. Use the output template: `skills/material-3-expressive/references/m3-component-token-output-template.md`

## Structure

```
android-skills/
├── skills/
│   └── material-3-expressive/
│       ├── SKILL.md
│       ├── assets/
│       │   └── examples/
│       │       ├── ui/
│       │       └── ux/
│       ├── references/
│       └── scripts/
└── .github/
    └── workflows/
```

## Automation

References are updated weekly via GitHub Actions.

Schedule:
- Monday at 9:00 AM UTC
- Branch: `codex/m3-expressive-refresh`

Manual update:

```bash
python -m pip install playwright
python -m playwright install chromium
python skills/material-3-expressive/scripts/update_m3_expressive_refs.py
```

## Resources

- [Material Design](https://m3.material.io/)
- [Agent Skills Spec](https://agentskills.io)

## License

See individual reference files for source attribution. Component specifications and design tokens are derived from Material Design.
