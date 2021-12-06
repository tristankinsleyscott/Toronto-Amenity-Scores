# Toronto-Amenity-Scores
A program for determining the densities of user inputted buildings/amenities in the City of Toronto via OpenStreetMap.

## Libraries

Libraries and packages used in this project include:

[osmnx](https://osmnx.readthedocs.io/en/stable/)

[Geopandas](https://geopandas.org/en/stable/)

[Folium](http://python-visualization.github.io/folium/)

[Pandas](https://pandas.pydata.org/)

[pyproj](https://pyproj4.github.io/pyproj/stable/)

## OpenStreetMap

OpenStreetMap is the collaborative, open platform used for this project. Tags are to be selected from its repository, found here: https://wiki.openstreetmap.org/wiki/Map_features

## Neighbourhood Shapefile

Data source: https://open.toronto.ca/dataset/neighbourhoods/ This neighbourhood shapefile, which is included in this repository, serves as the geographic boundaries for the choropleth map to be created.
Steps for map creation

Download and unzip the Neighbourhoods.zip file in your working directory.

Create a nested dictionary consisting of your preferred OpenStreetMap tags and store it in a variable. Example: You are wanting a map showing the density of schools, clinics, and police stations. Your dictionary would look as follows:

`tags = {'schools': {'amenity':'school'}, 'clinics': {'amenity':'clinic'}, 'police': {'amenity':'police'}}`

Utilize the main function of this script. Only your nested dictionary needs to be included as the function's parameters. For example:

`amenity_score(tags)`

## Insights

One will generally see a higher density of selected tags in:

The downtown/CBD, due to population/commercial density,
Around Toronto's two main subway lines.

Outside of these two areas, Toronto appears to be a city based upon sprawl, and therefore car-based. Bus lines are quite significant in numbers however, allowing for some level of expediated connection in the city.

## Example Map

Visit the example density map at https://tristankinsleyscott.github.io/Toronto-Amenity-Scores/ to see the density of schools, police stations, and health clinics in Toronto.