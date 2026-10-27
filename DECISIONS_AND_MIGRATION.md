# SimVizion v1.3 — consolidation notes (non-authoritative)

The governing principle is **Family Resemblance, Not Uniformity**. New applications may freely choose functional layouts; modernization preserves workflows and makes targeted improvements. Desktop-first, web-adaptable.

## Explicit choices retained

- Surface-led panel separation, integrated headers, spacing-first sections, contextual dividers.
- Near-white subsection headings; cyan used for navigation, focus, selection and selective informational values.
- Strong selected outlines **for navigation destinations**, connected outlined tabs; background-led selection **for table rows**.
- Consistently bordered ordinary buttons and icon-only buttons; text-first labels with purposeful icons; one dominant primary action per functional context.
- Recessed control family; 32px normal / 28px compact; horizontal labels in inspectors / stacked in forms; neutral invalid fields with error icons; disabled colors distinct from read-only.
- Dropdown selected background/checkmark; keyboard highlight with narrow cyan marker; connected menu.
- Checked/on lime for checkbox/radio/switch; routine success subdued green. Status prominence by consequence; favorable numerical green only for featured meaningful data, maximum one uniform featured favorable table column.
- Contextual search, empty/loading states, resizable panels, responsive window constraints, table organization, sorting, overflow, multi-selection, and status bars.
- Small functional motion, outline icons, readable typography, contrast checks and proportional visual-polish pass.

## Migration check

Where older examples implied red invalid borders, per-row full selected outlines, cyan subsection headings, elevated panel headers by default, or white outer focus rings, v1.3 canonical rules supersede them. Reference CSS demonstrates sample classes, not a complete framework component library. Test every real component and its states in the actual app.


## v1.3 approved visual-impact refinements

- Selective **bright lime** on semantically featured headline values, including one equivalent metric per equally important peer card; no blanket lime columns.
- Readable-secondary prose `#C5D4D6`, while secondary labels and tertiary metadata remain distinct.
- Adaptive content/dashboard typography while retaining compact 13px table and control typography.
- Intermediate `#101F23` optional *unified* content-rich card surface; decorative internal segmentation is not mandatory.
- Contextual density, 16px content-card padding as a starting point, and balanced use of available space.
- Purpose-driven focal hierarchy: never arbitrarily feature one of several equal peers based on magnitude.
- Mandatory whole-screen visual polish when a rendered app is available; test font rendering before applying smoothing hacks.
