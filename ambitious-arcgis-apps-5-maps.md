<!-- .slide: data-background-size="cover" style="padding-left: 80px" data-background="img/bg-1.png" -->

<h1 style="text-align: left; font-size: 2em;">Building Ambitious Applications Integrated with ArcGIS Online/Portal</h1>
<h2 style="text-align: left; font-size: 1.5em">Maps</h2>
    <p style="text-align: left; font-size: 1em;"><a href="https://github.com/tomwayson/">@tomwayson</a></p>
    <p style="text-align: left; font-size: 1em;">
      <a href="https://tomwayson.github.io/devsummit-2018/ambitious-arcgis-apps-5-maps.html" target="_blank">http://esriurl.com/ambAgsSlds5</a>
    </p>

---

<!-- .slide: data-background="img/bg-9.png" -->

  <h3>Follow Along</h3>
  <p>
    <a href="https://tomwayson.github.io/devsummit-2018/ambitious-arcgis-apps-5-maps.html" target="_blank">http://esriurl.com/ambAgsSlds5</a>
  </p>
  <p>
    <a href="https://github.com/tomwayson/devsummit-2018/ambitious-arcgis-apps-5-maps.html" target="_blank">@tomwayson/devsummit-2018</a>
  </p>

---

<!-- .slide: data-background="img/bg-7.png" -->

<h3>Esri's 2 JavaScript mapping libraries</h3>
<div style="width: 900px; margin: 0 auto; display: flex; justify-content: space-around">
  <div style="width: 450px">
    <a href="https://developers.arcgis.com/javascript/" target="_blank" style="color: #373288">
      <div><img src="img/esri.png" class="transparent" height="200" style="vertical-align: middle" /></div>
      <span>ArcGIS API for JavaScript</span>
    </a>
  </div>
  <div style="width: 450px">
    <a href="http://esri.github.io/esri-leaflet/" target="_blank" style="color: #949494">
      <div><img src="img/leaflet-logo.png" class="transparent" height="200" style="vertical-align: middle" /></div>
      <span>esri-leaflet</span>
    </a>
  </div>
</div>

---

<!-- .slide: data-background="img/shrug-2799746255_436723e65c_z.jpg" -->
   <h4>Which should you use?</h4>

---

<!-- .slide: data-background-color="#373288" -->
<img src="img/homepage-banner-sample.png" width="759" class="transparent">
<h3 style="font-size: 1.6em"><img src="img/esri.png" class="transparent" width="80" style="vertical-align: middle" /> 3D, geom engine, smartmapping</h3>

---

<!-- .slide: data-background-color="#373288" -->
<img src="img/homepage-banner-sample.png" width="759" class="transparent">
<h3 style="font-size: 1.6em"><img src="img/esri.png" class="transparent" width="80" style="vertical-align: middle" /> web maps, analysis services</h3>

---

<!-- .slide: data-background="img/phone-16981803257_4bcd3c45dc_z.jpg" -->
<h4><img src="img/leaflet-logo.png" class="transparent" width="80" style="vertical-align: middle" /> Lightweight / mobile friendly</h4>

---

<!-- .slide: data-background="img/bg-4.png" -->
<h3>esri-leaflet: framework friendly</h4>
<div>
  <img src="img/leaflet-logo.png" class="transparent" height="200" />
  <img src="img/Heart_corazon.svg" class="transparent" height="200" />
  <img src="img/angular.png" class="transparent" height="200" />
  <img src="img/tomster-sm.png" class="transparent" height="200" />
</div>

---

<!-- .slide: data-background="img/bg-4.png" -->
<h3>ArcGIS: challenge to load modules</h4>
<div>
  <img src="img/esri.png" class="transparent" height="200" />
  <img src="img/Broken_heart.svg" class="transparent" height="180" />
  <img src="img/angular.png" class="transparent" height="200" />
  <img src="img/tomster-sm.png" class="transparent" height="200" />
</div>
<p class="fragment"><code style="text-decoration: line-through">import Map from 'esri/Map';</code></p>

---

<!-- .slide: class="white" data-background="#f02541" -->
# Only way to load esri modules is with <a href="http://dojotoolkit.org/reference-guide/1.10/loader/" _target="blank">Dojo</a>

---

<!-- .slide: data-background="img/bg-3.png" -->
<h3><a href="https://developers.arcgis.com/javascript/latest/sample-code/widgets-frameworks-react/index.html?search=frameworks" target="_blank">4.x Samples</a> show framework <em>components</em> in ArcGIS apps</h3>
<div>
  <img src="img/esri.png" class="transparent" height="200" />
  <img src="img/Heart_corazon.svg" class="transparent" height="200" />
  <a href="https://developers.arcgis.com/javascript/latest/sample-code/widgets-frameworks-react/index.html" target="_blank"><img src="img/react-js-img.png" class="transparent" height="200" /></a>
  <a href="https://developers.arcgis.com/javascript/latest/sample-code/widgets-frameworks-vue/index.html" target="_blank"><img src="img/vue-logo.png" class="transparent" width="200" /></a>
</div>
<p><code>require(['vue','esri/Map'],(Vue, Map)=>{...})</code></p>

---

<!-- .slide: data-background="img/bg-3.png" -->
<h3>ArcGIS map in a React app?</h4>
<div>
  <img src="img/esri.png" class="transparent" height="100" />
  <img src="img/Broken_heart.svg" class="transparent" height="80" />
  <img src="img/react-js-img.png" class="transparent" height="100" />
  <img src="img/react-router-logo.png" class="transparent" width="200" />
  <img src="img/redux-logo.svg" class="transparent" height="100" />
</div>
<p class="fragment"><code style="text-decoration: line-through">import Map from 'esri/Map';</code></p>


---

<!-- .slide: data-background="img/bg-3.png" -->
<h3>Module loading <a href="https://github.com/Esri/jsapi-resources/tree/master/frameworks" target="_blank">solutions</a></h4>
<div>
  <img src="img/esri.png" class="transparent" height="120" />
  <img src="img/Broken_Love_Heart_bandaged_2_nevit.svg" class="transparent" height="100" />
  <img src="img/angular.png" class="transparent" height="120" />
  <img src="img/tomster-sm.png" class="transparent" height="120" />
  <img src="img/react-js-img.png" class="transparent" height="120" />
  <img src="img/vue-logo.png" class="transparent" height="120" />
</div>

---

<!-- .slide: data-background="img/bg-3.png" data-transition="fade" -->
<h3>One approach</h3>
<p>Configure webpack to skip:</p>
<p><code>import Map from 'esri/Map';</code></p>
<p>&nbsp;</p>

---

<!-- .slide: data-background="img/bg-3.png" data-transition="fade" -->
<h3>One approach</h3>
<p>Then output as app as AMD:
<p><code>require(['esri/Map'],(Map)=>{...})</code></p>
<p class="fragment">Load entire app w/ Dojo</a>

---

<!-- .slide: data-background="img/bg-3.png" data-transition="fade" -->
### Not ideal for:
<p>Framework CLIs or targeting mobile devices</p>
<img class="transparent" src="img/No_sign.svg" style="height: 200px; width: 200px; background-image: url(img/icons8-console.png); background-size: contain;">
<img class="transparent" src="img/No_sign.svg" style="height: 200px; width: 200px; background-image: url(img/icons8-multiple_smartphones.png); background-size: contain; margin-left: 200px">

---

<!-- .slide: data-background="img/bg-3.png" data-transition="fade" -->
### Better approach for those scenarios:

Use <a href="https://github.com/Esri/esri-loader" target="_blank">esri-loader</a>

<img class="transparent" src="img/icons8-console.png" style="height: 200px; width: 200px;">
<img class="transparent" src="img/icons8-good_quality.png" style="height: 200px; width: 200px;">
<img class="transparent" src="img/icons8-multiple_smartphones.png" style="height: 200px; width: 200px;">

---

<!-- .slide: data-background="img/bg-3.png" class="code-lg" -->
### Using <a href="https://github.com/Esri/esri-loader" target="_blank">esri-loader</a>:

```js
import { loadModules } from 'esri-loader'

loadModules([
  'esri/views/MapView',
  'esri/WebMap'
]).then(([MapView, WebMap]) => {
  // use MapView and WebMap as normal
})
```

---

<!-- .slide: data-background="img/shrug-2799746255_436723e65c_z.jpg" -->
  <h4>Which is right for _our_ use case?</h4>

---

<!-- .slide: data-background="img/bg-5.png" -->
### Advanced mapping capabilities?
<img src="img/homepage-banner-sample.png" height="200" class="transparent">

Not really...<span class="fragment"> but let's pretend</span>

---

<!-- .slide: data-background="img/bg-5.png" -->
### Framework: Ember
<img src="img/tomster-sm.png" class="transparent" height="200" />

<a href="https://github.com/Esri/jsapi-resources/tree/master/frameworks/ember" target="_blank">Lot's of resources</a>

---

<!-- .slide: data-background="img/bg-5.png" -->
### Two good choices
<img src="img/esri.png" class="transparent" height="200" />
<img src="img/Broken_Love_Heart_bandaged_2_nevit.svg" class="transparent" height="200" />
<img src="img/tomster-sm.png" class="transparent" height="200" />

<a href="https://github.com/Esri/ember-cli-amd" target="_blank">ember-cli-amd</a> and <a href="https://github.com/Esri/ember-esri-loader" target="_blank">ember-esri-loader</a>

---

<!-- .slide: data-background="img/bg-5.png" -->
### _Both_ work with CLI
<img src="img/esri.png" class="transparent" height="200" />
<img src="img/Broken_Love_Heart_bandaged_2_nevit.svg" class="transparent" height="200" />
<img src="img/Ember CLI on Light.png" class="transparent" height="200" />

---

<!-- .slide: data-background="img/bg-5.png" -->
### Targeting mobile?
<p class="fragment">Sure</p>

---

<!-- .slide: data-background="img/bg-5.png" -->
<h3>We'll use <a href="https://github.com/Esri/ember-esri-loader" target="_blank">ember-esri-loader</a></h4>
<div>
  <img src="img/esri.png" class="transparent" height="200" />
  <img src="img/Broken_Love_Heart_bandaged_2_nevit.svg" class="transparent" height="200" />
  <img src="img/tomster-sm.png" class="transparent" height="200" />
</div>

---

<!-- .slide: data-background="img/Backlit_keyboard.jpg" -->
  <h4>Let's <a href="https://github.com/mjuniper/ambitious-arcgis-app-2018/blob/master/workshop/5-maps.md" target="_blank">make a map!</a></h4>

---

<!-- .slide: data-background="img/bg-final.jpg" -->

<img class="transparent" src="img/esri-science-logo-white.png">
