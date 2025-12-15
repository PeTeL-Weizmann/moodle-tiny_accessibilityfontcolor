# moodle-tiny_accessibilityfontcolor

A TinyMCE plugin for Moodle that provides text and background color controls
with built-in accessibility enforcement.  
The plugin dynamically filters available color combinations to ensure
WCAG AA contrast compliance (minimum 4.5:1).

---

## Accessibility Focus

- Enforces **WCAG AA contrast ratio (4.5:1)** for text and background colors
- Dynamically filters available colors based on the current selection
- Updates available options in real time during editing
- Prevents selection of inaccessible color combinations

---

## Key Features

- WCAG AA (4.5:1) contrast enforcement
- Dynamic filtering of foreground and background colors
- Configurable preset color palettes
- Optional free-form color pickers (disabled by default)
- Multilanguage color names (supports Moodle multilang tags)
- Integration with Tiny toolbar, format menu, and context menu
- Hex color validation (`#RRGGBB` only)
- Privacy compliant (implements null provider)

---

## Configuration

### Admin UI Configuration

The plugin can be configured via the Moodle administration interface:

**Site administration → Plugins → Text editors → Tiny editor → Accessibility font color**

Available settings:
- **Available text colors** – Named text colors with hex values
- **Available background colors** – Named background colors with hex values
- **Text color picker** – Enable or disable free-form text color selection
- **Background color picker** – Enable or disable free-form background color selection

If no colors are defined and the corresponding color picker is disabled,
the related toolbar button and menu entry will not be shown.

---

### JSON Color Scheme Configuration

As an alternative to the admin UI, color palettes can be defined using a
`colorscheme.json` file.

This approach is useful for:
- Initial setup
- Bulk definition of color palettes
- Version-controlled color schemes

The JSON configuration acts as a fallback and can be used alongside
the admin interface. If admin settings are defined, they take precedence.

---

## Installation

1. Copy the plugin into the following directory:  lib/editor/tiny/plugins/accessibilityfontcolor
2. Log in as a Moodle administrator
3. Go to **Site administration → Notifications** to complete the installation
4. Configure the plugin settings under:
**Site administration → Plugins → Text editors → Tiny editor**

### Requirements
- Moodle 4.1 or later
- Tiny editor enabled
- Not compatible with Atto

---

## Technical Notes

- Contrast calculation follows WCAG 2.1 relative luminance rules
- Contrast ratio formula: (L1 + 0.05) / (L2 + 0.05)
- Only 6-digit hex color values (`#RRGGBB`) are accepted
- Color filtering occurs dynamically as editor content changes
- Original color palettes are preserved internally to allow reset and re-filtering

---

## Privacy

This plugin does not store any personal data.  
It implements Moodle’s privacy null provider.

---

## License and Credits

This plugin is licensed under the GNU General Public License v3 or later.

### Original Work

This plugin is based on the **Tiny Font Color** plugin (`tiny_fontcolor`),
originally developed by:

- **Luca Bösch** (Bern University of Applied Sciences, BFH) – 2023  
- **Stephan Robotta** (Bern University of Applied Sciences, BFH) – 2023  

### Accessibility Extensions

Accessibility-focused extensions, including WCAG AA contrast enforcement,
dynamic color filtering, and administrative enhancements, were developed by:

- **Oshrat Luski** (PeTeL Project, Weizmann Institute of Science) – 2024  

### Maintenance

Current maintenance and public release are provided by the  
**PeTeL Project – Weizmann Institute of Science**.

