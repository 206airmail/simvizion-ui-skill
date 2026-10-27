# Public websites and responsive web pages

SimVizion is **desktop-first and adaptable to web**. Its canonical visual identity may also be applied to public websites, dashboards, and mobile browsers without imposing desktop shells or interaction patterns. **Choose layout by medium**:

- **Desktop application shell**: use the existing 6px outer margins, fixed panel headers where the pane scrolls independently, optional persistent toolbars and status bars. Never force this shell onto a public website.
- **Public website**: document/body normally scrolls as a whole. Headers may be sticky if needed, but avoid fixed-height viewport panels, nested scrolling, and persistent bottom status bars by default. Use semantic landmarks (`header`, `nav`, `main`, `footer`).
- **Admin/dashboard website**: use a bounded content region for forms and editorial content even on large screens; dashboards, maps, and broad data grids may be wider where needed. A 1400px-wide input is usually a layout failure, not a feature.

## Web sizing defaults (contextual recommendations)

| Region | Recommended limit | Rationale |
|---|---|---|
| General page content | `max-width: 1120px` | Keeps web layout readable on large displays |
| Forms/settings content | `max-width: 760px` | Avoids stretched fields and labels |
| Long-form reading | `max-width: 720px` | Comfortable line lengths |
| Full data canvas | wider/full width only when justified | Dense tables, maps, charts |

Use responsive `width: min(100% - 24px, var(--sv-page-max))` or a comparable container; preserve the compact 4px spacing scale within components. Web **page gutters** may be larger than desktop application's 6px window inset: 12px on small screens, 16–24px tablet/desktop as available. This is a medium-specific difference, not a new desktop padding rule. Use container queries or measured content widths rather than arbitrary device assumptions.

## Phone and touch behavior

- On narrow phone screens, stack columns and form labels; use full-width form controls where appropriate but never exceed the constrained form container on large screens.
- Navigation may move to a drawer; tables can scroll horizontally with visible discoverability, collapse unimportant columns, or use cards only where the data shape allows. Keep labels and data associations clear.
- Touch targets should aim for **at least 40×40px** on public/mobile web even though visual controls remain 28/32px; increase hit target via surrounding padding/pseudo-elements without artificially making desktop interfaces huge. Do not place dangerous controls so close together that they are easy to mis-tap.
- Body scrolling is default for public pages. Avoid `height:100vh; overflow:hidden` on mobile public pages unless building a deliberately app-like tool. Account for soft keyboard, safe-area insets, zoom, and text reflow.
- Support focus indicators and actual links: keyboard-visible focus, descriptive labels, valid contrast, link semantics. Do not treat hover as the only affordance.

## Application web views

Browser-based desktop tools may intentionally use independent scrolling panes and fixed toolbars; use the desktop shell rules in that case. The decision is based on interaction model, not on whether the implementation uses web technologies.

## Wide data tables on small screens

When a table is wider than the viewport, users must be able to discover the hidden columns before attempting to scroll. Prefer a subtle fading right edge and/or a visible partial next column with a brief accessible sideways-scroll hint; update the cue as the horizontal scroll reaches either edge. Avoid an overlay that covers values or blocks gestures. A sticky first identifier column is optional if it leaves useful room. Document/page scrolling remains primary, with intentional horizontal scroll on the table only. A page-sticky column header may become incompatible with horizontal table scrolling: preserve horizontal alignment and usable scrolling, and allow the header to scroll normally where necessary. Do not prescribe fixed device-width breakpoints.
