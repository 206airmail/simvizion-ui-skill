# Typography, spacing, geometry — canonical foundation (v1.2)

## Typography

Use **Segoe UI Variable**, falling back to **Segoe UI**, then a platform system sans-serif. Use **Consolas** (then monospace) for code, log entries, and technical values where fixed-width glyphs help; do not use monospace throughout ordinary forms. Set letter spacing to 0 by default and a normal line-height of **1.3**. Regular text uses proportional numerals; aligned numeric data, counters, financial values, and timestamps use tabular numerals.

| Role | Size | Weight | Default color and use |
|---|---:|---:|---|
| Application / page heading | 20px | 600 | Near-white; not repeated on every panel |
| Dialog / major section heading | 16px | 600 | Near-white |
| Internal subsection heading | 14px | 600 | Near-white by default; not automatically teal |
| Integrated panel identification/title | 14px | 500–600 | Muted neutral or near-white according to hierarchy |
| Body, field value, label, button | 13px | 400–500 | Primary or secondary neutral by role |
| Tooltip / supporting description | 12px | 400 | Readable neutral; not unnecessarily faded |
| Secondary metadata / compact chip | 11px | 400–500 | Muted neutral; never substitute for essential form labels |
| Technical inline code | 12px | 400 | Monospace on recessed surface |
| Major KPI (normal / compact / featured) | 28 / 24 / 32px | 600 | Tabular numerals, data semantics from `colors.md` |

Titles signal structure using size and weight before color. Compact uppercase panel identifiers are allowed; ordinary headings, descriptions, and labels use natural capitalization. Reserve cyan for active context or intentionally meaningful technical information, not every heading. Preserve at least 13px ordinary control text in compact density. Avoid all-bold interfaces. Don't shrink text to rescue crowded layouts; reorganize the layout instead. Text/background combinations must satisfy applicable accessibility criteria.

## Spacing scale and relationships

Canonical scale: **2, 4, 6, 8, 12, 16, 20, 24, 32px**. Base rhythm is 4px with 2px optical refinements. Prefer these tokens to ad hoc gaps, but select them by relationship—not by blindly applying the same gap everywhere.

| Relationship | Default | Approved context |
|---|---:|---|
| Desktop window outer inset | 6px | Web page gutters follow `web-layouts.md` |
| Separate workspace panels | 6px | Connected panels may share a boundary |
| Standard panel padding | 12px | 8px dense inspector, 16px spacious content |
| Between neighboring controls | 6px | 4px within tightly integrated toolbar groups |
| Internal subsection spacing | 12px | Use a divider only for meaningful transition |
| Label-to-input vertical gap | 4px | Horizontal label-to-field gap normally 8px |
| Tooltip/icon-to-text gap | 6–8px | Contextual, consistent per group |

Group related controls tightly; separate sections through space and near-white subgroup headings first, and use **contextual subtle 1px dividers** when they clarify a genuine boundary. Avoid redundant borders and whitespace. Keep grid alignment and control size consistent within a functional group.

## Control density and geometry

**32px** is the standard input/button height for ordinary forms, settings dialogs, and main actions. **28px** is the approved compact height for dense inspectors, repeated table controls, and toolbars. Match heights within a combined control row; keep 13px field text. At narrow widths adapt field layout before sacrificing legibility.

Controls use a **4px** radius; panels and popovers **6px**; modal dialogs **8px**. Crisp **1px** control borders use the standard `--sv-border` token; focused and selected states use the canonical semantic tokens. Ordinary panel structure is surface-led with selective borders. Floating elements use `0 2px 8px rgba(0,0,0,0.40)` without oversized shadows or glows.

## Form label placement

For dense property inspectors, use **left-aligned labels beside fields** with a consistent label column within each group. The previous 35–40% / 80–140px guidance is only a *starting point*, not a universal constraint. Adapt width to actual label lengths and panel dimensions.

For standard forms, preferences and descriptive settings, **labels above fields** are the default. Stack horizontal rows when space is constrained or labels become unreadable. Do not mix patterns arbitrarily within the same related group; allow long labels to wrap and technical field values to remain accessible.

## Text overflow

Ordinary descriptions wrap naturally. Compact filenames/identifiers may truncate, with full-value access. Prefer middle truncation for paths where both the root and filename matter; preserve the complete value for copying/editing. Numeric values should not be silently truncated. Logs/code preserve exact formatting, with horizontal scrolling when needed. See tables and controls references for component-specific handling.
