# Spatial Data Visualization using Python

This project demonstrates spatial data visualization using Python libraries like `Pandas`, `Matplotlib`, `Seaborn`, and `Folium`. The data consists of geographical coordinates (latitude and longitude) with timestamps, which are visualized on a map of Bangalore, India. The project also includes clustering analysis and dynamic heatmaps based on the data.

## Libraries Used:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `datetime`
- `sklearn.cluster` (DBSCAN for clustering)
- `folium` (for map visualization)

## Project Steps:
1. **Data Loading**: 
   The data is loaded from a `JSON` file using `pandas.read_json()`. It includes fields like `id`, `timestamp`, `latitude`, and `longitude`.

2. **Basic Data Exploration**:
   - Dataframe preview using `df.head()`.
   - Checking for duplicates and null values.
   - Conversion of timestamp strings into `datetime` objects and creating an additional column for `hour`.

3. **Plotting Spatial Data**:
   - **Scatterplot**: The geographical coordinates (longitude and latitude) are plotted using `matplotlib.pyplot.scatter()` on a Bangalore city map.
   - **Seaborn Scatterplot**: A more detailed scatterplot is created using `seaborn.scatterplot()` with different IDs highlighted.
   
   Example:
   ```python
   fig, ax = plt.subplots(figsize=(10, 10))
   ax.scatter(df.longitude, df.latitude)
   ax.set_title('Plotting Spatial Data on Map')
   ax.imshow(banglore_m, extent=BBox, aspect='equal')
