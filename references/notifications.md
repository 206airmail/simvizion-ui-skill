# Visual feedback: toasts, progress, logs, empty/loading states

## Toast appearance
Toasts top-right of usable content with 16px top/right inset; max width 360px; elevated `#14272B` background, border `#294147`, radius 6px, 12px padding, standard shadow. 20px semantic outline icon aligned at top of text. Title 13px/600 near-white; description 12px/400 secondary; 4px text gap. Right close-X always visible 20px target, 14px icon, accessible label. Optional one action in compact secondary styling bottom-right. Up to three visible, stacked downward with 8px gap. 150ms opacity fade, reduced motion instant. Routine success 3s, actionable 6s, important requiring attention persistent. Don't steal focus; announce accessibly, keep actions keyboard-accessible. Never make toast body implicitly clickable. Status icon conveys severity; avoid colorful text bodies.

A notification history interface is optional and determined by the application, not mandated by this visual skill. If present, it can be a compact elevated popover or right sidebar, using the same panel, scrollbar, search, filter, table/list and icon standards. Read/acknowledgment/storage rules are owned by the application.

## Progress
6px progress track recessed `#071215`, lime fill `#9AF000`, fully rounded. Status label left and percent right above bar; supporting details below. Width progress transition about 150ms; latest values not falsified; 100% only once confirmed. Spinners for indeterminate progress; completed success feedback uses subdued green, warnings amber and errors red as appropriate. Button spinners preserve size. For long operations, status/errors remain legible; visual loading can be spinner or skeleton according to scale. Reduced motion: no pulsing/sweeping animations.

## Logs
Technical operation logs may be recessed `#071215` bordered 4px panel with Consolas 13px, line height 1.3, 2px between entries. Timestamps secondary-muted, level label semantic, body text near-white. Optional fixed toolbar for Copy All / Save Log / Clear. Smart auto-scroll only when currently at bottom; paused state offers Resume Auto-Scroll. Logs can be collapsed by default for normal apps, exposed when the user's workflow needs them. Copy buttons 28px bordered; success tooltip “Copied!” ~1200ms only when copy genuinely succeeds. File export mechanisms and log retention are application-owned.

## Empty/loading/error
Keep tiny lists simple. In prominent/large panels, center a muted outline icon, near-white short heading, secondary explanation, optional relevant secondary action. Distinguish no data from no search results. Keep headers fixed while body loads. Spinner for short tasks, skeleton rows when maintaining larger layout prevents reflow. Skeleton colors `#294147`, `#223338`; reduced-motion placeholders static. Errors: red semantic icon, specific actionable description, optionally collapsible technical details, retry where meaningful; don't erase valid partial data. Do not prescribe backend retries or storage behavior.

## Persistent in-page banners

Not every alert is a toast. Use a persistent banner for ongoing application-level information: 20px semantic icon aligned with first text line, 12px padding, 6px radius, subdued tinted semantic background/border, near-white 13px/600 heading and readable description. Optional dismiss/actions as relevant. For detailed styling see `references/extended-components.md`. Never enforce notification persistence, storage, or retry architecture through these visuals.
