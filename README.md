# API DOCUMENTATION FOR NATIONAL WEATHER SERVICE API

*I've created this documentation as a personal project. The official documentation for the NWS API is [here](https://www.weather.gov/documentation/services-web-api).*

Tools used:
* Postman (to test the API endpoints and create examples)
* Visual Studio Code (for writing the docs in Markdown)
* GitHub Desktop (for branching and version control)

----
# Get started with the NWS API

This National Weather Service (NWS) API web service allows you to get weather forecast and information about weather offices across the USA. Forecast files are in `application/geo+json` format while the office information files are in `application/ld+json` format.

## 1. Get the grid data

The NWS API requests use grid data to retrieve information. The grid data corresponds to a grid that each NWS Weather Forecast Office  uses to create forecast. A grid is approximately 2.5 KM X 2.5 KM. 

1. Get coordinates for the location for which you want to obtain the grid values.

2. 



Grid values for a location may occassionaly change. Periodically monitor the latest grid mapping to ensure the correct output.








