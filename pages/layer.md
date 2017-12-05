# Layers

Layering allows us to add multiple layers of visual representation. Here we layer a bar chart and circle chart to create a lollipop chart.

**Single View #1- Bar Chart**

```vis
data:
  url: data/notes.csv
transform:
  - filter: datum.year == 2015
mark: bar
encoding:
  y:
    type: nominal
    field: denom
  x:
    type: quantitative
    field: number
  color:
    type: nominal
    field: denom
  size:
    value: 3
```

**Single View #2 - Circle Chart**


```vis
data:
  url: data/notes.csv
transform:
  - filter: datum.year == 2015
mark: circle
encoding:
  y:
    type: nominal
    field: denom
  x:
    type: quantitative
    field: number
  color:
    type: nominal
    field: denom
  size:
    value: 100
    
```

## Layered View - Lollipop Chart

```vis
data:
  url: data/notes.csv
transform:
- filter: datum.year == 2015
layer:
- mark: bar
  encoding:
    y:
      type: nominal
      field: denom
    x:
      type: quantitative
      field: number
    color:
      type: nominal
      field: denom
    size:
      value: 2
- mark: circle
  encoding:
    y:
      type: nominal
      field: denom
    x:
      type: quantitative
      field: number
    color:
      type: nominal
      field: denom
    size:
      value: 100      

```
