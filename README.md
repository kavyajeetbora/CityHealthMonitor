# Health Monitor for Delhi

## TODO

1. Develop a functionized pipeline to convert a given google earth engine raster data to h3 spatial indices
2. Explore more sprectral indices and other spatial data. [spyndex](https://github.com/awesome-spectral-indices/spyndex)
3. Explore more datasets in [gee-community-data-catalog](https://gee-community-catalog.org/changelog/) - Ground water data is available
4. Showing the accessibility of the metro line for all the area in a heatmap.
   [Another Interesting article on measuring the accesibility of subways](https://buff.ly/3WdQahO)

4. Loading open data buildings dataset from overturemaps, plotting in 3D map
5. Plotting the mobile network performance on the map. [Speedtest by Ookla Global](https://registry.opendata.aws/speedtest-global-performance/)


## Health Indices
To begin with, Dashboard showing the key health and environmental indicators for Delhi. 

It will cover the following indicators
  - Surface Temperature

<img src="Delhi Surface Temperature.PNG" height=400/>

  - Urban heat island
  - Landuse / Landcover
  - Air Quality
      - Aerosol Optical Depth (AOD):
          AOD assesses the amount of visible and infrared light that aerosols scatter or absorb in a column of the atmosphere.
          It is a unitless measure, with lower values indicating clear skies and higher values indicating dense aerosols.
          Satellites like MODIS and VIIRS provide AOD data globally1.
      - Nitrogen Dioxide (NO2):
          NO2 is an unhealthy pollutant primarily generated during fossil fuel combustion.
          Satellites, such as Aura Ozone Monitoring Instrument (OMI), observe NO2 levels globally.
          Changes in NO2 concentrations can indicate human activities and air quality2.
      - Ozone (O3):
        Ozone is both unhealthy to breathe and harmful to plants.
        Satellite instruments monitor surface ozone and its precursors.
        Elevated ozone levels impact human health and crop yields.
      - Particulate Matter (PM):
        PM includes tiny particles (e.g., smoke, dust) that cause health issues.
        Satellite data help assess PM concentrations and their sources.
  - Built up index (NDBI)
      - Calculate the total area of the built up, and report the change in total area in the last 5 years say
      - Plot a graph showing the trend of the indices for say last 10 years, show it as popup
## Dashboard

Creating a dashboard to showcase land cover and land use data from satellites is a commendable initiative for decision makers. Let's explore the potential decisions that can be informed by such a dashboard:

1. **Urban Planning and Zoning**:
   - **Decision**: Determine suitable areas for residential, commercial, industrial, and recreational purposes.
   - **Use Case**: Identify zones for housing development, green spaces, and industrial clusters based on land use patterns.

2. **Infrastructure Development**:
   - **Decision**: Plan transportation networks, utilities, and public facilities.
   - **Use Case**: Assess existing land cover to optimize road networks, water supply, sewage systems, and electricity distribution.

3. **Environmental Conservation**:
   - **Decision**: Protect natural habitats, forests, and wetlands.
   - **Use Case**: Identify ecologically sensitive areas for conservation efforts and wildlife corridors.

4. **Disaster Risk Management**:
   - **Decision**: Mitigate risks related to floods, landslides, and earthquakes.
   - **Use Case**: Monitor land cover changes near vulnerable zones and plan evacuation routes.

5. **Agricultural Productivity**:
   - **Decision**: Optimize agricultural practices.
   - **Use Case**: Assess crop distribution, soil quality, and irrigation needs. Promote precision agriculture.

6. **Climate Change Adaptation**:
   - **Decision**: Prepare for climate-related challenges.
   - **Use Case**: Monitor deforestation, urban heat islands, and green cover. Implement climate-resilient strategies.

7. **Land Degradation Assessment**:
   - **Decision**: Combat soil erosion and degradation.
   - **Use Case**: Detect changes in land cover due to mining, deforestation, or urban sprawl. Implement soil conservation measures.

8. **Real Estate and Property Valuation**:
   - **Decision**: Evaluate property values.
   - **Use Case**: Assess land use patterns to determine property worth based on location and amenities.

9. **Health and Well-Being**:
   - **Decision**: Enhance quality of life.
   - **Use Case**: Identify areas lacking green spaces or suffering from pollution. Plan parks and recreational areas.

10. **Monitoring Urban Growth**:
    - **Decision**: Manage urban expansion.
    - **Use Case**: Track changes in land cover over time. Balance development with environmental sustainability.

11. **Water Resource Management**:
    - **Decision**: Optimize water supply and conservation.
    - **Use Case**: Map water bodies, watersheds, and recharge areas. Plan reservoirs and rainwater harvesting.

12. **Biodiversity Assessment**:
    - **Decision**: Preserve biodiversity.
    - **Use Case**: Identify habitats for flora and fauna. Implement green corridors.

Remember that an effective dashboard should provide visualizations, trends, and actionable insights. Collaborate with experts, policymakers, and stakeholders to ensure the dashboard aligns with their needs. 🌍📊🏙️
## Modern Vegeatation Indices

When it comes to assessing vegetation in urban areas, it's essential to consider robust and context-specific vegetation indices. Here are a couple of recent and reliable indices tailored for urban environments:

1. **Multiview Semantic Vegetation Index (MSVI)**:
   - The **MSVI** is a novel vegetation index designed to address limitations in existing indices.
   - **Robust to color variations**, **viewpoint changes**, and **seasonal fluctuations**.
   - Can be directly applied to **RGB images**.
   - Based on **deep semantic segmentation** and **multiview field coverage**.
   - Tested on Google Street View imagery in Wyndham City Council, Melbourne, Australia.
   - Achieved an overall pixel accuracy of **89.4%** and **92.4%** for FCN and U-Net models, respectively¹.

2. **Enhanced Vegetation Index (EVI)**:
   - Although not entirely new, **EVI** remains relevant due to its robustness.
   - It combines **red**, **blue**, and **near-infrared** bands to quantify vegetation presence and activity.
   - Unlike traditional NDVI, **EVI** corrects for atmospheric influences and soil background effects.
   - Suitable for assessing vegetation health and greenness in urban areas⁶.

Remember that the choice of index depends on the specific goals of your analysis and the available data. While **MSVI** caters to urban forestry and street-level assessment, **EVI** provides a broader view of vegetation health. Consider the context and objectives when selecting the most suitable index for your urban vegetation studies! 🌿🏙️🛰️

## Sources:
1. [A Multiview Semantic Vegetation Index for Robust Estimation of Urban Vegetation Cover](https://www.mdpi.com/2072-4292/14/1/228) ¹
2. [Urban greenness, 2001, 2011 and 2019](https://www150.statcan.gc.ca/n1/pub/16-002-x/2021001/article/00002-eng.htm) ⁶

## Industries:

List of companies that work in similar roles:
1. [lobelia.earth](https://www.lobelia.earth/)

## Code snippets and solutions
1. [Maps to streamlit application](https://github.com/opengeos/leafmap/blob/2c25d6e84a9aea2d7f820d4e27093f31f58bbf56/leafmap/foliumap.py#L1875) - to deploy the interactive map to a streamlit component


## Articles and Projects:
1. [Flood prediction in Bangladesh](https://www.omdena.com/blog/floodguard-integrating-rainfall-time-series-and-gis-data-for-flood-prediction-and-waterbody-forecasting-in-bangladesh)
2. [Vegetation Indices To Drive Digital Agri Solutions](https://eos.com/blog/vegetation-indices/#lai)
3. [Urban Heat Island Index Explained](https://kermap.com/en/urban-heat-islands-explained/)
4. [Urban vegetation](https://kermap.com/en/urban-vegetation-the-case-for-green-cities/)
