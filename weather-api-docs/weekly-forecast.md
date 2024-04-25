# Get weekly forecast for a location
**Request**: `https://api.weather.gov/{gridId}/{gridX},{gridY}/forecast`

**Content type**: `application/geo+json`

## Required parameters

`{gridId}`: The three letter ID for the weather office. Must be all caps. For example, `BOX` for Boston, MA.

`gridX`: X axis of the grid where the location is. For example, `71`.

`gridY`: Y axis of the grid where the location is. For example, `90`.

## Overview

This request returns a seven-day forecast for the location includign the current day.



## Example
### Request
```
https://api.weather.gov/gridpoints/BOX/71,90/forecast
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
        "forecastGenerator": "BaselineForecastGenerator",
        "generatedAt": "2024-04-25T17:37:24+00:00",
        "updateTime": "2024-04-25T14:50:17+00:00",
        "validTimes": "2024-04-25T08:00:00+00:00/P8DT6H",
        "elevation": {
            "unitCode": "wmoUnit:m",
            "value": 3.9624000000000001
        },
        "periods": [
            {
                "number": 1,
                "name": "This Afternoon",
                "startTime": "2024-04-25T13:00:00-04:00",
                "endTime": "2024-04-25T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 53,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": -7.2222222222222223
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 26
                },
                "windSpeed": "6 to 9 mph",
                "windDirection": "E",
                "icon": "https://api.weather.gov/icons/land/day/skc?size=medium",
                "shortForecast": "Sunny",
                "detailedForecast": "Sunny, with a high near 53. East wind 6 to 9 mph."
            },
            {
                "number": 2,
                "name": "Tonight",
                "startTime": "2024-04-25T18:00:00-04:00",
                "endTime": "2024-04-26T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 33,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": -2.2222222222222223
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 75
                },
                "windSpeed": "5 to 9 mph",
                "windDirection": "SW",
                "icon": "https://api.weather.gov/icons/land/night/skc?size=medium",
                "shortForecast": "Clear",
                "detailedForecast": "Clear, with a low around 33. Southwest wind 5 to 9 mph."
            },
            {
                "number": 3,
                "name": "Friday",
                "startTime": "2024-04-26T06:00:00-04:00",
                "endTime": "2024-04-26T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 54,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": -3.3333333333333335
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 64
                },
                "windSpeed": "5 to 10 mph",
                "windDirection": "NE",
                "icon": "https://api.weather.gov/icons/land/day/skc?size=medium",
                "shortForecast": "Sunny",
                "detailedForecast": "Sunny, with a high near 54. Northeast wind 5 to 10 mph."
            },
            {
                "number": 4,
                "name": "Friday Night",
                "startTime": "2024-04-26T18:00:00-04:00",
                "endTime": "2024-04-27T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 41,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 0
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 67
                },
                "windSpeed": "6 to 9 mph",
                "windDirection": "S",
                "icon": "https://api.weather.gov/icons/land/night/skc?size=medium",
                "shortForecast": "Clear",
                "detailedForecast": "Clear, with a low around 41. South wind 6 to 9 mph."
            },
            {
                "number": 5,
                "name": "Saturday",
                "startTime": "2024-04-27T06:00:00-04:00",
                "endTime": "2024-04-27T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 62,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 0.55555555555555558
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 65
                },
                "windSpeed": "5 to 10 mph",
                "windDirection": "SW",
                "icon": "https://api.weather.gov/icons/land/day/few?size=medium",
                "shortForecast": "Sunny",
                "detailedForecast": "Sunny, with a high near 62. Southwest wind 5 to 10 mph."
            },
            {
                "number": 6,
                "name": "Saturday Night",
                "startTime": "2024-04-27T18:00:00-04:00",
                "endTime": "2024-04-28T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 45,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 30
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 1.6666666666666667
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 65
                },
                "windSpeed": "12 mph",
                "windDirection": "S",
                "icon": "https://api.weather.gov/icons/land/night/rain_showers,20/rain_showers,30?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers after 11pm. Mostly cloudy, with a low around 45. South wind around 12 mph. Chance of precipitation is 30%."
            },
            {
                "number": 7,
                "name": "Sunday",
                "startTime": "2024-04-28T06:00:00-04:00",
                "endTime": "2024-04-28T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 65,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 30
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 8.8888888888888893
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 77
                },
                "windSpeed": "9 to 13 mph",
                "windDirection": "SW",
                "icon": "https://api.weather.gov/icons/land/day/rain_showers,30/rain_showers?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers. Mostly cloudy, with a high near 65. Southwest wind 9 to 13 mph. Chance of precipitation is 30%."
            },
            {
                "number": 8,
                "name": "Sunday Night",
                "startTime": "2024-04-28T18:00:00-04:00",
                "endTime": "2024-04-29T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 51,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 10
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 88
                },
                "windSpeed": "7 to 12 mph",
                "windDirection": "SW",
                "icon": "https://api.weather.gov/icons/land/night/rain_showers?size=medium",
                "shortForecast": "Slight Chance Rain Showers",
                "detailedForecast": "A slight chance of rain showers before 1am. Mostly cloudy, with a low around 51. Southwest wind 7 to 12 mph."
            },
            {
                "number": 9,
                "name": "Monday",
                "startTime": "2024-04-29T06:00:00-04:00",
                "endTime": "2024-04-29T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 69,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": null
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 11.666666666666666
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 87
                },
                "windSpeed": "7 to 12 mph",
                "windDirection": "NE",
                "icon": "https://api.weather.gov/icons/land/day/bkn/rain_showers?size=medium",
                "shortForecast": "Partly Sunny then Slight Chance Rain Showers",
                "detailedForecast": "A slight chance of rain showers after 4pm. Partly sunny, with a high near 69. Northeast wind 7 to 12 mph."
            },
            {
                "number": 10,
                "name": "Monday Night",
                "startTime": "2024-04-29T18:00:00-04:00",
                "endTime": "2024-04-30T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 52,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 30
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 10
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 86
                },
                "windSpeed": "7 to 10 mph",
                "windDirection": "SE",
                "icon": "https://api.weather.gov/icons/land/night/rain_showers/rain_showers,30?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers. Mostly cloudy, with a low around 52. Southeast wind 7 to 10 mph. Chance of precipitation is 30%."
            },
            {
                "number": 11,
                "name": "Tuesday",
                "startTime": "2024-04-30T06:00:00-04:00",
                "endTime": "2024-04-30T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 71,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 40
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 10.555555555555555
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 85
                },
                "windSpeed": "7 to 14 mph",
                "windDirection": "S",
                "icon": "https://api.weather.gov/icons/land/day/rain_showers,30/rain_showers,40?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers. Mostly cloudy, with a high near 71. South wind 7 to 14 mph. Chance of precipitation is 40%."
            },
            {
                "number": 12,
                "name": "Tuesday Night",
                "startTime": "2024-04-30T18:00:00-04:00",
                "endTime": "2024-05-01T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 53,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 40
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 10.555555555555555
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 86
                },
                "windSpeed": "10 to 14 mph",
                "windDirection": "SW",
                "icon": "https://api.weather.gov/icons/land/night/rain_showers,40?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers. Mostly cloudy, with a low around 53. Southwest wind 10 to 14 mph. Chance of precipitation is 40%."
            },
            {
                "number": 13,
                "name": "Wednesday",
                "startTime": "2024-05-01T06:00:00-04:00",
                "endTime": "2024-05-01T18:00:00-04:00",
                "isDaytime": true,
                "temperature": 70,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 30
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 10.555555555555555
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 86
                },
                "windSpeed": "9 to 13 mph",
                "windDirection": "W",
                "icon": "https://api.weather.gov/icons/land/day/rain_showers,30?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers. Partly sunny, with a high near 70. West wind 9 to 13 mph. Chance of precipitation is 30%."
            },
            {
                "number": 14,
                "name": "Wednesday Night",
                "startTime": "2024-05-01T18:00:00-04:00",
                "endTime": "2024-05-02T06:00:00-04:00",
                "isDaytime": false,
                "temperature": 52,
                "temperatureUnit": "F",
                "temperatureTrend": null,
                "probabilityOfPrecipitation": {
                    "unitCode": "wmoUnit:percent",
                    "value": 30
                },
                "dewpoint": {
                    "unitCode": "wmoUnit:degC",
                    "value": 9.4444444444444446
                },
                "relativeHumidity": {
                    "unitCode": "wmoUnit:percent",
                    "value": 77
                },
                "windSpeed": "9 to 13 mph",
                "windDirection": "W",
                "icon": "https://api.weather.gov/icons/land/night/rain_showers,30/rain_showers?size=medium",
                "shortForecast": "Chance Rain Showers",
                "detailedForecast": "A chance of rain showers. Partly cloudy, with a low around 52. West wind 9 to 13 mph. Chance of precipitation is 30%."
            }
        ]
    }
}
```

## Properties

