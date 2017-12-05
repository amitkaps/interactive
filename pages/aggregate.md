# Aggregate

You can aggregate on a particular variable to do basic statistical operations like mean, sum, quantile etc.

```vis
width: 600
data:
  url: data/notes.csv
mark: area
encoding:
  x:
    field: year
    type: temporal
  y:
    aggregate: sum
    field: money
    type: quantitative
  color:
    field: denom
    type: nominal
```

### Binning

Binning is a technique for grouping quantitative, continuous data values of a particular field into smaller number of “bins”

You can bin directly in the encoding field which is a shorter option.

```vis
data: 
  url: data/notes.csv 
transform:
- filter: datum.value == 1000
mark: bar
encoding: 
  x: 
    field: money
    type: ordinal
    bin: true
  y: 
    aggregate: count
    type: quantitative
  color:
    field: denom
    type: nominal
```
