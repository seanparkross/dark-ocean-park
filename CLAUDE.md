# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Dark Ocean Park is a dual-platform color theme project providing oceanic-inspired dark themes for VS Code/Cursor and Zed editors.

## Repository Structure

```
dark-ocean-park/
├── vscode/          # VS Code/Cursor extension (has its own CLAUDE.md)
│   ├── themes/      # Theme JSON file
│   └── demo_files/  # 25+ language test files
└── zed/             # Zed editor theme
    └── dark-ocean-park.json
```

## Development Commands

```bash
# VS Code extension packaging (run from vscode/ directory)
cd vscode && vsce package

# VS Code extension publishing
cd vscode && vsce publish
```

## Architecture

**Two independent theme implementations sharing a common color palette:**

1. **VS Code** (`vscode/`): TextMate token scopes + semantic highlighting + workbench UI colors. Packaged as `.vsix` for Marketplace and manual Cursor installation.

2. **Zed** (`zed/`): Native Zed theme schema (v0.2.0) with UI elements, terminal ANSI colors, and collaborative editing cursor colors.

## Testing Workflow

- VS Code: Press F5 to launch Extension Development Host, test against files in `demo_files/`
- Zed: Install theme locally and reload editor

## Shared Color Palette

| Color | VS Code | Zed |
|-------|---------|-----|
| Background | `#17242b` | `#1b2b34` |
| Blue | `#61afef` | `#5a9bcf` |
| Cyan | `#56b6c2` | `#5fb3b3` |
| Purple | `#c678dd` | `#c5a5c5` |

When modifying colors, consider updating both themes to maintain visual consistency.
