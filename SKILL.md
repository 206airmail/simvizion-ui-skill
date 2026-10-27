---
name: simvizion-ui
version: 1.2.0
description: Apply the desktop-first SimVizion visual design language to new applications, existing applications, and web adaptations. Preserve a recognizable SimVizion family identity while choosing application-specific layouts, navigation, and workflows. Use for UI design, modernization, implementation, and visual review in Rust, Tauri, Electron, native desktop frameworks, and browser interfaces.
---

# SimVizion Unified UI Design Skill

## 1. Identity and philosophy

**Family Resemblance, Not Uniformity.** SimVizion is a shared visual design language, **not** a prescribed application template.

**Design every application for its purpose. Make every application unmistakably SimVizion.**

Applications MUST preserve the recognizable SimVizion identity through its canonical color system, typography, spacing language, surface treatments, component appearance, interaction semantics, and accessibility foundations. Applications MUST NOT be forced into identical layouts, navigation structures, panels, or workflows merely to resemble another SimVizion program.

Favor clarity, efficient technical work, readable information, and restrained polish over decoration, generic framework aesthetics, and unnecessary visual activity.

### Platform scope

- **Primary:** Desktop applications, including Rust, Tauri, Electron, and native Rust UI frameworks. Existing SimVizion desktop references establish the primary visual direction.
- **Adaptable:** Browser-based dashboards, web applications, and public websites MAY use the same visual identity with platform-appropriate layout, input, and accessibility adaptations. Do not force desktop interaction patterns onto touch or mobile environments.

## 2. Visual identity at a glance

- **Surfaces:** Deep teal-black window backgrounds, distinct but subtle panel surfaces, and recessed inputs. Prefer surface contrast and spacing over excessive panel borders and nested containers.
- **Accents:** SimVizion Lime for dominant affirmative actions and checked/on controls; cyan-teal for navigation, focus, selection, and selective meaningful informational emphasis. Semantic success, warning, error, and info colors communicate actual meaning, not decoration.
- **Text:** Predominantly near-white and neutral gray-teal; do not make ordinary body text or every heading cyan. Use restrained, purposeful emphasis for featured favorable statistics.
- **Typography:** Segoe UI Variable (Segoe UI fallback); 13px base text; compact, modest heading hierarchy; tabular numerals for aligned technical data.
- **Density:** 32px standard and 28px compact controls, 4px spacing rhythm with 2px refinements, 6px control/panel gaps where appropriate, and 12px standard panel padding. Keep text readable in both densities.
- **Geometry:** Crisp 1px boundaries where functional; restrained 4px control, 6px panel, and 8px dialog radii. Defined button boundaries; recessed fields; low-key shadows on floating elements.
- **Interaction:** Distinct hover, selected, focused, checked, invalid, loading, and disabled states. Keyboard focus remains independently identifiable.
- **Icons and motion:** Coherent Lucide-like outline icons and subtle functional transitions; no ornamental glows, oversized shadows, or unnecessary animation.
- **Composition:** Layout, navigation, and workspace arrangement are chosen for the application's actual tasks, not copied from existing SimVizion screenshots.

This summary conveys the identity; **canonical references own the exact values, component variants, and detailed behaviors**. Do not use this summary as a second independent token source.

## 3. Rule authority

- **MUST / Required:** Preserve functionality, data integrity, applicable accessibility requirements, core identity tokens, and established interaction semantics. Explicitly approved component decisions are binding where applicable.
- **SHOULD / Default:** Follow documented component appearances and usage patterns. Use an approved contextual variant when its documented conditions apply.
- **MAY / Contextual:** Choose application-appropriate layout, navigation, panel organization, information density, and necessary specialized visualization components.

**Contextual flexibility does not authorize arbitrary visual substitutions.** In particular, do not replace approved bordered buttons with borderless buttons, or the approved strongly bordered active navigation with a minimalist alternative, simply for stylistic preference.

Component-specific rules MAY specialize general guidance, but cannot override required functionality or accessibility.

## 4. References and source of truth

Before any SimVizion UI work, read this `SKILL.md` and the canonical foundations in `references/colors.md` and `references/typography-spacing.md`. Then read **all references relevant to the affected UI**:

| Work area | Authoritative reference |
| --- | --- |
| Colors, accents, and semantic data colors | `references/colors.md` |
| Typography, spacing, control geometry | `references/typography-spacing.md` |
| Buttons, inputs, checkboxes, radios, sliders, validation | `references/controls.md` |
| Panels, navigation, tabs, toolbars, status bars | `references/layouts.md` |
| Dialogs, popovers, dropdown/context menus, tooltips | `references/dialogs-popups.md` |
| Loading, progress, notifications and feedback | `references/notifications.md` |
| Dense tables, numeric hierarchy, sorting, selection, overflow | `references/tables.md` |
| Icons, motion, focus and interaction guidance | `references/icons-motion.md` |
| Constrained windows and responsive desktop layout | `references/responsive.md` |
| Web/mobile adaptations when relevant | `references/web-layouts.md` |
| Specialized UI components and metrics | `references/extended-components.md` |
| Charts, multi-series data and technical visualizations | `references/data-visualization.md` |
| Visual family examples and anti-patterns | `VISUAL_REFERENCE.md` |

`QUICK_REFERENCE.md` is a convenience summary, **not** an independent authority. `examples/tokens.css` and `examples/implementation-guide.md` are implementation aids, **not** independent rule sources. Do not infer that every detail of an existing example is mandated for every application.

**Conflict process:** (1) protect functionality/accessibility; (2) apply these governing principles; (3) consult the canonical reference for the affected area; (4) use documented context-specific variants; (5) flag genuine inconsistencies rather than silently inventing a new design rule. Do not assume that an older example overrides an approved newer decision.

**Version alignment:** The references in this package are consolidated for v1.2. Report remaining ambiguities; do not treat example CSS as a competing authority.

## 5. Agent workflow

1. **Understand the task.** Establish the application's primary purpose, workflows, platform, information hierarchy, constraints, and whether the work is a new UI, major redesign, or targeted modification.
2. **Design for purpose.** For a new application, choose the best composition rather than copying another SimVizion layout. Add sidebars, tabs, cards, tables, or complex workspaces only where useful.
3. **Preserve existing workflows.** When modernizing an existing application, retain functioning behaviors and familiar information architecture. Improve alignment, grouping, hierarchy, spacing, and inefficient layout where justified. Substantial restructuring requires explicit authorization.
4. **Load relevant references and apply tokens.** Use canonical specifications and the project's existing component architecture where practical. Reuse documented variants; avoid arbitrary values or unnecessary new dependencies.
5. **Implement all relevant states.** Include hover, pressed, focus, selection, checked, disabled, loading, validation, and keyboard behavior as appropriate. Distinguish disabled from read-only. Keep technical values accessible without breaking compact layouts.
6. **Inspect the rendered UI when available.** Check representative normal, constrained, and expanded window sizes as appropriate, along with focus, error, and selected states. Verify the whole-screen composition, not only individual components.
7. **Perform a proportional polish pass.** Correct awkward alignment, spacing, hierarchy, excess accent usage, unwanted borders, clipping, and balance issues **within the approved layout and workflow boundaries**. Do not use polish as permission for wholesale redesign.
8. **Report verification and deviations.** State what was checked, meaningful approved extensions, unresolved issues, and anything that could not be visually verified.

### Existing-application modernization boundary

Prefer **targeted adaptation over unnecessary replacement**. Restyle or modestly adjust an existing working component when possible. Do not replace navigation paradigms, relocate core workflows, remove features, or rewrite business logic merely to apply SimVizion. Recommend substantial changes separately and obtain authorization before implementing them.

## 6. Extensions and implementation

Canonical design specifications are framework-independent. CSS and native UI implementations SHOULD consume shared named tokens and reproduce the documented appearance and behavior; no particular UI framework or component library is required.

Application-specific extensions MAY be introduced for genuine needs such as specialized technical canvases, syntax highlighting, or multi-series charts. First check the existing system; name and document necessary additions; preserve the core visual identity. Do not redefine global tokens to solve a local problem.

Reference code SHOULD demonstrate required component states and SHOULD be maintained alongside the corresponding specification. If an example disagrees with a canonical rule, correct the example; do not silently change the rule.

## 7. Validation and completion

Before declaring UI work complete, verify as applicable:

- [ ] The interface is recognizably SimVizion **without copying another application's layout**.
- [ ] Canonical color, typography, spacing, geometry, icon, and motion rules are followed.
- [ ] Lime, cyan-teal, and semantic colors are used intentionally; ordinary text remains neutral and readable.
- [ ] Buttons, fields, menus, navigation, tables, and dialogs follow their canonical component rules and applicable interaction states.
- [ ] Layout supports actual tasks, respects supported window sizes, and handles overflow without hiding essential information.
- [ ] Keyboard interaction, focus visibility, contrast, labeling, reduced motion, and relevant scaling/accessibility behaviors are checked.
- [ ] Existing application logic, data, and familiar workflows are preserved unless authorized otherwise.
- [ ] A visual polish pass has been performed against the **rendered** UI where available.
- [ ] Approved extensions, unresolved deviations, and unverified items are clearly reported.

Do not claim rendered visual compliance from source-code inspection alone. Do not invent a numerical compliance score. **Preserve what works. Improve what needs improvement. Redesign only when justified and authorized.**
