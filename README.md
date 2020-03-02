# Godot Community Map
This is a list of Godot regional communities, it will be used as source data to generate the *upcoming* map for the [community page](https://godotengine.org/community).

## Submitting your community

To add your community, create a pull request with a `list/community-name.json` file.

### File name convention

Name the file with the lowercase English name of the community, spaces and other characters replaced with dashes and a `.json` file extension.

Example:

* sao-paulo.json
* rio-de-janeiro.json
* suomi.json

### File format

```
{
  "name": "<community name>",
  "languages": [
    "<ISO 3166-1 alpha 2 language code>",
    ...
  ],
  "location": {
    "city": "<city name>",
    "country": "<ISO 3166-1 alpha 2 country code>",
    "coordinates": {
      "latitude": <latitude>,
      "longitude": <longitude>
    }
  }
  "links": [
    {
      "name": "<text>",
      "link": "<link>"
    },
    ...
  ]
}
```

Notes:
* `name`: required, full name with case (case is missing in the file name).
* `languages`: required, one or many [ISO 3166-1 alpha 2](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) language codes.
* `location`: optional, all properties are also optionl if they don't apply to the community.
* `location.country`: optional, one [ISO 3166-1 alpha 2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements) country code.
* `location.coordinates`: optional, but if given both latitude and longitud must be provided.
* `links`: required, one or many.

Example:
```
{
  "name": "Godot São Paulo Meetup"
  "languages": [
    "SP",
    "EN"
  ],
  "location": {
    "city": "São Paulo",
    "country": "BR",
    "coordinates": {
      "latitude": -23.5505,
      "longitude": -46.6333
    }
  }
  "links": [
    {
      "name": "Meetup",
      "link": "https://www.meetup.com/GodotSP/"
    }
  ]
}
```

### Tips

* To get coordinates use OpenStreetMap, Google Maps or search for  "latitude longitude for ...".
* Pick the most important links for your community, less is more.

If your community is country or city based and a similar name exists and you only want to add an extra links, submit a pull request adding the links to the existing file.
