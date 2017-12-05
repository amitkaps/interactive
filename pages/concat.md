# Concat

We can concat different charts together horizontally or vertically

- **hconcat**: Horizontal concatenation
- **vconcat**: Vertical concatenation

```vis
hconcat:
- data:
    url: data/notes.csv
  transform:
    - filter: datum.year == 2015  
  mark: bar
  encoding:
    x:
      type: nominal
      field: denom
    y:
      type: quantitative
      field: number
    color:
      type: nominal
      field: denom
- data:
    url: data/notes.csv
  transform:
      - filter: datum.year == 2015  
  mark: circle
  encoding:
    x:
      type: nominal
      field: denom
    y:
      type: quantitative
      field: number
    color:
      type: nominal
      field: denom
    size:
      value: 100

```
