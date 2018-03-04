<!-- .slide: data-background-size="cover" style="padding-left: 80px" data-background="img/bg-1.png" -->

<h1 style="text-align: left; font-size: 2em;">Building Ambitious Applications Integrated with ArcGIS Online/Portal</h1>
<h2 style="text-align: left; font-size: 1.5em">Ember Addons</h2>
    <p style="text-align: left; font-size: 1em;"><a href="https://github.com/tomwayson/">@tomwayson</a></p>

---

<!-- .slide: data-background="img/bg-9.png" -->

  <!-- TODO: upate links -->
  <h3>Follow Along</h3>
  <p>
    <a href="http://tomwayson.github.io/dev-summit-2017-ambitious-arcgis-workshop" target="_blank">goo.gl/OYgA4q</a>
  </p>
  <p>
    <a href="https://github.com/tomwayson/devsummit-2018/ambitious-arcgis-apps-3-addons.html" target="_blank">@tomwayson/devsummit-2018</a>
  </p>

---

<!-- .slide: data-background="img/web.ns_.studentgamers.JHu_.DA_-640x519.jpg" -->
  <h4>Other people's code</h4>

---

<!-- .slide: data-background="img/fast-sport-car-1466168836N0A.jpg" -->
  <h4>Turbocharge your development?</h4>

---

<!-- .slide: data-background="img/rusted-1246518_1920.jpg" -->
  <h4>More trouble than it's worth?</h4>

---

<!-- .slide: data-background="img/rusted-1817343_1920.jpg" -->
  <h4>Total disaster?</h4>

---

<!-- .slide: data-background="img/bg-7.png" -->
<img src="img/bootstrap4-solid.svg" class="transparent" height="300" />
<h3 class="fragment"><span class="fragment">✔</span>CSS + JavaScript<span class="fragment">?</span></h3>

Note:
- bootstrap as a case study
- should be a no brainer
- we already have CSS
- how to get JS

---

<!-- .slide: data-background="img/bg-7.png" data-transition="fade" -->
  <img src="img/bootstrap4-solid.svg" class="transparent" height="300" />
  <img class="transparent" src="img/jquery_bumper.sh-600x600.png" height="300">

Note:
- JS implemented as jQuery plugin

---

<!-- .slide: data-background="img/bg-7.png" data-transition="fade" -->
  <img src="img/bootstrap4-solid.svg" class="transparent" height="300" />
  <img class="transparent" src="img/No_sign.svg" style="height: 300px; width: 300px; background-image: url(img/jquery_bumper.sh-600x600.png); background-size: contain;">

Note:
- most frameworks no jQuery
- should no manipulate DOM w/ jQuery
- use framework's components instead

---

<!-- .slide: data-background="img/bg-7.png" -->
  <img src="img/bootstrap4-solid.svg" class="transparent" height="200" />
  <img src="img/tomster-sm.png" class="transparent" height="206" />

  <img src="img/bootstrap4-solid.svg" class="transparent" height="200" />
  <img src="img/react-js-img.png" class="transparent" height="206" />
  <img src="img/bootstrap4-solid.svg" class="transparent" height="200" style="margin-left: 20px" />
  <img src="img/vue-logo.png" class="transparent" height="206" />

  <span class="fragment"><img src="img/bootstrap4-solid.svg" class="transparent" height="200" />
  <img src="img/ngx-bootstrap.svg" class="transparent" height="200" /></span>
  <img src="img/bootstrap4-solid.svg" class="transparent" height="200" style="margin-left: 20px" />
  <a href="https://github.com/gdi2290/awesome-angular" target="_blank"><img src="img/angular.png" class="transparent" height="206" /></a>
  <span class="fragment"><img src="img/bootstrap4-solid.svg" class="transparent" height="200" style="margin-left: 20px" />
  <img src="img/ng-bootstrap-logo.svg" class="transparent" height="200" /></span>

---

<!-- .slide: data-background="img/7658225516_b327a08733_k.jpg" -->
  <h4>Time to install and configure</h4>

---

<!-- .slide: data-background="img/bg-4.png" data-transition="fade" -->
<img class="transparent" src="img/800px-Npm-logo.svg.png" style="width: 300px; margin: 110px 0;">
<h3><code>npm install some-bootstrap-lib</code></h3>

Note:
- easier than ever

---

<!-- .slide: data-background="img/bg-4.png" data-transition="fade" -->
<img class="transparent" src="img/yarn-cat-eating-bower-bird.png">
<h3><code>yarn add some-bootstrap-lib</code></h3>

---

<!-- .slide: data-background="img/bg-4.png" data-transition="fade" class="code-lg" -->

```js
  // some-bootstrap-lib's package.json
  "main": "dist/node/index.js",
  "browser": "dist/umd/index.js",
  "module": "dist/esm/index.js",
  "js:next": "dist/esm/index.js",
  "types": "dist/esm/index.d.ts",
```

Note:
- well written libs will tell build tools where to find JS files

---

<!-- .slide: data-background="img/bg-4.png" -->

<div style="width: 50%; margin: 0 auto; display: flex; justify-content: space-around; align-items: center;">
  <img class="transparent" src="img/CSS3_logo_and_wordmark.svg" style="height: 300px">
  <span style="font-size: 2em">or</span>
  <img class="transparent" src="img/sass-logo.png" style="height: 300px">
</div>

Note:
on your own for other assets like styles, images

---

<!-- .slide: data-background="img/bg-4.png" -->
## What if this were easier?

---

<!-- .slide: data-background-color="#faf4f1" class="ember-brand" -->
  <h3>Ember Addons</h3>
  <img src="img/Ember CLI on Light.png" class="transparent" />
  <p>A plugin system for <a href="https://ember-cli.com/extending/" target="_blank">ember-cli</a></p>

Note:
- more than just runtime JS, CSS, components, etc

---

<!-- .slide: data-background="img/1280px-Tesla_auto_bots.jpg" data-transition="fade" -->
  <h4>Automate install and build steps</h4>

Note:
- includes node code to ^^^

---

<!-- .slide: data-background="img/1280px-Tesla_auto_bots.jpg" data-transition="fade" -->
  <h4><code>ember install some-addon</code></h4>

Note:
- Problem: someone has to write them

---

<!-- .slide: data-background="img/1280px-Tesla_auto_bots.jpg" data-transition="fade" -->
<h4><code>ember addon my-new-addon</code></h4>

Note:
- Ember goal: easy to author high qaulity addons
- Won't go into details,
- 2 things you should know

---

<!-- .slide: data-background="img/1280px-Tesla_auto_bots.jpg" data-transition="fade" -->
<h4>Scaffold addon <em>and</em> dummy app</h4>

Note:
Easy for author to:
- verify addon works
- demo/document behavior

---

<!-- .slide: data-background="img/release-tomsters.png" data-background-color="#faf4f1" class="ember-brand" -->
  <h4>Tests run in many ember versions</h4>

Note:
by default:
- recent stable versions
- future beta/canary versions

---

<!-- .slide: data-background="img/17517769750_2757bafdf9_k.jpg"  data-transition="fade" -->

Note:
what this means for you:
- generally Ember addons are good quality

---

<!-- .slide: data-background-color="#faf4f1" class="ember-brand" -->
  <h3>Add bootstrap to an Ember app</h3>
    <img src="img/tomster-sm.png" class="transparent" height="300" />
    <img src="img/bootstrap4-solid.svg" class="transparent" height="300" />
  <p>Start at <a href="https://www.emberaddons.com/?query=bootstrap" target="_blank">emberaddons.com</a></p>

---

<!-- .slide: data-background-color="#faf4f1" class="ember-brand" -->
  <h3>Over a dozen <a href="https://www.emberaddons.com/?query=arcgis" target="_blank">ArcGIS addons</a></h3>
  <a href="https://www.emberaddons.com/?query=arcgis" target="_blank">
    <img src="img/tomster-sm.png" class="transparent" height="300" />
    <img src="img/esri.png" class="transparent" height="300" />
  </a>

---

<!-- .slide: data-background="img/Backlit_keyboard.jpg" -->
  <h4>Let's <a href="https://github.com/mjuniper/ambitious-arcgis-app-2018/blob/master/workshop/3-addons.md" target="_blank">add some addons!</a></h4>

---

<!-- .slide: data-background="img/bg-final.jpg" -->

<img class="transparent" src="img/esri-science-logo-white.png">
