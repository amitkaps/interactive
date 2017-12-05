# Select

Selection allows you to define the interaction using user inputs e.g. `click`, `dblclick`

**Single Selection**

Select single value using `click`

```vis
data:
  url: data/notes.csv
transform:
  - filter: datum.year == 2015
selection:
  pts:
    type: single
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

**Multiple Selection**

Select multiple value using `click` & `shift` + `click`

```vis
data:
  url: data/notes.csv
transform:
  - filter: datum.year == 2015
selection:
  pts:
    type: multi
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
