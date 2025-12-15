# Changelog

All notable changes to this plugin are documented in this file.

The format follows Keep a Changelog and adheres to Moodle plugin conventions.

---

## [1.0 - Accessibility Edition] - 2025-03-13

### Added
- WCAG AA (4.5:1) contrast enforcement for text and background colors
- Dynamic filtering of available colors based on current selection
- Accessibility-focused extensions to the Tiny Font Color plugin
- Configurable preset color palettes via admin settings
- Optional free-form color pickers for text and background colors
- Multilanguage support for color names
- JSON-based color scheme configuration (`colorscheme.json`) as an alternative setup method

### Changed
- Extended standard Tiny color behavior to prevent inaccessible color combinations
- Improved validation of color values (hex color format only)

### Security
- Replaced direct superglobal access with Moodle parameter handling APIs
- Input validation aligned with Moodle security guidelines

---

## [0.8] - 2024-10-09

### Base Version
- Stable release of **Tiny Font Color** plugin (`tiny_fontcolor`)
- Admin-configurable text and background color palettes
- Optional color pickers for text and background colors
- Moodle Tiny editor integration
- Supported Moodle versions: 4.1 – 4.5
