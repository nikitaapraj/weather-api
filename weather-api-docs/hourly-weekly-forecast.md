# Get hourly forecast for a location
**Request**: `https://api.weather.gov/{gridId}/{gridX},{gridY}/forecast/hourly`

**Content type**: `application/geo+json`

## Required parameters

`{gridId}`: The three letter ID for the weather office. Must be all caps. For example, `BOX` for Boston, MA.

`{gridX}`: X axis of the grid where the location is. For example, `71`.

`{gridY}`: Y axis of the grid where the location is. For example, `90`.

## Overview

This request returns an hourly weather forecast for the coming week for the location starting the current hour.

## Example
### Request
```
https://api.weather.gov/gridpoints/BOX/71,90/forecast/hourly
```

### Response
```
{
    "@context": [
        "https://geojson.org/geojson-ld/geojson-context.jsonld",
        {
            "@version": "1.1",
            "wx": "https://api.weather.gov/ontology#",
            "geo": "http://www.opengis.net/ont/geosparql#",
            "unit": "http://codes.wmo.int/common/unit/",
            "@vocab": "https://api.weather.gov/ontology#"
        }
    ],
    "type": "Feature",
    "geometry": {
        "type": "Polygon",
        "coordinates": [
            [
                [
                    -71.082356500000003,
                    42.374593300000001
                ],
                [
                    -71.087520699999999,
                    42.353187200000001
                ],
                [
                    -71.058567699999998,
                    42.3493712
                ],
                [
                    -71.053397500000003,
                    42.370776999999997
                ],
                [
                    -71.082356500000003,
                    42.374593300000001
                ]
            ]
        ]
    },
    "properties": {
        "updated": "2024-04-25T14:50:17+00:00",
        "units": "us",
        "forecastGenerator": "HourlyForecastGenerator",
        "generatedAt": "2024-04-25T19:38:37+00:00",
        "updateTime": "2024-04-25T14:50:17+00:00",
        "validTimes": "2024-04-25T08:00:00+00:00/P8DT6H",
        "elevation": {
            "unitCode": "wmoUnit:m",
            "value": 3.9624000000000001
        },
        "periods": [
            {
                "number": 1,
                "name": "",
                "startTime": "2024-04-25T15:00:00-04:00",
                "endTime": "2024-04-25T16:00:00-04:00",
                "isDaytime": true,
                "temperature": 52,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 0
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": -8.8888888888888893
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 24
                },
                "windSpeed": "8 mph",
                "windDirection": "E",
                "icon": "https://api.weather.gov/icons/land/day/skc,0?size=small",
                "shortForecast": "Sunny",
                "detailedForecast": ""
            },
            {
                "number": 2,
                "name": "",
                "startTime": "2024-04-25T16:00:00-04:00",
                "endTime": "2024-04-25T17:00:00-04:00",
                "isDaytime": true,
                "temperature": 53,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 0
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": -7.2222222222222223
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 26
                },
                "windSpeed": "9 mph",
                "windDirection": "E",
                "icon": "https://api.weather.gov/icons/land/day/skc,0?size=small",
                "shortForecast": "Sunny",
                "detailedForecast": ""
            }
        ]
    }
}
```

## Properties

`updated`: Date and time the forecast was updated.

`units`: Measurement units for the forecast.

`forecastGenerator`: Forecast generator name.

`generatedAt`: Date and time the forecast was generated.

`updateTime`: Date and time the forecast was updated.

`validTimes`: Date and time the forecast generation is valid until.

`elevation`: Elevation of the location.

* `unitCode`: Measurement unit for the elevation.
* `value`: Elevation of the location.

`periods`: List of the seven-day periods with forecast data.

* `number`: Period number.
* `name`: Name of the period. For example, `This afternoon` or `Saturday night`.
* `startTime`: Start date and time of the period.
* `endTime`: End date and time of the period.
* `isDaytime`: Whether it's a day time. It's either `True` or `False`.
* `temparature`: Temperature for the period.
* `temperatureUnit`: Measurement unit for the temperature. 
* `temperatureTrend`: Temperature trend, if any.
* `probabilityOfPrecipitation`: Chances of precipitation.
    * `unitCode`: Measurement unit for the precipitation chances.
    * `value`: Value for precipitation chances.
* `dewpoint`:
    * `unitCode`: Measurement unit for the dew point.
    * `value`: Value for the dew point.
* `relativeHumidity`:
    * `unitCode`: Measurement unit for relative humidity.
    * `value`: Value for relative humidity.
* `windSpeed`: Range of the windspeed.
* `windDirection`: Direction of the windspeed in one or two letter code. For example, `E` for East.
* `icon`: URL for the relevant weather icon.
* `shortForecast`: Short description of the weather forecast.
* `detailedForecast`: Detailed description of the weather forecast.