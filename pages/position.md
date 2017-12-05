# Position

This identifies how the marks are going to be positioned on the X and Y Encoding.

- **Identity**
- **Stacked**
- **Normalise**
- **Jitter** *// Not Supported*

To stack the values, we can use `aggregate` as `sum`, which by default will stack them.

```vis
data:
  url: "data/notes.csv"
mark: area
encoding:
  x:
    type: temporal
    field: year
  y:
    type: quantitative
    field: money
    aggregate: sum
  color:
    type: nominal
    field: denom
```

To normalize the values, we can add the `stack` as `normalize` to the field.

```vis
data:
  url: "data/notes.csv"
mark: area
encoding:
  x:
    type: temporal
    field: year
  y:
    type: quantitative
    field: money
    aggregate: sum
    stack: normalize
  color:
    type: nominal
    field: denom
```
