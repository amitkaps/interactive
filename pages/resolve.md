# Resolve 

Resolve allows us to layering charts with different scales, guides and legends.

**First Layer**

```vis
width: 400
height: 300
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
  y:
    aggregate: sum
    field: money
    type: quantitative
    stack: normalize
    axis:
      format: %
  color:
    field: denom
    type: nominal
```

**Second Layer**

```vis
width: 400
height: 300
data:
  url: data/notes.csv
mark: line
encoding:
  x:
    field: year
    type: temporal
    axis:
      format: %Y
      labelAngle: 0
  y:
    aggregate: sum
    field: number
    type: quantitative
  size:
    value: 3
  color:
    value: black

```

**Combined**

```vis
width: 400
height: 300
data:
  url: data/notes.csv
layer:
- mark: area
  encoding:
    x:
      field: year
      type: temporal
      axis:
        format: %Y
        labelAngle: 0
    y:
      aggregate: sum
      field: money
      type: quantitative
      stack: normalize
      axis:
        format: %
    color:
      field: denom
      type: nominal
- mark: line
  encoding:
    x:
      field: year
      type: temporal
      axis:
        format: %Y
        labelAngle: 0
    y:
      aggregate: sum
      field: number
      type: quantitative
    size:
      value: 3
    color:
      value: black
resolve:
  scale:
    y: independent
```
