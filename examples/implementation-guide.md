> **v1.4:** Treat this as an implementation aid. Canonical references determine exact styling. Default panel header is integrated; selected table rows use a teal background rather than a full outline; invalid inputs use neutral borders with error indicators; lime means primary/on or a deliberately featured headline metric; subdued green conveys meaningful favorable data or success according to its semantic token.

# Practical implementation guide (Rust/Tauri, Electron)

1. Import `tokens.css` or map tokens into existing CSS variables or framework theme system. Prefer one CSS source of truth, avoiding duplicate hardcoded colors.
2. Layout using CSS grid/flex; use minmax(0,1fr), `min-width:0` for flexible text, and explicit scroll containment (`min-height:0; overflow:auto`) to make fixed headers and scrolling bodies work.
3. Use semantic class-based variants (`.sv-button--primary`, `.sv-panel__header`, `.sv-row--selected`) rather than inline per-component styles. Keep state mappings consistent.
4. Use `box-sizing:border-box` and reserve borders, icon slots and close-button space to prevent reflow on hover/selection.
5. Match only **actual app needs**: avoid creating notifications, logs, project selectors, filters, sorting, databases or backends merely because the skill includes their styling.
6. Test at normal, compact and very narrow windows; verify native desktop title bar/insets, control focus, keyboard navigation, scrolling regions, reduced motion and DPI scaling.
7. Open the actual applicable reference images before design; Markdown links alone are insufficient. Reference screenshots are the source of aesthetic intent when supplied. Compare excess cyan, border strength, paddings, font scale, title hierarchy, and hover/selected color balance.
8. Document unavoidable deviations (e.g. OS-native file chooser) and keep their surrounding controls in SimVizion style.

## Example component composition
```html
<div class="sv-panel">
  <div class="sv-panel__header"><strong>Properties</strong></div>
  <div class="sv-panel__content">...</div>
  <div class="sv-panel__footer"><button class="sv-button sv-button--secondary">Cancel</button><button class="sv-button sv-button--primary">Apply</button></div>
</div>
```

The snippet expresses visual structure only. Event handlers, validation, storage, and data workflows are application-owned.

## Public website and added components

Use the same core tokens on the web, but use natural document scrolling rather than desktop pane scaffolding. Use bounded page/form widths and phone-appropriate stacking. `references/web-layouts.md` and `references/extended-components.md` contain new v1.1 patterns. The CSS file supplies example classes for links, pills, segmented controls, display metrics, code, and alerts. Treat the CSS as a starter (not a full component library); validate contrast, semantic accessibility and real layout rendering. The `--sv-primary` variable is a backward-compatible alias to the canonical `--sv-lime`.

## Financial-data implementation guardrail

Do not set lime/green merely because a numeric value is greater than zero. The `.sv-value--positive` class deliberately renders near-white; `.sv-value--positive-exceptional` is opt-in only for an application-defined exceptional threshold. Negative results can use `.sv-value--negative`, with signs/labels retained. Do not automatically style the primary sort column green.

### Approved metric-color application

For cards, style a deliberately featured favorable value with `var(--sv-value-positive)` as a sparse accent (for example, one headline per station card). Keep ordinary numeric table cells `var(--sv-text)` even when positive, and reserve `var(--sv-value-negative)` for genuine losses. Other meaningful favorable statistics may use subdued green sparingly where domain semantics support it. Do not infer green from a plus sign or from ranking alone. Win-rate thresholds are application-defined; choose amber for cautions and red only for genuine failures.


## v1.3 content and visual-impact checks

Use `--sv-text-readable-secondary` for descriptive text that should be comfortably read. Use `.sv-content-card` selectively for content-rich cards without inserting decorative nested sections. The `.sv-kpi--headline-featured` class is reserved for genuine headline KPI roles; equal peer cards may each use it for their equivalent featured metric. Dense tables continue to use subdued data-green only for designated favorable roles. At the end of implementation, inspect normal and constrained layouts, confirm fonts actually load, check browser zoom/OS scaling, and assess the whole screen for proper hierarchy rather than merely token compliance.

See `composition-review.md` for a worked dashboard critique and `../references/identity-composition.md` for canonical branding/effect rules. Functional checks and visual review need separate evidence.
