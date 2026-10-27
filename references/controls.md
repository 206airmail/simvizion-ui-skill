# Controls

## Buttons
Standard height 32px, compact 28px, radius 4px, border 1px, horizontal padding 10px standard/8px compact. Primary lime background `#9AF000`, dark `#050C0E` content; hover `#ADFF24`, pressed `#7DC900`. Secondary recessed `#071215`, border `#294147`, near-white text, hover bg `#1B3237` border `#41858D`, pressed bg `#102328`. Tertiary less prominent. Destructive outlined bg `#24191C`, red border/text; filled red for high-severity confirmations. Disabled neutral surface. Icon-only buttons **always show a bordered shape**, hitbox 28/32px, icon 14/16px. Loading spinner and verb text e.g. “Saving…”; preserve width, avoid duplicate action.

## Inputs and validation
Text/numeric fields 28/32px height, 8px horizontal inset, recessed bg, radius 4px, 1px border. Hover border only where appropriate; focused teal **border only**. Invalid values retain a neutral field border with a clearly associated red error icon and concise specific explanation; cyan keyboard focus stays distinct. Do not wipe invalid in-progress text automatically or report partially typed values too early. Enter/blur commits valid drafts, Escape reverts. Numeric editing: optional stepper, optional predictable hold-to-repeat without a universal mandated timing; no incidental mouse-wheel value edits; tabular digits. Search left magnifier, right clear-X if text, live local filtering when inexpensive; debounce or explicit submission for expensive searches. Match indication and no-results feedback must be contextual; count only when useful.

Checkbox 18px radius 3px, lime on/indeterminate; radio 18px circle lime dot. Switch 32×18px, compact thumb sized to fit its track, full radius; **lime track when on**, dark track when off, subdued disabled state; restrained short transition. Checkbox uses lime fill/dark check, radio uses lime dot on recessed circle; focus remains distinct. Slider 4px track, lime fill, 12px thumb, numeric input at right (about 64px). No default ticks. Textarea 96px minimum, auto-grow to 256px max then scroll; no default resize handle; 8px padding.

## Dropdowns
Field and expanded menu form a continuous shape without internal separator or gap. Background `#071215`, 28px item height, max 224px list before scroll, 6px scrollbar. Committed selected option: selected teal background with a teal checkmark, no mandatory per-option full outline. Hover uses hover surface; keyboard-highlighted option uses hover surface plus reserved narrow cyan indicator; committed and keyboard-highlighted states remain independently visible. Standard Up/Down/Enter/Escape/Tab; menu closes after selection. Searchable grouping only when appropriate.

## Common compound controls
Editable path input with adjacent Browse button, 6px gap; native file picker preferred. Middle truncate paths visually when needed, tooltip full value; focus exposes full text; no writing to invalid drag/drop path. Time/date pickers reuse the same field, popover, focus, and error styles. Date calendar 260px width, 32px cells, 3px cell gap; selected teal outlined cell. Date-range intermediate cells soft-connected teal `#17363B` rather than hard rectangular stripes. Time picker list rows 32px, typically five visible; staged Apply/Cancel where changing more than one column. Avoid inventing special styling not based on core tokens.

## Additional controls and focus on lime

For pills, segmented controls, count chips and inline links consult `references/extended-components.md`. Segmented controls use **teal selection**, not lime, because they represent mutually exclusive view choices. Compact controls within toolbars are **28px tall** by default; the toolbar itself remains 40px high by default. Use 32px controls when a larger toolbar warrants them.

Default keyboard focus uses a 1px cyan-teal boundary. Where that fails to distinguish focus (especially on lime-filled controls), strengthen focus using a contrasting inset/outline as necessary, without changing geometry or mandating an unrelated bright white outer ring. Focus remains visible without glow, and must be distinguishable from selected/on state. Do not reduce hit areas to make room for focus styles.
