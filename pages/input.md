# Input Binding 

This allows for two-way binding between Input types and Selection

```vis
data:
  url: data/cars.csv
selection:
  pts:
    type: single
    fields:
    - type
    bind: 
      input: select
      options: 
      - Hatchback
      - Sedan
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
