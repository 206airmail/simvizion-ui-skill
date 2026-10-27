# SimVizion color system — canonical reference (v1.3)

> **Authority:** This file owns the color values and semantic color-use rules. `SKILL.md` summarizes the visual identity; `QUICK_REFERENCE.md` and `examples/tokens.css` must implement this file without defining competing standards. Component references own geometry and interaction mechanics. **Family resemblance, not uniformity:** keep the identity stable while designing layouts for their actual purpose.

## 1. Core surfaces, boundaries, and text

| Role / CSS token | Value | Use |
|---|---|---|
| `--sv-window` | `#050C0E` | Main application background |
| `--sv-panel` | `#0D1B1F` | Standard content panel |
| `--sv-surface-content-raised` | `#101F23` | Unified intermediate surface for content-rich cards; optional purposeful internal grouping |
| `--sv-elevated` | `#14272B` | Floating/raised content, toolbars where specified |
| `--sv-recessed` | `#071215` | Input fields, recessed content, dropdown menus |
| `--sv-border` | `#294147` | Normal 1px structural/control borders |
| `--sv-text` | `#EDF4F5` | Primary text, ordinary numeric values |
| `--sv-text-readable-secondary` | `#C5D4D6` | Frequently read supporting descriptions and explanatory content |
| `--sv-text-secondary` | `#A6B8BC` | Labels, meaningful supporting prose, secondary values |
| `--sv-text-muted` | `#91A6AB` | Metadata, placeholders, quiet helper text |

Near-white, readable-secondary (`#C5D4D6`), and neutral gray-teal are the default text hierarchy. Frequently read descriptions SHOULD use readable-secondary instead of metadata-muted colors. **Do not color every heading, label, or value cyan.** Do not use muted text for essential instructions. Separate regions primarily through surface contrast and spacing; borders reinforce purposeful boundaries. The intermediate surface MAY be used for whole content-rich cards. Internal raised strips are optional and must reflect meaningful groups, not decoration. Standard buttons remain visibly bordered; not every nested panel needs a full outline.

## 2. Functional accents and interactive states

| Role / CSS token | Value | Meaning |
|---|---|---|
| `--sv-lime` / `--sv-primary` | `#9AF000` | Dominant affirmative action in a functional context; checked/on controls |
| `--sv-primary-hover` | `#ADFF24` | Primary button hover |
| `--sv-primary-pressed` | `#7DC900` | Primary button pressed |
| `--sv-teal` | `#42CDD2` | Focus, active navigation, selection and interactive emphasis |
| `--sv-selected-bg` | `#194047` | Selected/active surface |
| `--sv-selected-border` | `#42C4CB` | Strong selected edge when appropriate to component |
| `--sv-hover-bg` | `#1B3237` | Hover surface |
| `--sv-hover-border` | `#41858D` | Hover border on discrete controls |
| `--sv-secondary-pressed` | `#102328` | Secondary button pressed background |
| `--sv-link` | `#86CDD0` | Links and selectively emphasized noninteractive technical context |
| `--sv-link-hover` | `#B2E5E6` | Link hover/focus text |

**Lime signifies actions and checked/on control state, plus approved semantically featured headline metrics; not routine success results, navigation, or ordinary numeric profitability.** Do not turn every positive number green. One dominant lime action per *functional context* is the normal hierarchy; independently functioning panels/dialogs may each have one.

**Teal signifies navigation, selection and keyboard focus.** Infrequent noninteractive informational emphasis (e.g., active profile name or important identifier) MAY use restrained `--sv-link` teal when it materially aids orientation; it is not a default label, heading, or numeric-data color. Hyperlinks must remain recognizable as links through semantics and appropriate underline treatment, especially in prose.

**Component-specific visual treatment is contextual:** bordered active sidebar/navigation items use selected background + selected border; connected tabs retain a defined active boundary; selected table rows use background-led selection without mandatory full-row outlines. Hover must not erase selection. Keyboard focus is separate from both selection and pointer hover; default is a 1px cyan-teal focus boundary, strengthened where accessibility or state distinction requires, without shifting geometry. Component references specify precise behavior.

## 3. Semantic statuses: outcomes, warnings and errors

| Role / token | Color | Meaning |
|---|---|---|
| `--sv-status-success` | `#A7D5A0` | Confirmed successful outcome or healthy operational status |
| `--sv-warning` | `#F0B84B` | Warning, caution, risk requiring attention |
| `--sv-error` | `#F07171` | Error, failed operation, invalid condition |
| `--sv-status-info` | `#86CDD0` | Informational status where semantic color is useful |

Status **meaning** determines semantic color; status **severity and consequence** determine prominence. Routine successful outcomes such as “Saved” or “Connected” SHOULD use understated neutral text with a subdued green icon/indicator as appropriate. Warning or blocked actions may use progressively more visible tinted containers, semantic indicators and actionable instructions. Keep long message text near-white; never rely on color alone. Not every success needs green text or a large banner.

For tinted status containers, existing guidance permits a lightly tinted semantic background (approximately `0x30` alpha) and a stronger but restrained semantic edge (approximately `0xCC` alpha). These are *presentation conventions*, not requirements to fill every status message with color. Verify contrast against the actual composited surface.

**Validation:** Invalid fields retain normal neutral borders, show a red error icon and an understandable associated explanation. When invalid and keyboard-focused, the teal focus indication remains recognizable alongside the error indication. Do not automatically turn input borders or full fields red. Dedicated error presentation may be stronger for blocking errors.

## 4. Data and numeric color hierarchy

| Role / token | Color | Policy |
|---|---|---|
| Ordinary numeric values | `--sv-text` `#EDF4F5` | Default, including positive values, margins, medians, win rates, ranks |
| `--sv-value-positive` | `#A7D5A0` | Featured favorable KPI, meaningful favorable statistic, or designated primary favorable metric column |
| `--sv-value-negative` | `#E8A0A0` | Genuine loss or unfavorable result, not merely a negative sign without context |
| Cautionary statistic | `--sv-warning` `#F0B84B` | Context-defined caution, incomplete history or meaningful risk |

**Sparse KPIs and equivalent peer cards:** A genuinely featured headline metric MAY use bright `--sv-lime` for visual impact; subdued `--sv-value-positive` remains available for meaningful favorable statistics. In a group of equally important entities, the same featured-metric role MAY be bright lime in every peer card without arbitrarily elevating one card. Ordinary positive values remain neutral; numerical magnitude alone never triggers headline status.

**Dense tables:** A table MAY intentionally designate **one primary favorable metric column** (for example Profit/hr) for subdued green emphasis, typically with medium/semibold text. This is a role-based decision by the application—not a consequence of a plus sign, row ranking, or active sort column. If a value in the designated column is neutral or unfavorable, style it neutrally or with its relevant negative meaning, **not automatically green**. Other profit, median, margin, win-rate and ranked metrics remain near-white by default. A few separately defined exceptional favorable values MAY also use green; never introduce a second uniformly green column. Sorting and selection stay independent from data semantics.

Reliability and win-rate color thresholds MUST be defined by the application's domain, if used; do not hardcode universal thresholds. Negative outcomes and caution must remain meaningful, labeled and not color-only. **Bright lime is never the routine numeric table-data accent.**

Although `--sv-status-success` and `--sv-value-positive` currently share the same hex value, they are **separate semantic roles** and should retain distinct names.

## 5. Destructive, disabled, switch and scrollbar tokens

| Token | Value | Purpose |
|---|---|---|
| `--sv-destructive-bg` | `#24191C` | Destructive action background |
| `--sv-destructive-hover` | `#F48787` | Destructive label/hover border emphasis |
| `--sv-destructive-pressed-bg` | `#341C22` | Destructive pressed background |
| `--sv-destructive-pressed` | `#D85B5B` | Destructive pressed edge |
| `--sv-disabled-bg` | `#101A1D` | Dedicated disabled surface |
| `--sv-disabled-border` | `#223338` | Disabled border |
| `--sv-disabled-text` | `#789096` | Disabled text/icon |
| `--sv-switch-on` | `#203518` | Subdued alternative active-switch surface where specified |
| `--sv-switch-on-hover` | `#2A451E` | Subdued switch hover |
| `--sv-switch-on-pressed` | `#14250F` | Subdued switch pressed |
| `--sv-scroll-track` | `#14272B` | Scrollbar track |
| `--sv-scroll-thumb` | `#41858D` | Scrollbar thumb |
| `--sv-scroll-thumb-hover` | `#42AEB5` | Hover thumb |
| `--sv-scroll-thumb-active` | `#42C4CB` | Dragged thumb |

The approved standard checkbox and toggle *on* appearance uses bright lime; the subdued switch tokens are existing contextual alternatives and MUST NOT override that default. Disabled controls use dedicated colors instead of blanket opacity and show no normal hover/pressed affordance; read-only fields remain legible and copyable where appropriate. The scrollbar visual width is **6px**, with a larger usable pointer target where practical.

Destructive action style remains red regardless of whether that action is the main choice in a confirmation workflow. Red for invalid field indicators is separate from the component's neutral structural border.

## 6. Accessibility, extensions, and implementation parity

- Check text and essential visual-state contrast against the **actual** surface. Target at least **4.5:1** for normal text and **3:1** for qualifying large text and essential nontext indicators; passive decorative panel borders need not meet a control-boundary target. Focus must be visible and distinguishable; enhance its default 1px teal border when needed. Verify case by case rather than recoloring the entire palette.
- No semantic status or selected state is conveyed by color alone; use labels, icons, border geometry, text weight, or other redundant cues as appropriate.
- Keep core tokens fixed. Application-specific specialized data visualizations MAY extend the palette with documented semantic tokens; normal UI may not quietly invent alternative primary, hover, input or selection colors.
- `examples/tokens.css` and condensed guidance must be synchronized to this reference. The v1.3 implementation examples and quick reference must remain aligned with this canonical specification; flag any future drift as a defect rather than treating it as an approved alternative.
