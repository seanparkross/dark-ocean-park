# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Oceanic Park is a VS Code/Cursor color theme extension. It's an oceanic-inspired dark theme with blue and aquamarine tones.

## Project Structure

- `themes/Oceanic Park-color-theme.json` - The main theme definition file containing all color configurations
- `package.json` - Extension manifest with metadata, keywords, and theme contribution points
- `demo_files/` - Sample files in various languages for testing theme appearance
- `ocean-icon.png` - Extension marketplace icon

## Development Commands

```bash
# Package the extension into a .vsix file
vsce package

# Publish to VS Code Marketplace
vsce publish
```

## Theme Development

The theme is defined in `themes/Oceanic Park-color-theme.json` with:
- `semanticTokenColors` - Semantic highlighting rules
- `tokenColors` - TextMate scope-based syntax highlighting
- `colors` - UI/workbench colors

To test changes: Press F5 in VS Code to launch Extension Development Host, or reload the window after modifying the theme file.

## Key Colors

- Background: `#17242b`
- Primary blue: `#61afef`
- Aquamarine/cyan: `#56b6c2`
- Purple: `#c678dd`
- Orange: `#d19a66`
- Red: `#e06c75`
- Yellow: `#e5c07b`
