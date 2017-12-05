# Pan & Zoom

By binding scales, it is possible to Pan & Zoom the visualisation.

```vis
data:
  url: data/cars.csv
selection:
  pts:
    type: interval
    bind: scales
mark: circle
encoding:
  x:
    type: quantitative
    field: kmpl
    scale:
     domain: [12,25]
  y:
    type: quantitative
    field: price
    scale:
     domain: [100,900]
  color:
    condition:
      selection: pts
      field: type
      type: nominal
    value: grey
  size:
    value: 200
width: 450
height: 300
```

**Nearest**

Select nearest value using `hover`


```vis
data:
  url: data/cars.csv
selection:
  pts:
    type: single
    on: mouseover
    nearest: true
mark: circle
encoding:
  x:
    type: quantitative
    field: kmpl
    scale:
     domain: [12,25]
  y:
    type: quantitative
    field: price
    scale:
     domain: [100,900]
  color:
    condition:
      selection: pts
      field: type
      type: nominal
    value: grey
  size:
    value: 200
width: 450
height: 300
```

**Multi Line Highlight**

```vis
width: 500
height: 300
data:
  url: data/notes.csv
config:
  point:
    opacity: 0
layer:
- selection:
    highlight:
      type: single
      'on': mouseover
      nearest: 'true'
      fields:
      - denom
  mark: point
  encoding:
    x:
      field: year
      type: temporal
      axis:
        format: "%Y"
        labelAngle: 0
    y:
      field: number
      type: quantitative
    color:
      field: denom
      type: nominal
- mark: line
  encoding:
    x:
      field: year
      type: temporal
      axis: 
    y:
      field: number
      type: quantitative
    color:
      field: denom
      type: nominal
    size:
      condition:
        selection:
          not: highlight
        value: 1
      value: 3
```
