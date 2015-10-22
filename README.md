# minicensus

A convenient JSON representation of the 2011 South African census data.
The data is organised hierarchically: country, province, district, municipality, ward. 

Structure:
```
{
  "tables": { //Data table definitions
    "table name": ["col 1 label", "col 2 label", ...],
    ...
  },
  "ZA": { //South African geographical division hierarchy with census data
    "code": "ZA"
    "name": "South Africa",
    "geo": {
      "bbox":[2.20003, -1.76001, 2.78003, -1.59002], //Min and max geo points
      "points": [[2.20003, -1.76001], [2.78003, -1.59002], ...] //Geo polygon
    },
    "data": {
      "table name": ["col 1 value", "col 2 value", ...],
      ...
    },
    "children": {
      "GT": {
        //Same structure as parent
      },
      ...
    }
  }
}

```
