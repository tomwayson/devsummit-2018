<!-- .slide: data-background="img/bg-4.png" -->

## Geocoding

```js

import { geocode } from '@esri/arcgis-geocoder';

geocode("LAX")
  .then((response) => {
    response.candidates[0].location;
    // { x: -118.409, y: 33.943, spatialReference: { wkid: 4326 }  }
  });
```

---

## Reverse Geocoding

```js
import { reverseGeocode } from '@esri/arcgis-geocoder';

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

---

## Suggestions

```js
<!-- require polyfills for fetch and Promise from https://polyfill.io -->
<script src="https://cdn.polyfill.io/v2/polyfill.js?features=es5,Promise,fetch"></script>

<script src="https://unpkg.com/@esri/arcgis-rest-request@1.1.1"></script>
<script src="https://unpkg.com/@esri/arcgis-rest-request@1.1.1"></script>

arcgisRest.suggest("Starb")
  .then((response) => {
    response.address.PlaceName; // => "Starbucks"
  });

```

---

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

---

## Prior art

https://www.npmjs.com/package/geocoder-arcgis


## Demo