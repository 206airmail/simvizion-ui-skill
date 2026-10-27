# Charts and technical data visualization — controlled extensions (v1.4)

Charts are not required in every SimVizion application. When used, their **containers, typography, grid, legends, controls, and interaction states MUST use canonical SimVizion tokens**. The number and kind of data series should determine the chart type and encoding, not the desire to introduce additional accent colors.

## Data-series color rules

- Ordinary chart-series colors are **categorical encodings**, not success/warning/error signals. Do not automatically use `--sv-lime` for the first series or red/green for arbitrary series. Lime retains its primary action / checked-control meaning.
- A one-series chart MAY use restrained cyan/teal when it does not misleadingly imply selection, focus, or an info status. Prefer near-white or neutral labels and secondary lines.
- For multiple series, create a **small, chart-scoped categorical palette** chosen to provide distinguishable hue, luminance and shape/line patterns on `--sv-panel` and `--sv-recessed`. Store it as named app-specific tokens (`--sv-chart-series-1`, etc.). Do not promote these into global UI accents.
- Use colors **consistently across charts in the same application**. Preserve category/series identity in legends, tooltips, selections and exports. Do not rely on color alone: use direct labels, line patterns, shapes or markers when necessary.
- Use the existing semantic green/amber/red only when the underlying data truly conveys success, caution or loss, or where explicitly meaningful threshold bands are shown. These semantic colors are not a default categorical series palette.
- Keep axes, gridlines, legend text, table numbers and supporting annotations subdued but readable. Highlight the actual active/selected datum with the established teal selection treatment, not a permanently glowing chart.
- Avoid gradients, 3D effects, gratuitous animation, dense gridlines, excessive colored fills and unexplained visual embellishment.

## Data-specific requirements

- Use tabular numerals for chart values and aligned statistics; units, baselines, scales, sample sizes, zero references and time zones should be clear when relevant.
- Domain thresholds such as positive/negative results or exceptional performance MUST be specified by the application, never guessed from the theme.
- Present accessible table/summary alternatives when a chart communicates essential data. Tooltips and chart interaction must work with the target platform, including keyboard use where appropriate.
- Respect reduced motion. Avoid invented intermediate values or inaccurate interpolation for live metrics.

Chart-series colors are an **approved category for controlled extensions**, not a fixed universal palette. Their exact hex values must be selected and tested against the actual application data and visualizations.
