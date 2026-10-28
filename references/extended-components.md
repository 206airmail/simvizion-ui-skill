# Extended reusable UI components (v1.4)

These are **specialized recommendations**, harmonized with the already-approved SimVizion tokens. They are visual rules, not application feature mandates.

## Tags / pills / compact labels

- A *tag* identifies category or metadata (e.g. “Pharmacy”); a *status pill* communicates state (e.g. “No price” or “Unsellable”). Do not style all tags as prominent badges.
- Default pill: **20px minimum height**, **4px radius**, **11px/500** Segoe UI Variable, 6px horizontal padding, 1px quiet border, text centered. **18px compact variant** is allowed where density requires it; this preserves an approved compact option without making it the universal default.
- Neutral: elevated `--sv-elevated` background, quiet `--sv-border` border, secondary text. Status-specific: light semantic tint, subtle semantic border, near-white text by default; semantic icon optional at 12px. Lime fill reserved for primary/on states, not category labels.
- Keep pills text-readable, usually single line. Avoid saturated fills, gratuitous uppercasing, and using color as the only source of meaning.

## Tab count chips

- Optional compact count beside label, within existing tab height. Size **min-width 18px, height 18px**, horizontal inset 5px, radius 9px, **11px/500**, tabular numerals.
- Inactive tab: recessed/elevated neutral background + muted text. Active tab: selected-tint `--sv-selected-bg`, subtle selected outline or muted near-white count. Do **not** create a second bright teal focal point inside every selected tab.
- Count is supplementary; tab selection remains communicated by the tab itself. If count represents a warning/error, use semantic color only when it truly communicates severity; accessible name includes the count.

## Persistent alert banners

- For persistent, in-page warnings or information—not toasts—use **12px padding**, **6px radius**, 1px semantic-tinted border and subdued tinted background (consistent with established alpha-30 bg / alpha-CC border convention). **20px outline semantic icon** aligned to first text line on the left; **8px** icon-to-content gap.
- Title 13px/600 near-white, description 13px/400 secondary or near-white according to contrast, 4px separation. Optional actions at right or in a footer on narrow screens. Dismiss X only if dismissal is safe/allowed.
- Semantic classes: information teal; caution amber; error red; success subdued green (`--sv-status-success`). Do not color the whole paragraph brightly. Distinguish persistent banners from the top-right toast component.

## Segmented controls (e.g. 24h / 36h / 7d)

- Standard **28px compact** or **32px standard** height, 4px outer radius, contiguous items with an integrated 1px quiet border. Inner segments share borders without gaps; 13px label.
- **Chosen option is a selection**, therefore use **teal selected fill `--sv-selected-bg` and selected edge `--sv-selected-border`** with near-white text. Lime is for independent on/off toggles, affirmative actions—not for selecting one of mutually exclusive view modes.
- Inactive segments use recessed bg + secondary text. Hover uses established hover surface/border. Active selection must not shift width. Use single-select accessibility semantics (radio-group or tab pattern based on content).

## Inline links

- Inline links need to be identifiable without turning whole paragraphs cyan. Recommended distinct link color **`--sv-link: #86CDD0`** (lighter, muted teal compared with selected/focus teal), with underline **on hover and keyboard focus**. In long-form web copy, underline by default where color alone is ambiguous.
- Hover/focus color **`--sv-link-hover: #B2E5E6`**. Maintain visible focus. Do not confuse links with navigation selection or primary lime buttons. In muted secondary text, link color should still contrast adequately.

## Positive / negative numeric values

- Lime `--sv-lime` is the primary action/on-state token. **Do not flood financial tables with bright lime values.**
- **Ordinary positive financial values in dense tables remain near-white** `--sv-text`; a positive sign alone does not justify green. Use **`--sv-value-negative: #E8A0A0`** for genuine losses and **`--sv-value-positive: #A7D5A0`** for featured favorable KPIs, clearly meaningful favorable statistics in sparse cards, or rare threshold-defined exceptions in dense tables (not every winning row).
- Use tabular numerals, right alignment, signs/units and/or labels. Do not rely solely on color to convey gain/loss. Do not color a column green merely because it is currently ranked or sorted. A single deliberately designated primary favorable metric column MAY use subdued data green in accordance with `colors.md` and `tables.md`; other numerical columns remain neutral. Each peer KPI card may feature its equivalent primary value; see the headline rules below.

## Display metrics / headline numbers

- Use the contextual typography scale in `typography-spacing.md`: 20px/600 technical page titles or 24px/600 dashboard titles; 28px/600 standard metrics, 24px compact, and 28–36px featured content/dashboard metrics where appropriate.
- Line-height ~1.1–1.2 and tabular numerals. Near-white is the default; meaningful favorable results may use subdued data green. A semantically featured headline may use lime, including one equivalent headline per equally important peer card. Numerical magnitude alone does not establish importance. Supporting descriptions use readable-secondary; metadata may be smaller. Follow `colors.md` for semantic limits.

## Expandable data-grid rows

- The *expanded* row is **not automatically selected**. Expansion and selection are different states. The row keeps its current hover/selection state; add a chevron (right when closed, down when open) and optional subdued expanded-row background/border for context.
- Place details directly beneath the row in a full-width recessed `--sv-recessed` area with 1px quiet border and 8–12px padding; keep column alignment and keyboard/ARIA expanded state. Preserve selected background-led emphasis **only if the row is actually selected**.
- Expansion animation may use shared 150ms for small details, instant for complex layouts/reduced motion. Avoid extra row-level scrollbars unless truly needed.

## Inline code

- Inline `code`: Consolas/monospace, approximately **12px**, near-white text on recessed `--sv-recessed` surface, 1px quiet border optional, 4px radius, 2px horizontal/1px vertical padding. Preserve text selection, copy and wrap safely for long IDs/paths.
- Multiline snippets use a separately padded recessed code block with scrolling or wrap appropriate to content. Avoid code-style cyan text.


## Dense financial tables: approved featured-column option B

Use `--sv-value-positive` on **one intentionally prioritized favorable measure column** where it improves scanability (for example Profit/hr), not on every positive numeric cell and not simply because it is sorted. Keep other routine positive metrics near-white. Add small, exceptional context-defined green highlights sparingly. Do not turn entire columns green for common win rates, and keep bright lime out of dense numeric table columns. This rule refines earlier strict neutral-only dense-table wording; see `references/tables.md`.


## Coordinated identity and metric hierarchy (v1.5)

In an expressive content-rich card, an entity/item title and a featured numerical result MAY both be prominent because they answer different questions. Give identity strong near-white text; reserve lime for metrics explicitly qualified as featured under `colors.md`. Present supporting values in aligned, calmer groups and keep tertiary context readable. Equal peer cards use equivalent metric roles; the largest numerical result does not automatically become the featured category. See `identity-composition.md` for layouts and responsive sectional reflow.
