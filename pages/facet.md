# Facet

We can also create small multiple charts using `row` or `column` encoding

- Row wise
- Column wise

```vis
data:
  url: "data/notes.csv"
transform:
- filter: datum.denom > 30
mark: area
encoding:
  x:
    type: temporal
    field: year
  y:
    type: quantitative
    field: money
  color:
    type: nominal
    field: denom
  column:
    type: nominal
    field: denom
```
