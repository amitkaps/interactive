# Mark

Mark are the basic shapes used to represent the data. You can change the `mark` to `point`, `circle`, `square`, `text`, `tick`, `bar`, `line`, and `area`.


```vis
data:
  url: data/notes.csv
mark: line
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
```
