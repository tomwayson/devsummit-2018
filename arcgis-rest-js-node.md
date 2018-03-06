<!-- .slide: data-background="img/bg-7.png" -->

## Node

- can be used in node servers (express, hapi, etc)
- and command-line tools

---

<!-- .slide: data-background="img/bg-9.png" -->

## Node
```js
// need fetch and form-data
require('isomorphic-fetch');
require('isomorphic-form-data');
// bring in modules you need...
const { searchItems } = require("@esri/arcgis-rest-items");
return searchItems({
    searchForm: {
      q: 'bike trails',
      start: 1,
      num: 100
    }
  })
  .then((results) => {
    // work with the items...
  })
```

---

<!-- .slide: data-background="img/bg-9.png" -->

## Demo

- Bulk Geocoder
  - configure input, output, field mappings
  - good if you have a repeated process
as
- command-line toolkit
  - build with `commander`
  - easy to add more cli tools
