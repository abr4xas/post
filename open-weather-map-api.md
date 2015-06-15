Title: Jugando con la API de OpenWeatherMaps
Date: 2015-06-15 10:20
Category: Web
Tags: json, api, php
Slug: open-weather-map-api
Author: abr4xas
twitter: abr4xas
Summary: Como obtener datos del clima desde OpenWeatherMap usando PHP
image: https://superrepo.org/static/images/icons/original/weather.openweathermap.extended.png

> OpenWeatherMap service provides open weather data for more than 200,000 cities and any geo location that is available on our web-site and through API. Ideology of our service is inspired by OpenStreetMap and Wikipedia that make information free and available for everybody. OpenWeatherMap provides wide range of weather data including current weather, forecast, precipitations, wind, clouds, data from weather stations, lots of maps, analytics and many others. We have own model of weather calculation that involves global meteorological broadcast data, own WRF calculation for regions and real-time data from more than 40,000 weather stations.

[http://openweathermap.org/](http://openweathermap.org/)

Entonces, que necesitamos para obtener info sobre el clima en la ciudad?

* URL del API de OWM
* Saber un poquito de PHP

## Juguemos  ᕕ( ᐛ )ᕗ

URL del API:

http://api.openweathermap.org/data/2.5/weather?q=valencia,ve&units=metric

(* Pueden cambiar lo de ```valencia,ve``` con el nombre de su ciudad y el pais *)

Vamos a obtener algo como esto:

```json
{
  "coord": {
    "lon": -68.01,
    "lat": 10.16
  },
  "sys": {
    "type": 1,
    "id": 4292,
    "message": 0.5854,
    "country": "VE",
    "sunrise": 1434017427,
    "sunset": 1434063184
  },
  "weather": [
    {
      "id": 802,
      "main": "Clouds",
      "description": "scattered clouds",
      "icon": "03n"
    }
  ],
  "base": "stations",
  "main": {
    "temp": 28.56,
    "pressure": 1014,
    "humidity": 58,
    "temp_min": 28,
    "temp_max": 29
  },
  "visibility": 10000,
  "wind": {
    "speed": 1.5,
    "deg": 230
  },
  "clouds": {
    "all": 40
  },
  "dt": 1433980800,
  "id": 3625549,
  "name": "Valencia",
  "cod": 200
}
```

En un archivo PHP colocamos lo siguiente:

```php

    $url = file_get_contents("http://api.openweathermap.org/data/2.5/weather?q=valencia,ve&units=metric");

    $json = json_decode($url);

    $ciudad         = $json->name;
    $latitud        = $json->coord->lat;
    $longitud       = $json->coord->lon;
    $temperatura    = $json->main->temp;
    $temperaturamax = $json->main->temp_max;
    $temperaturamin = $json->main->temp_min;
    $presion        = $json->main->pressure;
    $humedad        = $json->main->humidity;
    $viento         = $json->main->speed;

```

Ya solo nos queda imprimir las variables y listo :)

Es muy sencillo, no hay gran cosa en esto quizas, lo que se puede hacer para mejorar esto es:

* Guardar los datos que se necesiten en una tabla en una db para no tener que consultar a cada rato la API  ya que es muy lenta la consulta.
