### Get started with HERE JavaScript Maps API
https://developer.here.com/documentation/examples/maps-js

#### 1. Copy code to `index.html`
```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <meta http-equiv="Content-type" content="text/html;charset=UTF-8">
    
    <title>Map at a specified location</title>
    <link rel="stylesheet" type="text/css" href="https://js.api.here.com/v3/3.1/mapsjs-ui.css" />   
    <script type="text/javascript" src="https://js.api.here.com/v3/3.1/mapsjs-core.js"></script>
    <script type="text/javascript" src="https://js.api.here.com/v3/3.1/mapsjs-service.js"></script>
    <script type="text/javascript" src="https://js.api.here.com/v3/3.1/mapsjs-ui.js"></script>
    <script type="text/javascript" src="https://js.api.here.com/v3/3.1/mapsjs-mapevents.js"></script>
    
    <style>
      html, body, #map {
        height: 100vh;
        width: 100vw;
        margin: 0px;
      }
    </style>
  </head>
  <body>
    <div id="map"></div>
    <script type="text/javascript"></script>
  </body>
```

#### 2. Copy javascript code into `<script>...</script>`
```javascript
var platform = new H.service.Platform({
  apikey: YOUR_APIKEY
});

var defaultLayers = platform.createDefaultLayers();

var map = new H.Map(document.getElementById('map'),
  defaultLayers.vector.normal.map,{
  center: {lat:50, lng:5},
  zoom: 4,
  pixelRatio: window.devicePixelRatio || 1
});

window.addEventListener('resize', () => map.getViewPort().resize());

var behavior = new H.mapevents.Behavior(new H.mapevents.MapEvents(map));
var ui = H.ui.UI.createDefault(map, defaultLayers);
```

#### 3. Open `index.html` in browser
