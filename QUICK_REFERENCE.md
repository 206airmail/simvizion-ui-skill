# SimVizion quick reference (v1.4)

> Summary only. `SKILL.md` and the canonical `references/*.md` are authoritative; resolve discrepancies against them. Family resemblance, not uniformity.

# SimVizion UI — Quick Reference (v1.4)

## Essential colors
| Token | Hex | Purpose |
|---|---|---|
| `--sv-window` | `#050C0E` | Window canvas |
| `--sv-panel` | `#0D1B1F` | Main panels |
| `--sv-surface-content-raised` | `#101F23` | Optional unified content-rich cards |
| `--sv-elevated` | `#14272B` | Elevated regions, popovers, toolbars; headers when warranted |
| `--sv-recessed` | `#071215` | Inputs, code areas, recessed content |
| `--sv-border` | `#294147` | 1px borders and dividers |
| `--sv-text` | `#EDF4F5` | Primary near-white text |
| `--sv-text-readable-secondary` | `#C5D4D6` | Readable descriptions/supporting content |
| `--sv-text-secondary` | `#A6B8BC` | Secondary labels/body |
| `--sv-text-muted` | `#91A6AB` | Metadata/placeholders |
| `--sv-lime` | `#9AF000` | Primary CTA, checked/on-state |
| `--sv-teal` | `#42CDD2` | Info, focus, selected icons |
| `--sv-selected-bg` | `#194047` | Selected surface |
| `--sv-selected-border` | `#42C4CB` | Active navigation / connected tab border |
| `--sv-hover-bg` | `#1B3237` | Hovered surface |
| `--sv-hover-border` | `#41858D` | Hover outline |
| `--sv-warning` | `#F0B84B` | Warning |
| `--sv-error` | `#F07171` | Error indicator
| `--sv-status-success` | `#A7D5A0` | Success status, separate from favorable KPI role |

## Geometry / typography
- Font: Segoe UI Variable → Segoe UI; Consolas for code/logs/IDs.
- Body: **13px/400, line-height 1.3**; page 20/600; section 16/600; group 14/500; metadata 11/400; near-white headings, secondary-gray supporting text. Tabular numerals in numeric UI.
- Space rhythm: **2, 4, 6, 8, 12, 16, 20, 24, 32px**. Window edge **6px**; panel gaps **6px**; panel padding **12px** (compact 8, spacious 16); section gaps **12px**; form control gaps **6px**.
- Border: 1px. Radius: controls **4px**, panels **6px**, modal **8px**. Shadow for floating UI: `0 2px 8px rgba(0,0,0,.40)`.
- Button/input heights: **32px standard**, **28px compact**. Icon-only controls are always bordered. Icons 16px default, 14 compact, 20 prominent; rounded outline, 1.75px stroke.

## Core shared states
- Primary: lime surface, dark text; hover `#ADFF24`; pressed `#7DC900`.
- Focus: 1px teal border on dark controls, **no glow**; on lime-filled controls also use a contrasting 2px inner dark ring. Selected: background-led teal; strong border on active navigation and connected tabs, not on table rows.
- Secondary button: recessed; hover `#1B3237` / `#41858D`.
- Disabled: `#101A1D` bg, `#223338` border, `#789096` text; no hover.
- Destructive: muted red outline `#24191C` + red border/text, filled red for high-impact confirmation.
- Hover/selection transitions typically 100ms; user-triggered drawers/accordions ~150ms; tab **content switches instantly**. Reduced motion makes transitions instant.

## Window and navigation defaults
- Adaptive shell: single workspace, sidebar, or multi-panel based on purpose. Resizable detail/workspace panels where useful; handles visually subtle, teal on hover/drag.
- Header in independent scrolling panel remains fixed; content scrolls, optional persistent footer fixed.
- Panel header: **32px** default (28/36 alternatives), integrated by default; elevated only for functional header separation. Actions on right. Panel footer: integrated for short content, fixed elevated for scrolling content; Cancel then primary on right.
- Navigation sidebar: **180px expanded**, **48px icon-only**, optionally collapsible, saved user preference; navigation item **32px**, full teal selected outline. Toggle in sidebar header. Responsive: expanded → icon-only → menu/drawer.
- Drawer: 240px default (220–280), 30% black backdrop, 150ms user-triggered slide/fade; auto responsive changes instant.
- Main toolbar: **40px** (36/44), identity left, contextual project optional, actions right; separate or connected surface. Distinct action groups may use subtle dividers when useful. Icon-only utilities; primary actions can carry text. Secondary groups overflow to ellipsis menu.
- Status bar: **28px** (24/32), left primary status, right independent indicators. Simple states dots, warnings/errors semantic icons. Optional, contextual separate/connected surface.

## Tabs and data
- Tabs: connected with a defined active cyan border; **32px** default (28/36). Horizontal default, contextual vertical tabs **140px** width (120–180). Instant content switching. Horizontal dynamic tabs scroll; small fixed tab groups overflow into menu.
- Table rows: **36px** standard / **28px** dense; fixed column headers; selected rows use a teal background without mandatory full outline; uniform rows by default; zebra striping/dividers optional for dense grids. Text left, numeric right/tabular, compact icons center.
- Table toolbars: Search+Filter grouped left, utilities right, contextual overflow/reflow; title/count only when useful. Pagination compact previous/next and attached footer when needed.
- Notifications: elevated toasts top-right, 16px inset, max 360px wide, 12px padding, radius 6px, icon 20px; status uses semantic color but messages remain near-white/gray. History panels optional.

## Never turn appearance guidance into app functionality
This skill does **not** mandate storage (JSON/SQLite), recovery journals, notification retention, retry intervals, file-saving strategies, or specific screens, features, and workflows.

## Web, extended components, and financial data (extended guidance)
- **Public website:** document/body scrolling by default, **not** a fixed desktop window; bounded content **1120px max** general, **760px forms**, **720px reading**; responsive gutters and touch hit targets ~40px while visual controls remain compact. See `references/web-layouts.md`.
- **Pills:** 20px standard / 18px compact, 4px radius, 11px/500, 6px horizontal inset; neutral by default, semantic tints only if meaningful.
- **Tab count chips:** 18px height/min width, rounded, 11px/500; avoid extra bright teal inside selected tab.
- **Persistent banners:** 20px semantic icon, 12px padding, 6px radius, subdued status tint, 13px/600 title.
- **Segmented toggles:** 28px compact / 32px standard, selected uses **teal** (`--sv-selected-bg`/`--sv-selected-border`), not lime.
- **Inline links:** restrained `--sv-link: #86CDD0`, hover `#B2E5E6`, underline hover/focus; underline by default in prose if clarity requires.
- **Financial data (approved):** positive/ordinary numbers stay near-white `--sv-text`, losses use subdued red `--sv-value-negative: #E8A0A0`, featured favorable KPIs and meaningful favorable statistics may use restrained `--sv-value-positive: #A7D5A0` in sparse cards; dense tables may use subdued green on **one intentionally designated primary favorable metric column**, plus sparse meaningful exceptional values. Neither positive sign nor sort state alone triggers green; bright lime is permitted for featured headline KPI roles, not routine numeric data.
- **Headline KPIs:** 28px/600 typical (24px compact, 32px featured), near-white default, subdued positive green for a favorable featured value, or bright lime for a semantically featured headline metric, tabular digits.
- **Expandable table rows:** expansion is **not selection**. Recessed breakdown below row; keep background-led selection only if selected.
- **Scrollbar:** 6px **visual** width globally (prior standard); optional larger pointer hit target.
- **Toolbar controls:** 28px compact default, 32px if appropriate. Right-aligned numeric header sort arrow may precede label inside a right-aligned heading group to preserve numeric alignment.
- **Inline code:** Consolas 12px, recessed surface, small 4px radius, 2px H/1px V inset.
- Text semantics: **secondary** for meaningful labels/explanations; **muted** for metadata, timestamps and placeholders; disabled separate.
- All CSS token names must match `examples/tokens.css`: **use `--sv-lime`**, with `--sv-primary` only as a documented backward-compatible alias.

- **Approved data-accent balance B:** Featured favorable KPI figures and genuinely meaningful favorable statistics in sparse cards may be subdued green, while dense tables may feature one primary favorable metric column in subdued green and a few exceptional statistics; other normal positive figures remain near-white. No blanket green-per-positive-value rule. Equal peer cards may each feature a bright-lime headline number if each has the same featured role. Win-rate thresholds are app-defined, not global.
- **Mobile wide-table cue:** edge fade/partial next-column indication + accessible horizontal-scroll hint; preserve scrolling even if a page-level sticky header must become nonsticky. Repeated destructive row actions are secondary on pointer hover/focus but reachable on touch/keyboard.

- **Approved dense-table hierarchy B:** A single *purposefully featured favorable metric* column (e.g. Profit/hr) may use `--sv-value-positive` with semibold figures; all other routine positive columns stay near-white. Sorting a different column must not automatically move green. Extra green accents must be rare and meaningfully exceptional; never use bright lime for table data.

## v1.3 visual-impact guidance
- **Purpose-driven hierarchy:** Equal peer categories remain equally prominent; use hierarchy *inside* each card rather than promoting one arbitrarily.
- **Content type:** Dense controls/tables retain 13px type; dashboards may use 14–15px descriptive text, 16px card headings, and 28–36px featured KPI figures.
- **Surface:** `--sv-surface-content-raised` is an optional unified content-card treatment, not a mandatory nested background strip.
- **Density:** Dense regions 8–12px panel padding, standard 12px, content cards ~16px when beneficial.
- **Quality:** Review full-screen hierarchy, readable secondary content, purposeful emphasis, available-space utilization, font rendering and scale.

## v1.4 family identity and composition

Use `references/identity-composition.md` as the canonical guide. Open the actual reference images. Preserve family color roles, clear typography, control styling and coherent depth while choosing navigation, layout and density for the application. Branding gradients, artwork lighting and selective primary-action illumination are optional role-specific treatments, never replacements for focus or selection. Give content appropriate scale; keep tables compact. Review and correct whole-screen weaknesses separately from functional verification. See `examples/composition-review.md` for a written dashboard comparison, not a rendered template.
