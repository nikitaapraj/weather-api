# API DOCUMENTATION FOR NATIONAL WEATHER SERVICE API

*I've created this documentation as a personal project. The official documentation for the NWS API is [here](https://www.weather.gov/documentation/services-web-api).*

Tools used:
* Postman (to test the API endpoints and create examples)
* Visual Studio Code (for writing the docs in Markdown)
* GitHub Desktop (for branching and version control)

----
# Get started with the NWS API

This National Weather Service (NWS) API web service allows you to get weather forecast and information about weather offices across the USA. Forecast files are in `application/geo+json` format while the office information files are in `application/ld+json` format.

**Grid data**

Many requests use grid data. Each NWS Weather Forecast Office creates forecast on a grid definition. A grid is approximately 2.5 KM X 2.5 KM. You can obtain the grid values using the location coordinates. Grid values for a location may occassionaly change. Periodically monitor the latest grid mapping to ensure the correct output.








