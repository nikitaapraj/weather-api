# Get weather office information
**Request**: `https://api.weather.gov/offices/{cwa}`

**Content type**: `application/geo+json`

## Required parameters

`{cwa}`: The three letter code for the weather office. Must be all caps. For example, `BOX` for Boston, MA.

## Overview

Use this request to get information about a weather office including name, address, and contact information. It also returns a list of counties, forecast zones, and fire zones the office is responsible for as well as a list of approved observation stations under the office.

## Example
### Request
```
https://api.weather.gov/offices/BOX
```

### Response
```
{
    "@context": {
        "@version": "1.1",
        "@vocab": "https://schema.org/"
    },
    "@type": "GovernmentOrganization",
    "@id": "https://api.weather.gov/offices/BOX",
    "id": "BOX",
    "name": "Boston / Norton, MA",
    "address": {
        "@type": "PostalAddress",
        "streetAddress": "46 Commerce Way",
        "addressLocality": "Norton",
        "addressRegion": "MA",
        "postalCode": "02766"
    },
    "telephone": "508.622.3250",
    "faxNumber": "",
    "email": "box.webmaster@noaa.gov",
    "sameAs": "https://www.weather.gov/boston",
    "nwsRegion": "er",
    "parentOrganization": "https://api.weather.gov/offices/ERH",
    "responsibleCounties": [
        "https://api.weather.gov/zones/county/CTC003",
        "https://api.weather.gov/zones/county/CTC013",
        "https://api.weather.gov/zones/county/CTC015",
        "https://api.weather.gov/zones/county/MAC001"  
    ],
    "responsibleForecastZones": [
        "https://api.weather.gov/zones/forecast/ANZ230",
        "https://api.weather.gov/zones/forecast/ANZ231",
        "https://api.weather.gov/zones/forecast/ANZ232",
        "https://api.weather.gov/zones/forecast/ANZ233",
        "https://api.weather.gov/zones/forecast/ANZ234",
        "https://api.weather.gov/zones/forecast/ANZ235"
    ],
    "responsibleFireZones": [
        "https://api.weather.gov/zones/fire/CTZ002",
        "https://api.weather.gov/zones/fire/CTZ003",
        "https://api.weather.gov/zones/fire/CTZ004",
        "https://api.weather.gov/zones/fire/MAZ002",
        "https://api.weather.gov/zones/fire/MAZ003",
        "https://api.weather.gov/zones/fire/MAZ004",
        "https://api.weather.gov/zones/fire/MAZ005",
        "https://api.weather.gov/zones/fire/MAZ006"
    ],
    "approvedObservationStations": [
        "https://api.weather.gov/stations/K1P1",
        "https://api.weather.gov/stations/KACK",
        "https://api.weather.gov/stations/KAFN",
        "https://api.weather.gov/stations/KAQW",
        "https://api.weather.gov/stations/KASH",
        "https://api.weather.gov/stations/KBAF"
    ]
}
```
## Properties