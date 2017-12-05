# Encoding

These are the channel properties used to set the position and appearance of the mark

- Position x
- Position y
- Color
- Shape
- Size


Change the `fields` in `x` ,`y`, `shape`, `size` and `color`

```vis
data:
  url: "data/notes.csv"
transform:
  -
    filter: datum.year > 2010
mark: circle
encoding:
  x:
    type: quantitative
    field: money
  y:
    type: quantitative
    field: number
  color:
    type: nominal
    field: denom
  size:
    type: quantitative
    field: value
```
