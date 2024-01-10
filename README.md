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
Configure virtual environment:
```bash
virtualenv .venv
source .venv/bin/activate
```
Install Dependencies:
```bash
pip install matplotlib geopandas
```
Code:
```python
import geopandas as gpd
import matplotlib.pyplot as plt
import subprocess

FILE_PATH = './nepal.geojson'

admin_boundaries = gpd.read_file(FILE_PATH)
ax = admin_boundaries.plot()
plt.savefig('output_plot.png', format='png')
subprocess.run(['xdg-open', 'output_plot.png'])
```
Run the program:
```bash
python map-of-nepal.py
```
Output image:
![output_plot](https://github.com/opentechcommunity/map-of-nepal/assets/10881526/08b88631-9c67-4c1c-9cf8-a3058c6e8da5)

## License
This geospatial data is provided under the  [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/). Please review the license before using the data.

Feel free to contribute, report issues, or suggest improvements to enhance the usability of this repository. Happy mapping!





