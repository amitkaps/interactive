# Visdown

**Make visualisations using only markdown**

Write visualisation using a simple declarative markup like you would write code. Just wrap it in fenced block (three backticks) and mark the language as `vis`.

*Make simple static visualisations*

```vis
data:
  url: data/cars.csv
transform:
- filter: datum.kmpl > 20
mark: point
encoding: 
  x: 
    field: kmpl
    type: quantitative
  y: 
    field: price
    type: quantitative
```

Visdown is based on the grammar of interactive graphic (vega-lite) which allows you to specify the visualisation including interactions in a declarative fashion.

*Make interactive visualisations*

Select the circles with the mouse

```vis
data(cars.csv) | point(x=kmpl:Q, y=price:Q, color=bhp:Q)
```
