# Nepal Geospatial Data Repository

This repository contains geospatial data for various administrative divisions of Nepal in GeoJSON format. The data is organized into directories based on provinces, districts, and municipalities. The information is intended for use in mapping and geographic information system (GIS) projects related to Nepal.



## Directory Structure

- `maps-of-districts`: Contains GeoJSON files representing the geographical boundaries of districts within various provinces of Nepal.

- `maps-of-municipalities`: Includes GeoJSON files of municipalities categorized by provinces.

- `maps-of-provinces`: Contains GeoJSON files representing the overall boundaries of the provinces in Nepal.

- `nepal.geojson`: Serves as a consolidated dataset, encompassing the entire geographical extent of Nepal

## Usage

- Clone the repository: `git clone https://github.com/opentechcommunity/map-of-nepal.git`
- Explore the desired directory based on your area of interest.
- Use the GeoJSON files in your mapping and GIS projects.


#### Example Usage (Python)
```
pip install matplotlib geopandas
```


```python
import geopandas as gpd

# Load administrative boundaries data
admin_boundaries = gpd.read_file('nepal.geojson')

# Plot the data
admin_boundaries.plot()
```


## License
This geospatial data is provided under the  [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). Please review the license before using the data.

Feel free to contribute, report issues, or suggest improvements to enhance the usability of this repository. Happy mapping!





