# Scales

Scales are functions that transform a domain of data values (numbers, dates, strings, etc.) to a range of visual values (pixels, colors, sizes).

There are three type of scales
- **Continuous Scales** – mapping continuous domains to continuous output ranges ("linear", "pow", "sqrt", "log", "time", "utc", "sequential").
- **Discrete Scales** – mapping discrete domains to discrete ("ordinal") or continuous ("band" and "point") output ranges.
- **Discretizing Scales** – mapping continuous domains to discrete output ranges ("bin-linear" and "bin-ordinal").


The default scales for each type of field is given below.

|                      | Nominal / Ordinal   | Quantitative   | Bin-Quantitative| Temporal        |
|--------------------:|:--------------------:|:--------------:|:---------------:|:---------------:|
| __X, Y__             | Band / Point        | Linear         | Linear          | Time            |
| __Size, Opacity__    | Point               | Linear         | Bin-Linear      | Time            |
| __Color__            | Ordinal             | Sequential     | Bin-Ordinal     | Sequential      |
| __Shape__            | Ordinal             | N/A            | N/A             | N/A             |
