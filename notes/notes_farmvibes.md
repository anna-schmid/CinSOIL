_Last updated: 2025-08-11_

# FarmVibes

## Intro

Goal is to enable researchers, practitioners, and data scienctists to build affordable digital technologies to help farmers estimate the emissions in their farm, with climate adaptation by predicting weather variation, and determine the right management practices that can be profitable and help improve soil health. 

Key technologies: 
- [FarmVibes.Connect](https://www.microsoft.com/en-us/research/articles/farmvibes-connect/): Capturing farm data from sensors, drones, and farm equipment (will be released to GitHub soon)
- [FarmVibes.Edge](https://www.microsoft.com/en-us/research/articles/farmvibes-edge/): Processing farm data captured by drones or other farm sources (will be released to GitHub soon)
- [FarmVibes.AI](https://www.microsoft.com/en-us/research/articles/farmvibes-ai/): Extracting intelligence from farm data and remote sensing sources 
- [FarmVibes.Bot:](https://www.microsoft.com/en-us/research/articles/farmvibes-bot/): Using chat bots to connect with the farmer, either to query data or relay insights (will be released to GitHub soon)



## Farmvibes.AI (MIT license)

The idea is that merging a variety of sources helps to creat the "ultimate truth about a farm". FarmVibes.AI combines several data sources: 
- Heat maps (sensor + ariel imagery, like soil moisture, soil temp, carbon, ...)
- Seeing through clouds (Optical + RADAR, technique SpaceEye)
- Super-res satellite imagery (low res cloud-free + high res cloudy satellite imagery)
- Microclimate prediction (on-farm sensor data with weather predictions from weather services)

FarmVibes.AI can be used to develop and build models that fuse multiple geospatial and spatiotemporal data from the field to obtain insights regarding its carbon footprint (as determined by tilling, fertilization, and cover crops), the nutrition of food that it is growing (e.g., yield and protein content), and the long-term sustainability of the soil and the water (e.g., detect if topsoil erosion is being arrested and water ways are designed to retain rain and flood water).

### Farmvibes on GitHub

[FARMVIBES ON GITHUB](https://github.com/microsoft/farmvibes-ai): Multi-Modal GeopSpatial ML Models for Agriculture and Sustainability 

You can build models that combine geopspatial and spatiotemporal datasets to obtain insights. You can fuse satellite imagery (RGB, SAR, multispectral), drone imagery, weather data, and more.

The GitHub repo conatins several fusion workflows (WF) that help build robust remote sensing, EO, and geopsatial models. 

#### FarmVibes.AI Primer

There are three main pieces to FarmVibes.AI: 

1. Data ingestion and pre-processing WFs (help to prepare data for fusion models tailored toward agriculture) - [FarmVibes.AI Fusion-Ready Dataset Preparation: GitHub Link](https://github.com/microsoft/farmvibes-ai?tab=readme-ov-file#farmvibesai-fusion-ready-dataset-preparation)
  - Select the datasets for fusing, comes with many dataset downloaders: Satellite imagery from Sentinel 1 and 2, US Cropland Data, USGS Elevation maps, NAIP imagery, NOAA weather data, private weather data from Ambient Weather. You can add any rasterized dataset that you want to make them fusion-ready. (Coming: also custom sensor data, like weather sensors)

2. Model training notebook examples, and tuning models. - [FarmVibes.AI Model Sample Notebook Library: GitHub Link](https://github.com/microsoft/farmvibes-ai?tab=readme-ov-file#farmvibesai-model-sample-notebook-library)
  - Can tune the models to make it more accurate for the parts of the world or seasons that you are focusing on.
  - The library includes notebooks for detecting practices (e.g. harvest date detection), estimating climate impact (both seasonal carbon footprint and long term sustainability), micro climate prediction, and crop identification.
  - Starting guide to train fusion models

Complete list of notebooks currently available in FarmVibes.AI: [LIST](https://microsoft.github.io/farmvibes-ai/docfiles/markdown/NOTEBOOK_LIST.html)

Most relevant for our usecase: 
  - Carbon notebook 

3. Computing engine, that supports data ingestion as well as adjusting/creating WFs with the tuned model - [FarmVibes.AI Inference Engine: GitHub Link](https://github.com/microsoft/farmvibes-ai?tab=readme-ov-file#farmvibesai-inference-engine)
  - Combine data connectors, pre-processing, and the model pieces together into a robust inference WFs.t. it runs inference for time range and updates the results once upstream data is uploaded (done by creating a WF composed of fused data prep and fusion model WFs)

### Operation Mode
Open-source, data generated is persisted locally. actual WF and implementation are provided via Docker images. 

User can interact with the local FarmVibes.AI via a REST API, or a local Python client.



### Microsoft Workshop on FarmVibes.AI
Food Security Workshop by Microsoft on [FarmVibes.AI](https://www.youtube.com/watch?v=RNoA7ri2v5I) (Overview & TRAINING), Microsoft Research Summit 2022:
 
We need more data-driven agri-food systems, which will drive efficiencies in the each individual step as part of the whole agri-food chain.
FarmVibes is building on FarmBeats. There are two other big projects, FoodVibes and Modern R&D for Food. FarmVibes.AI is mainly focused on sustainable agriculture. Agriculture is also the most impacted by climate change, farmers need to be better prepared. FarmVibes.AI wants to reduce the amount of impact to climate change, to limit the risk that farmers face and to also use agriculture as a solution to climate change. 

Introduction by Leonardo Nunes: 

Data-driven agriculture: improve yield, reduce cost, ensure sustainability
Challenges: no single data source
WF: Connect data, pre-process, train/build, infer
User input (region, date) -> L2A preprocess -> Detect shadows -> Remove clouds -> Output

Rest API, Python Client



# ![USECASE CINSOIL](https://img.shields.io/badge/USECASE%20CINSOIL-green)

FarmVibes.AI can be used for: 
1. Data acquisition
  - Download Sentinel-1 (SAR), Sentinel-2 (multispectral), Landsat, MODIS (and combine!)
2. Data preprocessing
  - Atmospheric correction
  - Cloud masking 
  - Spatial alignment 
3. Feature/indices generation
  - Vegetation Indices (Normalized Difference Vegetation Index (NDVI), Enhanced Vegetation Index (EVI), Soil/Bare Ground Indices (BSI), Soil-Adjusted Vegetation Index (SAVI)) 
  - Moisture Indices (Normalized Difference Moisture Index (NDMI))
  - Climate, precipitation layers 
  - Topography using Digital Eleveation Models (DEM)

Once we have this foundation we can: 

1. Join them with SOC data (see file [notes_data.md](../notes/notes_data.md) for SOC data brainstorming)
2. Train our model (RothC, Random Forest, etc.) inside or outside FarmVibes.AI
3. Predict SOC spatially

Possible pipeline:
Collect data (SOC reference data (field/lab measurements), Satellite + climate features, DEM, etc.) &rarr Preprocess &rarr  Model: Train our ML model for SOC prediction &rarr Predict + visualize





