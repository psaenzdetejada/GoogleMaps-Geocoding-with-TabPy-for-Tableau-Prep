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

This means, having in your dataset a field that looks more or less like this:

|address                                     |
|--------------------------------------------|
|110 Southwark Street, SE10SU, London, UK    |

The reason is that the more details we include in the address field, the more accurate the geocoding will be. There might be similar Street names in different cities, or similar City names in different States or Countries. The more context we include in the address, the less error the geocoding will return in the results.

## Output
The script is configured to return three additional fields in your output: Latitude, Longitude and Formatted Address from Google's Geocoding API. you should expect an output, based on the previous example, like the following:


|address                                     |latitude |longitude|formatted_address                                   |
|--------------------------------------------|---------|---------|----------------------------------------------------|
|110 Southwark Street, SE10SU, London, UK    |51.50591 |-0.10016 |110 Southwark Street, London SE10SU, United Kingdom |

[tabpy]: https://tableau.github.io/TabPy/docs/server-install.html

