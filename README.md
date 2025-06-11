# Network-Based-Spatial-Analysis-of-Transport-Accessibility-for-Urban-Agriculture
This research uses a network-based spatial analysis approach combining real travel distances from OpenStreetMap (OSM) and environmental data from NASA POWER. It leverages Python geospatial libraries to model, analyze, and visualize transport accessibility across five cities.
**Steps Carried Out in the Analysis**
**1. Study Area Definition**
Selected 5 Northern Nigerian cities for analysis: Kaduna, Kano, Jos, Sokoto, and Maiduguri.
**2. Data Collection**
Extracted road networks and farming facility locations using OpenStreetMap via OSMnx.
Retrieved temperature data for farm locations using the NASA POWER API.
**3. Exploratory Data Analysis (EDA)**
Mapped farm locations and road networks.
Generated summary statistics for farm temperature and distance.
**4. Data Preprocessing**
Cleaned and filtered geographic coordinates.
Standardized temperature values.
Ensured consistency in projections (CRS).
**5. Network Construction**
Built city-specific road graphs with OSMnx.
Located nearest graph nodes to farms and city centers.
**6. Distance Calculation**
Calculated shortest-path distances between farms and city centers (bike mode).
Environmental Integration
Merged temperature data with each farm’s distance to city center.
Accessibility Score Computation
Normalized distance and temperature values.
Calculated accessibility score:
(Lower score = better accessibility)
**7. Visualization and Mapping**
Interactive map with farm markers (colored by accessibility).
Distance histogram.
Scatterplot of temperature.
Accessibility score histogram.
**8.Result Interpretation**
Identified Top 5 and Bottom 5 farms by accessibility.
Observed urban core farms (e.g., near 10.49°N, 7.42°E in Kaduna) had better scores.
Noted peripheral farms faced higher travel times and temperatures.
Proposed implications for investment, planning, and policy.
**Tools & Libraries**
pandas, geopandas
osmnx, networkx
matplotlib, seaborn
NASA POWER API
