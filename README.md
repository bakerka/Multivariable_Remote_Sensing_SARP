# Seasonal and Land-Use Influences on Urban Heat Island Drivers: A Multi-Sensor Assessment in Gangseo, Seoul
<img align = "left" src="https://science.nasa.gov/wp-content/uploads/2023/11/sarp-patch.jpeg?w=1280&format=webp" alt="drawing" width="200"/>This project was created as part of the [NASA Student Airborne Research Program (SARP)](https://science.nasa.gov/earth-science/early-career-opportunities/student-airborne-research-program/), Hydrology West group of 2026. Along with this project, there was the opportunity to fly on multiple NASA aircrafst (B200, GIII, GV) from the NASA JSC center in Houston, Texas, to take airborne data, as well taking soil moisture measurements in Austin, Texas to validate the satellite data. These measurements were not used in this project. The work done on this project spanned an 8-week time period.


## Abstract
Understanding how land use and urban morphology influence urban heat islands (UHIs) is essential for climate-resilient cities. While many remote sensing studies examine UHIs using limited seasonal observations, this study investigates how moisture, built-up density, and structural complexity influence localized thermal environments across four seasons and five land-use classes. Utilizing satellite imagery from 2016 to 2025 in Gangseo, Seoul, South Korea, I executed stratified regression analyses across five land-use classifications: Urban, Dense Urban, Roads, Nature, and Water. The modeling framework integrated Land Surface Temperature (LST) from Landsat 8 and normalized per image, optical spectral indices (NDVI, NDBI, NDWI) from Sentinel-2 and Synthetic Aperture Radar (SAR) texture metric (VH/VV Ratio) from Sentinel-1, which is sensitive to both moisture and building geometry.

Results demonstrate that UHI drivers vary seasonally, with NDBI associated with higher median temperatures in urban areas, successfully capturing the UHI effect (p<0.01). NDWI was associated with lower median temperatures in the summer, fall, and spring, namely through vegetation and water (p<0.01). SAR VH/VV backscatter ratio didn’t differ with daily rainfall data with any land usages, suggesting that SAR was more sensitive to building structure rather than moisture. Summer had the highest overall explanatory power (R² = 0.84), with other high explanatory powers in the fall (R² = 0.61) and spring (R² =0.71). These results demonstrate the importance of seasonal, multi-variable analysis for understanding urban heat dynamics and supporting climate-resilient urban planning.


## About this template
This template was generated as part of NASA's pursuit of Open Science and to create a public, reproducible analysis of my data workflow. These files begin from Google Earth Engine image collection, to Python statistical analysis and data cleaning, to the creation of all tables and graphs I utilized in my paper. This code can be repurposed for other study areas. 

1. **Run Google Earth Engine first.** When using Google Earth Engine, make sure you have the necessary imports.
2. **Download the Exported Files.** It is recommended to save all exported files into a folder, then move that folder into your Python working directory. When using Python, please execute the first code block, and the rest should work independent of each other.

## Google Earth Engine
Includes the Following:
- Site Selection
- Landsat 8 Scaling and Cloud Cover
- Annual Median Composite Images
- Random Forest Training (80/20)
- Random Forest Classification
- Sentinel 1 and 2 Processing
- NDWI, NDBI (Sentinel 2), LST (Landsat 8), VH, VV (Sentinel 1) Calculations
- Multi-Sensor Table Export Sorted by Sentinel 2 Data

Imports:
- Seoul Municipality Map by Lucy Park (https://github.com/southkorea/seoul-maps)
- USGS Landsat 8 Level 2, Collection 2, Tier 1 (USGS)
- Harmonized Sentinel-2 MSI: MultiSpectral Instrument, Level-2A (SR) (European Union/ESA/Copernicus)
- Cloud Score+ S2_HARMONIZED V1 (Google Earth Engine)
- Sentinel-1 SAR GRD: C-band Synthetic Aperture Radar Ground Range Detected, log scaling (European Union/ESA/Copernicus)
- Land Usage Polygon Points (500 Total, 100 per land use)

## Python
Includes the Following:
- Data Cleaning and Creation of Master CSV File
- Pearson's Correlation and VIF
- Linear Validation of Regression
- Multiple Linear Regression
- LST Bar Graphs
- NDWI and LST_Difference Scatterplots
- NDBI and LST_Difference Scatterplots
- Regression Statistics
- Rainfall Data Spearman Correlation with VH/VV and NDWI (Rainfall CSV Required)
- Image Counts by Year and Season 

Packages Used:
- `pandas`
- `numpy`
- `scipy`
- `scikit-learn`
- `statsmodels`
- `matplotlib`
- `seaborn`

## Acknowledgments
* **NASA SARP 2026** - Hydrology West Group
* NASA Early Career Research Program
* Dr. Mehmet Kurum and Mashalle Olomi - For guidance and support throughout the project.
* Rachel Wegener and Alex Saunders - For teaching me how to code and make code accessible. 


## Contact
**Kira Baker** 
* [LinkedIn Profile](https://www.linkedin.com/in/kira-baker-27b7a5367/)

## Citation
If you use this code or data in your research, please cite this repository:
> Baker, K. (2026). Seasonal and Land-Use Influences on Urban Heat Island Drivers: A Multi-Sensor Assessment in Gangseo, Seoul. NASA Student Airborne Research Program. GitHub. [https://github.com/bakerka/Multivariable_Remote_Sensing_SARP](https://github.com/bakerka/Multivariable_Remote_Sensing_SARP)

## AI Assistance Disclosure
ChatGPT and Google Gemini were used in order to develop and troubleshoot Google Earth Engine and Python scripts for data extraction, statistical regression, and visualization. After using these tools, the author manually reviewed and validated all code outputs and takes full responsibility for the integrity and accuracy of the data analysis and the content of this publication.
