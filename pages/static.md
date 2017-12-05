# Static Visualisation

We will be using the notes dataset for the workshop today. This dataset was inspired by the demonetisation of INR 500 and INR 1000 notes in India conducted in 2016.

| year    | type   |  denom |  value |   money | number |
|--------:|:-------|-------:|-------:|--------:|-------:|
| 1977    | Notes  |   0001 |      1 |    2.72 |  2.720 |
| 1977    | Notes  |   1000 |   1000 |    0.55 |  0.001 |
| 1977    | Notes  |   0002 |      2 |    1.48 |  0.740 |
| 1977    | Notes  |   0050 |     50 |    9.95 |  0.199 |
| ...     | ...    |    ... |    ... |     ... |    ... |
| 2015    | Notes  |   0500 |    500 | 7853.75 | 15.708 |
| 2015    | Notes  |   0001 |      1 |    3.09 |  3.090 |
| 2015    | Notes  |   0010 |     10 |  320.15 | 32.015 |
| 2015    | Notes  |   1000 |   1000 | 6325.68 |  6.326 |

Metadata
- Filename: `notes.csv`
- Observations `(n)`: 351
- Features `(p)`    : 6
  - `year`  : The year of circulation
  - `type`  : The type of currency
  - `denom` : The denomination of the currency
  - `value` : The face value of the currency
  - `money` : The monetary value of currency in circulation (in INR Billion)
  - `number`: The number of currency in circulation (in INR Billion)
- Source: It is taken from Reserve Bank of India’s - Handbook of Statistics on Indian Economy 2016. Within it, Table 160 deals with [Notes and Coins in Circulation](https://www.rbi.org.in/scripts/PublicationsView.aspx?id=17293) and this dataset is only about the Notes circulation.

Lets make this static visualisation for this dataset.

```vis
width: 600
height: 400
title: Demonetisation Overview 
width: 600
height: 400
data:
  url: data/notes.csv
mark: area
encoding:
  x:
    field: year
    type: temporal
    axis:
      format: %Y
      labelAngle: 0
      title: Year
      titleFontSize: 12
  y:
    aggregate: sum
    field: money
    type: quantitative
    stack: normalize
    axis:
      title: Notes in Circulation (Value ₹ Billions)
      titleFontSize: 12
  color:
    field: denom
    type: nominal
```
