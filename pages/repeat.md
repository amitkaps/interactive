# Repeat

This allows us to generate multiple plots like facet. However, unlike facet it allows full replication of a data set in each view.

```vis
data:
  url: data/notes.csv
transform:
- filter: datum.year == 2015
repeat:
  column: 
    - money
    - number
spec: 
  mark: bar
  encoding:
    x:
      type: nominal
      field: denom
    y:
      type: quantitative
      field: 
        repeat: column
    color:
      type: nominal
      field: denom
```
