# Godot Community Map

This is a list of [Godot Engine](https://godotengine.org) regional
communities. It is used as source data to generate a world map in the
[community page](https://godotengine.org/community).

## Submitting your community details

To add your community, create a pull request adding a `.cfg` file in
the `locations` folder using the following naming convention:
```
<ISO country code>-<region name in English>.cfg
```

For example:
```
BR-sao-paulo.cfg
ES-catalonia.cfg
FR-lyon.cfg
```

If your community is country-wide, omit the region name, e.g.:
```
IT.cfg
RU.cfg
```

The country code should be a two-letter
[ISO 3166-1 alpha 2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements).

The file format is as follows:
```
Region: Name of the region
Country: Country code. Multiple ones can be specified, separated by commas.
[Coordinates: Latitude and longitude on the map, e.g. "23.5505° S, 46.6333° W". Can be left out for countries or wider region.]
Link: <Name of the community>,<URL>
[Link: <Optional extra link name>,<Optional extra link URL>]
```

For example:
```
Region: São Paulo
Country: BR
Coordinates: 23.5505° S, 46.6333° W
Link: Godot SP Meetup,https://www.meetup.com/GodotSP/
```

If your a file already exists for your region, add extra links using the
above format. Please check existing region name files to use as an example.
If you want to obtain the coordinates for a place, use OpenStreetMap, Google
Maps or just search "Coordinates for <city>".

If your community spans several countries, feel free to add more country
codes in the "Country" field as comma separated.
