# Calculate

This allows you to derive a new field using a calculation on an existing cell.

```
transform: 
  calculate:
  as: 
```

Lets derive a new value of `money` in the notes dataset by converting it to milions.

```vis
data:
  url: data/notes.csv 
transform:
- calculate: datum.money * 1000 
  as: moneyMillion
mark: line 
encoding: 
  x: 
    field: year
    type: temporal
  y: 
    field: moneyMillion
    type: quantitative
  color:
    field: denom
    type: nominal
```
