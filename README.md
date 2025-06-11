# Network-Based-Spatial-Analysis-of-Transport-Accessibility-for-Urban-Agriculture
Spatial analysis transport accessibility across five Northern Nigerian cities using network-based methods
Study Area Definition

Selected 5 Northern Nigerian cities for analysis: Kaduna, Kano, Jos, Sokoto, and Maiduguri.

Data Collection

Extracted road network and farming facility locations using OpenStreetMap via the OSMnx library.

Retrieved environmental data (temperature, humidity) from the NASA POWER API for farm locations.

Exploratory Data Analysis (EDA)

Plotted initial farm locations and road network.

Generated summary statistics for temperature and location spread.

Data Preprocessing

Cleaned and filtered farm coordinates.

Converted temperature data into a consistent format.

Unified CRS and ensured data compatibility.

Network Construction

Built road network graph for each city using OSMnx.

Calculated graph nodes nearest to farm locations and city center.

Distance Calculation

Computed realistic travel distances from each farm to the city center using shortest paths on the network (bike mode).

Stored distance in kilometers for each farm.

Environmental Integration

Merged temperature data with each farm’s distance information.

Accessibility Score Computation

Normalized distance and temperature.

Combined both into a single Accessibility Score:

Score
=
Distance
max
⁡
(
Distance
)
+
Temperature
max
⁡
(
Temperature
)
Score= 
max(Distance)
Distance
​
 + 
max(Temperature)
Temperature
​
 
(Lower score = better accessibility)

Visualization and Mapping

Plotted:

Map of farms and road network with city center.

Histogram of distance to city center.

Scatterplot of temperature at farm locations.

Histogram of accessibility scores (lower is better).

Used Viridis reversed colormap to visualize accessibility.

Result Interpretation

Identified Top 5 and Bottom 5 farms based on accessibility score.

Highlighted spatial inequality and implications for planning and investment.

