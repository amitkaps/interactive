# Brushing

Brushing allows us to select the an `interval` of area

**Interval / Brushing**

Select an interval by dragging the mouse

```vis
data:
  url: data/notes.csv
transform:
- filter: datum.year == 2015
selection:
  pts:
    type: interval
mark: circle
encoding:
  x:
    type: nominal
    field: denom
  y:
    type: quantitative
    field: number
  color:
    condition:
      selection: pts
      type: nominal
      field: denom
    value: grey
  size:
    value: 250
```
