<!-- .slide: data-background="img/bg-7.png" -->

### Item Search

### searchItems( string or options )

```js
const { searchItems } = require("@esri/arcgis-rest-items");
return searchItems('water')
  .then((results) => {
    // work with the items...
  })
```

---

<!-- .slide: data-background="img/bg-7.png" -->

### it's just q

```js
const { searchItems } = require("@esri/arcgis-rest-items");
return searchItems('water AND type: Web Map')
  .then((results) => {
    // work with the items...
  })
```

---

<!-- .slide: data-background="img/bg-7.png" -->

### Paging...

```js
const { searchItems } = require("@esri/arcgis-rest-items");
return searchItems({
    searchForm: {
      q: 'bike trails AND (typekeywords: hubSolutionTemplate)',
      start: 1203,
      num: 100
    }
  })
  .then((results) => {
    // work with the items...
  })
```

---

<!-- .slide: data-background="img/bg-7.png" -->

### Private Items on your Portal

```js
return searchItems({
    authentication: myUserSession,
    portal: 'https://my-portal.org/sharing/rest',
    searchForm: {
      q: 'bike trails AND (typekeywords: hubSolutionTemplate)',
      start: 1203,
      num: 100,
    }
  })
  .then((results) => {
    // work with the items...
  })
```


---

<!-- .slide: data-background="img/bg-7.png" -->

### CRUD
- `createItem`
- `getItem`
- `updateItem`
- `removeItem`

---


<!-- .slide: data-background="img/bg-7.png" -->

### Other Item-y Things
- `addItemJson`
- `createItemInFolder`
- `getItemData`
- `getItemResources`

---

<!-- .slide: data-background="img/bg-7.png" -->

### Resources & Protection

- `getItemResources`
- `updateItemResource`*
- `removeItemResource`*
- `protectItem`
- `unprotectItem`

---


<!-- .slide: data-background="img/bg-7.png" -->

### Groups

- `searchGroups`
- `createGroup`
- `getGroup`
- `updateGroup`
- `removeGroup`

---

<!-- .slide: data-background="img/bg-7.png" -->

### Groups


- `getGroupContent`
- `getGroupUsers`
- `protectGroup`
- `unprotectGroup`


---

<!-- .slide: data-background="img/bg-9.png" -->

### Node
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

### Demo

- CLI toolkit
  - build with `commander`
  - easy to add more cli tools
- Hub Cleaner
  - surgical purge for our test org
