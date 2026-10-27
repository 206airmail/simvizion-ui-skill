# Responsive desktop window behavior

Responsive sizing follows **available component/content width**, not one global hard-coded window breakpoint. Preserve essential content and controls before optional actions. Standard panel padding 12px can reduce to 8px when genuinely dense, not as an automatic substitute for proper reflow. Forms use two columns when usable, stack labels and fields when width is inadequate. Min-width constraints prevent unusable panels, fields, numeric values, or action groups. Never clip important actions; truncate labels only when needed with full-text tooltip.

Modular windows: single panel → multi-panel contextually; detail/editor panes resizable where useful. Keep header fixed, content scrolling, footer fixed if it has persistent actions. Navigation width 180px expanded, 48px icon-only, then hidden with dropdown/drawer at very narrow widths. Responsive collapse/expansion instant and does not overwrite saved preference. Drawer 240px default, constrained viewport, 30% backdrop.

Toolbars: no routine wrapping on main application toolbar; overflow secondary action groups. Panel footer: Cancel+primary stay together, utilities shift to own row, very narrow may stack. Table toolbar: utility actions overflow first; if necessary reflow search/filter to second row rather than shrink to unusability. Status bar always one row, optional info suppressed and secondary actions overflow. Tabs: fixed small groups overflow to menu, dynamic document tabs scroll horizontally. Keep selection and focus visible with any layout. Reduced-motion means instant.

## Website and phone layouts

Do not impose the desktop application's 6px external window margin on public websites or render a whole webpage as a fixed-height pane. Public web pages use document scrolling, sensible page max widths (1120px general, 760px forms, 720px reading recommended) and adaptive gutters. Phone layouts use stacking, drawer navigation where useful, keyboard/safe-area-aware layout, and touch targets around 40px minimum while preserving compact visual controls. Detailed rules: `references/web-layouts.md`.
