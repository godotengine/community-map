# Godot Community Map
This is a list of Godot regional communities, it is used as source data to generate the map in the [community page](https://godotengine.org/community). 

## Submitting your community

To add your community, create a pull request with a list/<community-name>.cfg text file. 
  
In this case <community_name> is the name of your community, translated to english and using lowercase and dashes. As an example:
  
* godot-engine-in-spanish.cfg
* rio-de-janeiro.cfg
* germany.cfg
 
 

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

Some tips:
* If you want to obtain the coordinates for a place, use OpenStreetMap, Google Maps or just search "Coordinates for <city>".
* If your community spans several countries, feel free to add more country codes in the "Country" field as comma separated.
* For language based communities (non-region based) other than English, just put the list of countries, comma separate, where this language is spoken (For Spanish this may be a a lot, but please add all of them).
* The country code should be a two-letter [ISO 3166-1 alpha 2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements).

If your community is just a simple country or city based community and a similar name exists (like godot-germany.cfg ), and you are only wanting to add an extra social network or link where members of this same community interact, simply submit a pull request to modify the existing file.
