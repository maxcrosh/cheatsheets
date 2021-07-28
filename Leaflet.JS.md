### Get started with Leaflet maps
https://leafletjs.com/examples/quick-start/

#### 1. Copy code to index.html
```html
<html>
    <head>
        <title>Leaflet map example</title>

        <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
        integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
        crossorigin=""/>

        <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
        integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
        crossorigin=""></script>

        <style>
            html, body, #mapid {
                height: 100vh;
                width: 100vw;
                margin: 0px;
            }
        </style>
    </head>
    <body>
        <div id="mapid"></div>
        <script>
            const mymap = L.map('mapid').setView([51.505, 39], 4);

            L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
                maxZoom: 19,
                attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
            }).addTo(mymap);
        </script>
    </body>
</html>
```

#### 2. Open file in a browser
