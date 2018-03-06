<!-- .slide: data-background="img/bg-5.png" -->

## Feature Services

---

<!-- .slide: data-background="img/bg-5.png" -->

### Use Case: [Hub Open Dataset Attribute Charts ](http://hub.arcgis.com/datasets/dfdaef8ca5ff4a0fb014abecb7d6615e_8)

<img src="img/hub-dataset-attribute-chart-screenshot.png" width="860" />

---

<!-- .slide: data-background="img/bg-5.png" -->

### Use Case: [Hub Open Dataset Attribute Charts ](http://hub.arcgis.com/datasets/dfdaef8ca5ff4a0fb014abecb7d6615e_8)

Field stats cached ahead of time by a node process

<div style="width: 870px; display: flex; justify-content: space-between; margin: 0 auto;">
<pre style="width: 425px; margin: 0; box-shadow: none;"><code class="hljs json" style="height: 412px;">"statistics": {
  "values": [
    {
      "value": "Yes",
      "count": 199,
      "code": "Y"
    },
    {
      "value": "No",
      "count": 99,
      "code": "N"
    }
  ],
  "count": 2
}</code></pre>
<img src="img/hub-dataset-attribute-chart.png" style="width: 425px; height: 412px; margin: 0">
</div>

Note:
[cedar](http://cedar-v1.surge.sh/) charts not always used in the context of a map

---

<!-- .slide: data-background="img/bg-5.png" -->

### [@esri/arcgis-rest-feature-service](https://esri.github.io/arcgis-rest-js/api/feature-service/)

<ul>
<li class="fragment">currently "read-only"</li>
<li class="fragment">[plan to add CRUD, info, & admin functions](https://github.com/Esri/arcgis-rest-js/issues/46)</li>
</ul>

Note:
- newly released, in a fit of conference driven development

---

<!-- .slide: data-background="img/bg-5.png" -->

### Get Feature

```js
import { getFeature } from '@esri/arcgis-rest-feature-service';

const featureLayerUrl = 'https://services.arcgis.com/V6ZHFr6zdgNZuVG0/arcgis/rest/services/Landscape_Trees/FeatureServer/0';

getFeature({ url: featureLayerUrl, id: 42 })
  .then(response => {
    response.attributes.FID; // 42
  });
```

---

<!-- .slide: data-background="img/bg-5.png" -->

### Query Features

```js
import { queryFeatures } from '@esri/arcgis-rest-feature-service';

const featureLayerUrl = 'https://services.arcgis.com/V6ZHFr6zdgNZuVG0/arcgis/rest/services/Landscape_Trees/FeatureServer/0';
const queryParams = {
  where: 'Condition='Poor'',
  returnCountOnly: true
}

queryFeatures({ url: featureLayerUrl, params: queryParams })
  .then(response => {
    response.count; // 7
  });
```

---

<!-- .slide: data-background="img/bg-9.png" -->

## Demo

[demos/feature-service-browser](https://github.com/Esri/arcgis-rest-js/tree/master/demos/feature-service-browser)
