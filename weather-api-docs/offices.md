# Get weather office information
**Request**: `https://api.weather.gov/offices/{cwa}`

**Content type**: `application/ld+json`

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
        "https://api.weather.gov/zones/forecast/ANZ233"
    ],
    "responsibleFireZones": [
        "https://api.weather.gov/zones/fire/CTZ002",
        "https://api.weather.gov/zones/fire/CTZ003",
        "https://api.weather.gov/zones/fire/CTZ004",
        "https://api.weather.gov/zones/fire/MAZ002"
    ],
    "approvedObservationStations": [
        "https://api.weather.gov/stations/K1P1",
        "https://api.weather.gov/stations/KACK",
        "https://api.weather.gov/stations/KAFN",
        "https://api.weather.gov/stations/KAQW",
        "https://api.weather.gov/stations/KASH"
    ]
}
```
## Properties
`id`: ID of the weather office.

`name`: Name of the weather offfice.

`address`: Postal address of the weather office.

`telephone`: Phone number of the weather office.

`faxNumber`: Fax number of the weather office.

`email`: Email address of the weather office.

`sameAs`: Website link of the weather office.

`nwsRegion`: NWS region the office falls under. It can be one of the six regions:
* `ar`: Alaska region
* `cr`: Central region
* `er`: Eastern region
* `pr`: Pacific region
* `sr`: Southern region
* `wr`: Western region

`parentOrganization`: Three letter code for the headquarter the office falls under.

`responsibleCounties`: List of URLs for the counties that fall under the weather office.

`responsibleForecastZones`: List of URLs for the forecast zones that fall under the weather office.

`responsibleFireZones`: List of URLs for the fire zones that fall under the weather office.

`approvedObservationStations`: List of URLs for the approved observation stations that fall under the weather office.