<!-- .slide: data-background="img/bg-7.png" -->

## Geocoding

```
npm install @esri/arcgis-rest-request && npm install @esri/arcgis-rest-geocoder
```
```js
import { geocode } from '@esri/arcgis-rest-geocoder';

geocode("LAX")
  .then((response) => {
    response.candidates[0].location;
    // { x: -118.409, y: 33.943, spatialReference: { wkid: 4326 }  }
  });
```

<aside class="notes">
  * Promise based
  * prioritizes simple use cases
  * try to avoid unnecessary GIS jargon
</aside>

---

<!-- .slide: data-background="img/bg-7.png" -->

## Reverse Geocoding

```js
import { reverseGeocode } from '@esri/arcgis-rest-geocoder';

// long, lat
reverseGeocode([ -118.409,33.943 ])
  .then((response) => {
    response.address.PlaceName; // => "LA Airport"
  });

// or
reverseGeocode({ latitude: 33.943, latitude: -118.409 })
reverseGeocode({ x: -118.409, y: 33.9425 }) // wgs84 is assumed
reverseGeocode({ x: -13181226, y: 4021085, spatialReference: { wkid: 3857 })
```

<aside class="notes">
  * overloaded constructor
</aside>

---

<!-- .slide: data-background="img/bg-8.png" -->

## Suggestions

```js
<!-- require polyfills for fetch and Promise from https://polyfill.io -->
<script src="https://cdn.polyfill.io/v2/polyfill.js?features=es5,Promise,fetch"></script>

<script src="https://unpkg.com/@esri/arcgis-rest-request@1.1.1"></script>
<script src="https://unpkg.com/@esri/arcgis-rest-geocoder@1.1.1"></script>

arcgisRest.suggest("Starb")
  .then((response) => {
    response.address.PlaceName; // => "Starbucks"
  });

```

<aside class="notes">
  * arcgisRest namespace
  * method names reflect that
</aside>

---

<!-- .slide: data-background="img/bg-9.png" -->

## Suggestions

```js
arcgisRest.suggest("Disneyl", {
  httpMethod: "POST",
  params: {
    countryCode: "FR",
    maxSuggestions: 2
  }
})
  .then((response) => {
    console.log(response.suggestions.length); // => 2 (in France)
  });
```

<aside class="notes">
  * second optional parameter
  * other methods that need two pieces of information expect it via a single object
</aside>

---

<!-- .slide: data-background="img/bg-2.png" -->

## Prior art

https://www.npmjs.com/package/geocoder-arcgis

---

<!-- .slide: data-background="img/bg-3.png" -->

## Demo ([Batch geocoding](https://github.com/Esri/arcgis-rest-js/blob/509afd71425daa7401c8c0cf6a5eb5b1958985b6/demos/batch-geocoder-node/batch-geocode.js#L79-L82) in Node.js)