### Get started with Folium with HERE REST API
http://python-visualization.github.io/folium/

#### 1. Import libraries
```python
import requests
import folium
```

#### 2. Initialize access key to external API and basemap
```python
API_KEY = "YOUR_API_KEY" // Get credentials on https://developer.here.com
basmap = f"https://1.base.maps.ls.hereapi.com/maptile/2.1/maptile/newest/normal.day/11/525/761/256/png8?apiKey={API_KEY}"
```

#### 3. Create map with custom basemap
```python
m = folium.Map(
      location=[55.7477, 37.62189], 
      zoom_start=10,
      tiles=basemap,
      attr='HERE'
  )
```

#### 4. Interface to get Weather data
```python
def getWeather(lat, lon, apiKey):
  """
  Get weather by coordinates.
  Weather API docs: 
  https://developer.here.com/documentation/examples/rest/auto_weather/weather-observation-lat-long
  """

  weather_url = "https://weather.ls.hereapi.com/weather/1.0/report.json"

  params = {
      "product": "observation",
      "latitude": lat,
      "longitude": lon,
      "oneobservation": "true",
      "apiKey": apiKey,
  }

  response = requests.get(weather_url, params=params).json()
  temperature = response['observations']['location'][0]['observation'][0]['temperature']
  
  return { "lat": lat, "lon": lon, "temp": temperature }
```

#### 4. Add marker with weather data
```python
markerData = getWeather(55.7477, 37.62189, API_KEY)

marker = folium.Marker(
            location=[ markerData['lat'], markerData['lon'] ],
            popup=f"{markerData['temp']}"
         )

marker.add_to(m)

m.save(weather_map.html)
```
