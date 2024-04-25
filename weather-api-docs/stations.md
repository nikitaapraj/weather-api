# Get observation station information
**Request**: `https://api.weather.gov/gridpoints/{gridId}/{gridX},{gridY}/stations`

**Content type**: `application/ld+json`

## Required parameters

`{gridId}`: The three letter ID for the observation station. Must be all caps. For example, `BOX` for Boston, MA.

`{gridX}`: X axis of the grid where the location is. For example, `71`.

`{gridY}`: Y axis of the grid where the location is. For example, `90`.

## Overview

Use this request to get a list of observation stations under the specified weather office. Each entry in the list includes the name of the observation stations and URLs for its county, forecast zone, and fire zone. 

## Example
### Request
```
https://api.weather.gov/gridpoints/BOX/71,90/stations
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
            },
            "observationStations": {
                "@container": "@list",
                "@type": "@id"
            }
        }
    ],
    "type": "FeatureCollection",
    "features": [
        {
            "id": "https://api.weather.gov/stations/KBOS",
            "type": "Feature",
            "geometry": {
                "type": "Point",
                "coordinates": [
                    -71.010559999999998,
                    42.36056
                ]
            },
            "properties": {
                "@id": "https://api.weather.gov/stations/KBOS",
                "@type": "wx:ObservationStation",
                "elevation": {
                    "unitCode": "wmoUnit:m",
                    "value": 6.0960000000000001
                },
                "stationIdentifier": "KBOS",
                "name": "Boston, Logan International Airport",
                "timeZone": "America/New_York",
                "forecast": "https://api.weather.gov/zones/forecast/MAZ015",
                "county": "https://api.weather.gov/zones/county/MAC025",
                "fireWeatherZone": "https://api.weather.gov/zones/fire/MAZ015"
            }
        }
    ]
}

```
## Properties

`id`: URL of the observation station.

`type`: Type of the observation station.

`elevation`: Elevation of the observation station.

* `unitCode`: Measurement unit for the elevation.
* `value`: Value for the elevation of the observation station.

`stationIdentifier`: Four letter Id of the observation station.

`name`: Name of the observation station.

`timeZone`: Time zone of the observation station.

`forecast`: URL for the forecast zone of the the observation station.

`county`: URL for the observation station's county.

`fireweatherzone`: URL for the fire zone of the observation station.

