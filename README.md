# Capstone Project — The Battle of Neighborhoods
*Finding a Better Place in Scarborough, Toronto*

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-IBM%20Watson%20Studio-054ADA?logo=ibm&logoColor=white)

## Overview

This project tackles a real-world data science problem: given the sprawling neighborhoods of Scarborough, Toronto, which area offers the best combination of venue amenities, housing affordability, and school quality? Using the Foursquare Places API alongside public datasets, the analysis clusters Scarborough's postal-code-level neighborhoods via K-Means into distinct profiles — then overlays average housing prices and school ratings to surface data-driven relocation recommendations. The result is an interactive, map-based report that turns raw geospatial and venue data into actionable neighborhood insights.

## Features

- Automated extraction of Toronto postal codes and borough boundaries from Wikipedia via web scraping
- Geocoding of all neighborhoods using ArcGIS / Nominatim (with Geopy fallback)
- Foursquare API integration to collect the top venue categories for each neighborhood
- One-hot encoding of venue categories followed by frequency aggregation per neighborhood
- K-Means clustering sweep across 3–10 cluster counts with visual elbow-curve evaluation
- Choropleth and marker maps rendered with Folium for spatial interpretation
- Housing price overlay and school rating analysis to augment pure venue-based clusters
- Full narrative report published to IBM Watson Studio (links below)

## Tech Stack

- **Language:** Python 3
- **Notebook environment:** Jupyter Notebook / IBM Watson Studio
- **Data wrangling:** pandas, NumPy
- **Web scraping:** BeautifulSoup, requests
- **Geocoding:** geocoder, geopy (Nominatim, ArcGIS)
- **Venue data:** Foursquare Places API (REST)
- **Machine learning:** scikit-learn (KMeans)
- **Mapping / visualization:** Folium, Matplotlib

## Getting Started

### Prerequisites

Ensure you have Python 3.x and Jupyter Notebook (or JupyterLab) installed.

### Installation

```bash
# Clone the repository
git clone https://github.com/katkhedepushpak/Capstone-Project-The-Battle-of-Neighborhoods.git
cd Capstone-Project-The-Battle-of-Neighborhoods

# Install dependencies
pip install pandas numpy requests beautifulsoup4 geocoder geopy folium scikit-learn matplotlib
```

> No `requirements.txt` is committed to the repository. The pip command above installs all libraries referenced inside the notebook.

### Foursquare API Credentials

The notebook calls the Foursquare Places API. Before running, set your credentials:

```python
CLIENT_ID     = "YOUR_FOURSQUARE_CLIENT_ID"
CLIENT_SECRET = "YOUR_FOURSQUARE_CLIENT_SECRET"
VERSION       = "20230101"   # YYYYMMDD API version string
```

Replace the placeholder values in the notebook with your own credentials from [developer.foursquare.com](https://developer.foursquare.com/).

## Usage

```bash
jupyter notebook "Capstone Project – The Battle of Neighborhoods - Finding a Better Place in Scarborough, Toronto.ipynb"
```

Run all cells from top to bottom. The notebook will:

1. Scrape and clean the Canada postal-code table from Wikipedia
2. Geocode every Scarborough neighborhood
3. Query Foursquare for nearby venues and encode them
4. Fit K-Means models and display cluster maps
5. Merge housing price and school-rating data and render the final recommendation map

## Live Reports

| Resource | Link |
|---|---|
| Blog post write-up | [roshangrewal.com — Finding a Better Place in Scarborough](http://roshangrewal.com/capstone-project-the-battle-of-neighborhoods-finding-a-better-place-in-scarborough-toronto/) |
| IBM Watson Studio — Project Report | [View notebook](https://eu-gb.dataplatform.cloud.ibm.com/analytics/notebooks/v2/f19f82af-cc9a-4e46-9c0c-41d17204d841/view?access_token=f95b1a10e7d54830dc65fc223fc02fa81ce1b2de5ccce9901c6de7458b1ab859) |
| IBM Watson Studio — Analysis Notebook | [View notebook](https://eu-gb.dataplatform.cloud.ibm.com/analytics/notebooks/v2/92a5a935-0436-4b89-942e-81c89b65b4ee/view?access_token=ad58f325757bfc28d5279ea219383625bba0ba8d9ce99c2726cfe4ef05be66c4) |

## Screenshots

> _Map outputs (Folium choropleth, cluster marker maps) render interactively inside the notebook. Open the IBM Watson Studio links above to view them without a local environment._

## Author

Built by [Pushpak Vijay Katkhede](https://katkhedepushpak.github.io)
