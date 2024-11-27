# Local Results Performance Heatmap

This notebook generates a heatmap to visualize the performance of a client's website in local search results. It uses a city and state to generate surrounding zip codes and runs a SERP API query for each keyword and zip code. The results are then visualized on a heatmap.


## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/tylergargula/Local_Results_Heatmap.git
   cd Local_Results_Heatmap
   ```
   
2. Install Poetry (if you haven't already):
```sh
curl -sSL https://install.python-poetry.org | python3 -

# Install dependencies
poetry install
   ```

## Usage
1. Set your SERP API key and endpoint in the script:  
```python 
VALUE_SERP_KEY = 'YOUR_SERP_API_KEY'
VALUE_SERP_ENDPOINT = 'https://api.valueserp.com/search'
```

2. Configure the city, state, and distance threshold:  
```python 
city = "Santa Clarita"
state = "CA"
distance_threshold = 6  # in miles, adjust as needed
```
3. Run the notebook to generate a heatmap

4. The results will be saved in a CSV file and visualized in a Plotly heatmap and a Folium map.

## Output
```txt
CSV file: export/kw_zipcode_data.csv
Plotly heatmap: plots/heatmap_ranking_zipcodes_<timestamp>.png
Folium map: plots/folium_map_<timestamp>.html
```
#### Plotly Heatmap
![Plotly Heatmap](https://github.com/tylergargula/local-seo-results-heatmap/blob/main/plots/plotly_heatmap_20240917_172836.png)

#### Folium Heatmap
![Folium Heatmap](https://github.com/tylergargula/local-seo-results-heatmap/blob/main/plots/folium_map_20240917_172836.png)