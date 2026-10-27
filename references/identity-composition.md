# Family identity and screen composition — canonical guidance (v1.4)

## Stable family, purpose-built applications

SimVizion should be recognizable across an editor, dashboard, catalog, small utility and public website. Shared identity comes from deep teal-black surfaces, clear near-white typography, deliberate lime and cyan roles, crisp bordered controls, coherent imagery, and controlled depth. It does not require the same navigation, page proportions, card grid, viewport, or density.

Choose the primary task and reading order before choosing containers. State the proposed composition briefly for substantial screen work; do not require a design ceremony for a small control change. Dense inspection, browsing, comparison and form entry need different arrangements. Do not add a canvas, chart, hero section, sidebar or artwork merely to resemble a reference.

## Composition and scale

- Give product identity deliberate presence appropriate to the application. A modest branded header can establish character without consuming the screen; a tiny utility need not have a large masthead.
- Choose density by region. Use the content typography scale for dashboard titles and explanations; retain technical typography for controls and dense tables. Do not make an entire website inspector-sized.
- Place useful work early. Consolidate quiet operational metadata when appropriate; avoid repeated introductions and status cards without a distinct purpose.
- Give equal peer categories equivalent visual importance. Align recurring titles, metrics and actions where it improves comparison; equal-height cards are optional. Preserve sensible reading order on narrow screens.
- Use artwork at a size that is legible and meaningful. Preserve aspect ratio and consistent framing; provide accessible names/alternative text where informative and usable missing-image states. Use only assets with appropriate rights.
- Structure comparisons with labels and aligned values when prose obscures relationships. Avoid repeating identical explanatory blocks when a shared explanation or compact status communicates the same facts.
- Match container width to its content. A broad dashboard or table may use more space than a form; avoid a wide form panel containing a narrow unexplained island of fields. Empty space is valid when intentional.

## Atmospheric and branding treatments

Restrained gradients, illumination and imagery are permitted parts of the family language. They are optional tools, not completion requirements. Core surface colors and semantic state tokens remain stable.

Approved roles:

1. **Identity region:** low-contrast teal shading, fine nonessential linework and localized emblem backlighting can give a product header depth.
2. **Domain artwork:** coherent illustrated library/catalog tiles may include soft lighting within their artwork frames. This is distinct from ordinary utility icons.
3. **Primary action:** a restrained static lime halo may reinforce an already recognizable primary button. It must not replace its boundary, label, focus indicator or disabled treatment; use selectively within functional contexts.

Define effects through named contextual tokens. `examples/tokens.css` supplies optional illustrative values, not new mandatory global surfaces. Keep gradients and lighting away from dense data backgrounds and essential labels. Check contrast against the actual composite. Focus, hover, selection and status must remain independently identifiable; ambient lighting does not communicate state. Do not animate ambient lighting by default. Provide a plain-surface fallback when effects are unavailable or inappropriate.

**Appropriate:** a subtle teal header wash around a clear product emblem, quiet data panels, framed item artwork and one restrained illuminated primary action.

**Excessive:** glowing every card edge and icon, gradients behind table rows, saturated cyan body text, or pulsing lights competing with data. Also avoid interpreting restraint as a requirement for uniformly flat, anonymous screens.

## Visual review and evidence

Open the relevant reference images and distinguish styling from domain-specific content. Compare overall hierarchy, surface relationships, typography, branding and emphasis, without copying their screen arrangement. Inspect normal and constrained renders and representative states. Check whether effects remain coherent on wide screens and narrow layouts.

Identify concrete weaknesses, correct those within the authorized scope, and recheck. Report unresolved design issues rather than inventing scores. Functional/layout validation establishes usable behavior; a separate visual critique establishes what was observed about composition and family character. Neither substitutes for the other.
