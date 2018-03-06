<!-- .slide: data-background-size="cover" style="padding-left: 80px" data-background="img/bg-1.png" -->

<h1 style="text-align: left; font-size: 2em;">Using ArcGIS REST JS</h1>
<h2 style="text-align: left; font-size: 1.5em;">and the ArcGIS REST APIs</h2>
  <p style="text-align: left; font-size: .5em;">John Gravois
  <a href="https://github.com/jgravois" target="_blank">@jgravois</a></p>
  <p style="text-align: left; font-size: .5em;">Dave Bouwman
  <a href="https://github.com/dbouwman" target="_blank">@dbouwman</a></p>
  <p style="text-align: left; font-size: .5em;">Tom Wayson
  <a href="https://github.com/tomwayson/" target="_blank">@tomwayson</a></p>
  <p style="font-size: 1em;">slides: <a href="http://bit.ly/2FlTihi">http://bit.ly/2FlTihi</a>

---

<!-- .slide: data-background="img/bg-2.png" -->

## Agenda

1. Prior art
1. Getting&nbsp;started
1. Use cases
1. Demos (lots!)

---

<!-- .slide: data-background="img/bg-3.png" -->

* https://github.com/Esri/arcgis-rest-js
* https://esri.github.io/arcgis-rest-js

<aside class="notes">
  * collaboration between ArcGIS Hub and developers.arcgis.com teams
  * shoutout to Patrick Arlt and Noah Mulfinger
  * shoutout to Ian WA Fish and Game, and Jeff from WA DOT 
</aside>

---

<!-- .slide: data-background="img/bg-3.png" -->

```
npm install @esri/arcgis-rest-request
```
Disclaimer*

<aside class="notes">
  * not a product, no roadmap
  * work in progress
  * scratching our own itch
</aside>

---

<!-- .slide: data-background="img/bg-4.png" -->

### If at first you don't succeed...

---

<!-- .slide: data-background="img/bg-4.png" -->

* github.com/Esri/geoservices-js
* github.com/Esri/node-arcgis
* `XMLHttpRequest` in _lots_ of apps

<aside class="notes">
  * we've been down this road before
  * geoservices, node-arcgis, etc.
  * one off implementations of XMLHttpRequest in apps
</aside>

---

<!-- .slide: data-background="img/bg-5.png" -->

### Goals

* Node.js **and** (modern) browsers
* a la carte
* framework agnostic
* shave down the sharp edges

<aside class="notes">
  
</aside>

---

<!-- .slide: data-background="img/bg-5.png" -->

### Comparison

* _kind of_ analogous to ArcGIS API for Python
* much different than the ArcGIS API for JavaScript

<aside class="notes">
  thin wrapper, web centric
  pairs well with other open source libraries
</aside>

---

<!-- .slide: data-background="img/bg-6.png" -->

* `request` - 2kb
* `feature-service` - 500 bytes
* `auth` - 2.5kb
* `groups` - 750 bytes
* `geocoder` - 1kb
* `items` - 1kb

<aside class="notes">
  compact
  compact because they are *far* from complete
</aside>
