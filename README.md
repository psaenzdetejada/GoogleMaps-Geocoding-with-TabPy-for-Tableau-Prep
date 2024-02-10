# TabPy Geocoding with Tableau Prep and Google Maps Geocoding API

The following script allows to geocode addresses using Tableau Prep, TabPy and Google Maps Geocoding API.

## Requirements
The process will require a few requirements in order to work properly:

1. Install TabPy in your computer or in a Server and make sure TabPy is running when geocoding your addresses. You can follow the official documentation to install [TabPy][tabpy].
2. Make sure you have the following Python libraries installed where TabPy is running: googlemaps, pandas and json.
3. The script will run in a Tableau Prep. The way I create the script, it requires to have a field called 'address'.
4. To have an accurate geocoding it's recommended to have as much information in the *address* field. I'd recommend to include:

  - Street name
  - Street number
  - Zip or Postal Code
  - City name
  - County, Province, State or similar detail.
  - Country name.

|address                                           |
|--------------------------------------------------|
|110 Southwark St, London SE1 0SU, United Kingdom  |


[tabpy]: https://tableau.github.io/TabPy/docs/server-install.html

