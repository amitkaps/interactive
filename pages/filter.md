# Filter

It is possible to apply a filter to the dataset to get a smaller subset. 

We can refer to any field using the bound term `datum`. For example, setting filter to `datum.b2 > 60` would make the output data includes only items that have values in the field b2 over 60.

For example, let us filter the notes data for denominations greater than INR 10.

```vis
data:
  url: data/notes.csv 
transform:
- filter: datum.value > 10
mark: line 
encoding: 
  x: 
    field: year
    type: temporal
  y: 
    field: money
    type: quantitative
  color:
    field: denom
    type: nominal 
```
