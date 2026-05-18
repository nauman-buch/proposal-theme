# BIH-HIS Design System Proposal

A self-contained, interactive HTML proposal for the BIH-HIS application's design system. Open `DESIGN_SYSTEM_PROPOSAL.html` in any modern browser. No build step, no server, no dependencies beyond a network connection for Google Fonts.

## What's inside

1. **Color roles** — semantic colors with hex codes (Background, Card, Foreground, Muted, Border, Focus ring) plus the 4 status colors (Success / Warning / Danger / Info) with both solid and soft variants.
2. **Theme palettes** — 6 selectable themes (Default, Corporate, Emerald, Elegant, Sapphire, Sunset) each showing light & dark backgrounds and primary colors.
3. **Spacing & sizing** — per-component specs (Page, Card, Modal, Button, Input, Form, Table, Status box) with exact pixel values.
4. **Typography** — 5 text roles (Title, Heading, Label, Body, Caption) with size, weight, and line height.
5. **Components preview** — live, interactive samples of Buttons, Inputs, and Selects that re-tint to whichever theme is selected.

## Features

- **Theme picker** at the top of the page — click any of the 6 theme buttons to instantly re-tint every color, button, input border, and selected-option highlight across the entire document. Selection persists across page reloads via localStorage.
- **Hover tooltip** — hover any element to see its computed styles:
  - Hover a button → padding, border-radius, border, size, font-size, font-weight
  - Hover an input → padding, border-radius, border, height, font-size
  - Hover a select trigger / chip / menu option → trigger / option styling
  - Hover text → font-size, line-height, font-weight
  - Hover a card → full box-model + typography stats
- **Mobile responsive** — tables stack into card layouts on phones; theme picker becomes horizontally scrollable.
- **Print friendly** — `@media print` hides the theme picker so the page prints cleanly.

## Interactive components

- **Buttons** — all 6 variants (default, outline, secondary, ghost, destructive, link), 4 sizes (xs, sm, default, lg), and 6 states (normal, hover, loading, disabled, with-left-icon, with-right-icon). Hover lift and active shrink work on real mouse interaction.
- **Inputs** — 9 working examples including search, calendar, password (with toggle), prefix `$` / suffix `kg`, error state, disabled, and helper text. Focus ring auto-tints to the active theme's primary.
- **Selects** — both single-select with check-icon and multi-select with removable chip + overflow counter. Click to open, click outside or Esc to close.

## Tech notes

- Single file, ~80 KB, no external JS/CSS dependencies except Google Fonts (Inter + JetBrains Mono).
- All theming via CSS custom properties on `:root[data-theme=<name>]`.
- All interactivity via vanilla JS in isolated IIFEs (no React, no Vue, no framework).
- Inline `<div>` color swatches — no third-party image services.

## Use

Open in browser:
- Double-click the file
- Or drag it onto any browser tab
- Or `start DESIGN_SYSTEM_PROPOSAL.html` from a terminal in this folder
