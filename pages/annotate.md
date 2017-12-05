# Annotate

Annotations are useful to help the audience understand the visual data better.

- **Title**: To provide overall overview of the data.
- **Axes**: Provide axis lines, ticks, and labels to convey how a positional range represents a data range. Axes visualize (positional) scales.
- **Legends**: Legends aid interpretation of scales with ranges such as colors, shapes and sizes. Legends visualize scales. 
- **Grids and Reference marks**
- Text Annotation
- Story Elements *// Not available*


```vis
title: Demonetisation Overview 
width: 600
height: 400
data:
  url: data/notes.csv
mark: area
encoding:
  x:
    field: year
    type: temporal
    axis:
      format: %Y
      labelAngle: 0
      title: Year
      titleFontSize: 12
  y:
    aggregate: sum
    field: money
    type: quantitative
    axis:
      title: Notes in Circulation (Value ₹ Billions)
      titleFontSize: 12
  color:
    field: denom
    type: nominal

config:
  cell:
    width: 400
    height: 300
```
