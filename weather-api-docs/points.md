# Get weather forecast for a location
**Request**: `https://api.weather.gov/points/{lat},{lon}`

**Content type**: `application/geo+json`

## Required parameters

`{lat}`: Latitude of the location represented as a decimal number. Maximum four decimal places. Must be a positive number since all US locations are in the northern hemisphere. For example, 42.3601° N will be `42.3601`.

`{lon}`: Longitude of the location represented as a decimal number. Maximum four decimal places. Must be a negative number since all US locations are in the western hemisphere. For example, 71.0589° W will be `-71.0589`.

## Overview

## Example
### Request
```
https://api.weather.gov/points/42.3601,-71.0589
```

### Response

```
{
    "@context": [
        "https://geojson.org/geojson-ld/geojson-context.jsonld",
        {
            "@version": "1.1",
            "wx": "https://api.weather.gov/ontology#",
            "s": "https://schema.org/",
            "geo": "http://www.opengis.net/ont/geosparql#",
            "unit": "http://codes.wmo.int/common/unit/",
            "@vocab": "https://api.weather.gov/ontology#",
            "geometry": {
                "@id": "s:GeoCoordinates",
                "@type": "geo:wktLiteral"
            },
            "city": "s:addressLocality",
            "state": "s:addressRegion",
            "distance": {
                "@id": "s:Distance",
                "@type": "s:QuantitativeValue"
            },
            "bearing": {
                "@type": "s:QuantitativeValue"
            },
            "value": {
                "@id": "s:value"
            },
            "unitCode": {
                "@id": "s:unitCode",
                "@type": "@id"
            },
            "forecastOffice": {
                "@type": "@id"
            },
            "forecastGridData": {
                "@type": "@id"
            },
            "publicZone": {
                "@type": "@id"
            },
            "county": {
                "@type": "@id"
            }
        }
    ],
    "id": "https://api.weather.gov/points/42.3601,-71.0589",
    "type": "Feature",
    "geometry": {
        "type": "Point",
        "coordinates": [
            -71.058899999999994,
            42.360100000000003
        ]
    },
    "properties": {
        "@id": "https://api.weather.gov/points/42.3601,-71.0589",
        "@type": "wx:Point",
        "cwa": "BOX",
        "forecastOffice": "https://api.weather.gov/offices/BOX",
        "gridId": "BOX",
        "gridX": 71,
        "gridY": 90,
        "forecast": "https://api.weather.gov/gridpoints/BOX/71,90/forecast",
        "forecastHourly": "https://api.weather.gov/gridpoints/BOX/71,90/forecast/hourly",
        "forecastGridData": "https://api.weather.gov/gridpoints/BOX/71,90",
        "observationStations": "https://api.weather.gov/gridpoints/BOX/71,90/stations",
        "relativeLocation": {
            "type": "Feature",
            "geometry": {
                "type": "Point",
                "coordinates": [
                    -71.020173,
                    42.331960000000002
                ]
            },
            "properties": {
                "city": "Boston",
                "state": "MA",
                "distance": {
                    "unitCode": "wmoUnit:m",
                    "value": 4463.2341874031999
                },
                "bearing": {
                    "unitCode": "wmoUnit:degree_(angle)",
                    "value": 314
                }
            }
        },
        "forecastZone": "https://api.weather.gov/zones/forecast/MAZ015",
        "county": "https://api.weather.gov/zones/county/MAC025",
        "fireWeatherZone": "https://api.weather.gov/zones/fire/MAZ015",
        "timeZone": "America/New_York",
        "radarStation": "KBOX"
    }
}

```
## Attribute table





