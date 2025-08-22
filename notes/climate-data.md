---
title: Climate Data Sources
last_updated: 2025-08-22
status: Work in progress
---

# Climate Data

Climate data are necessary input for several analyses and models, including soil organic carbon models. The most relevant variables include:
- Temperature
- Precipitations
- Soil moisture


#### ![USECASE CINSOIL](https://img.shields.io/badge/USECASE%20CINSOIL-green)

So far, we used [ERA-5 Land](https://www.ecmwf.int/en/era5-land) dataset, that, in its consolidated version, covers the period from January 1950 to 2-3 months before the present. In addition, the ERA5-Land-T version delivers non-checked close to Near-Real-Time (NRT) daily updates. ERA5-Land-T is synchronized with the close to NRT daily updates provided by the ERA5 climate reanalysis (ERA5T). Currently, ERA5-Land dataset contains only one (9 km) high resolution realisation (HRES).

It provides information on wind, temperature, snow cover, soil temperature, surface pressure, surface solar radiation, total precipitation, and soil water. But it is desirable to use data with higher spatial resolution.


---

## ToDo / Open Questions
- [ ] Search for more **datasets**
- [ ] Check dataset update frequency
- [ ] Circle back after checking in with Research Community, big missing datasets?

---


## Data Sets

<details>
<summary> Expand climate data </summary>

| Dataset | License | Coverage | Notes |
|---------|---------|----------|-------|
|[ERA-5 Land](https://www.ecmwf.int/en/era5-land) | ✅ open access | wind, temp, snow, soil temp, surface precssure, solar rad, prec, soil water; worldwide | | 
|[Worldclim](https://worldclim.org/data/index.html) | ❓ commercial use is not allowed without prior permission | avg min/max temp, total prec: spatial resolution is 2.5 minutes (~21 km2 at the equator), 5 minutes (~85 km2) or 10 minutes (~340 km2): monthly data for 1950-2024 | downscaled from CRU-TS-4.09 by the Climatic Research Unit |
|[TerraClimate](https://www.climatologylab.org/terraclimate.html) | ✅ public domain | Maximum temperature, minimum temperature, vapor pressure, precipitation accumulation, downward surface shortwave radiation, wind-speed: monthly, 4km spatial resolution, 1958-2019 | combining high-spatial resolution climatological normals from the WorldClim dataset, with coarser spatial resolution, but time-varying data from CRU Ts4.0 and the Japanese 55-year Reanalysis (JRA55) |
|[CHIRPS](https://www.chc.ucsb.edu/data/chirps3) | ✅ CC BY 4.0 | 40+ year, high-resolution quasi-global rainfall dataset | |
|[CHIRTS-monthly](https://www.chc.ucsb.edu/data/chirtsmonthly) | ✅ CC BY 4.0 |
|[CHIRTS-ERA5](https://www.chc.ucsb.edu/data/chirts-era5)| ✅ CC BY 4.0 | bias-corrected and downscaled version of the ERA5 temperature product made to be compatible with the CHIRTS product | |
|[NASA POWER](https://registry.opendata.aws/nasa-power/) | ✅ CC BY 4.0 | Solar and meteorological data derived from satellite observations and models | |
|[E-OBS](https://www.ecad.eu/download/ensembles/download.php)| 🔒 Strictly non-commercial | ENSEMBLES daily gridded observational dataset for precipitation, temperature and sea level pressure in Europe | | 

</details>


## Carbon Flux Data

<details>
<summary> Expand carbon flux data </summary>

| Data Set              | License | Overview. | Remarks  | 
|-----------------------|---------|-----------|----------|
|[ICOS FLUXCOM-X](https://www.icos-cp.eu/data-products/fluxcom-x-global-fluxes-collection) | ✅ CC BY 4.0 | Global exchange fluxes for CO2 as GPP, NEE, and water vapor as transpiration and evapotranspiration for the years 2001 until 2021. Depending on the spatial resolution of the data the temporal resolutions are: 0.5 degree: monthly; 0.25 degree: daily, monthly diurnal cycle; 0.05 degree: monthly | |
|[ICOS Carbon Tracker Europe](https://www.icos-cp.eu/data-products/high-resolution-near-real-time-co2-fluxes-over-europe-carbon-tracker-europe-2017-2025) | ✅ CC BY 4.0 | Collection of hourly CO2 fluxes for 2017-2025 | |
|[ICOS Biosphere-atmosphere exchange fluxes for CO2](https://www.icos-cp.eu/data-products/biosphere-atmosphere-exchange-fluxes-co2-vegetation-photosynthesis-and-respiration) | ✅ CC BY 4.0 | Biosphere-atmosphere exchange fluxes for CO2 simulated with the Vegetation Photosynthesis and Respiration Model VPRM for the European domain. | |
|[FLUXNET](https://fluxnet.org/about/)| ✅ open access | | [Access to FLUXNET2015, the most recent dataset](https://fluxnet.org/data/fluxnet2015-dataset/); planned to be fully operational by December 2025|
|[FLUXCOM](https://www.fluxcom.org)| ✅ CC BY 4.0 | [Scaling carbon fluxes from eddy covariance sites to globe: synthesis and evaluation of the FLUXCOM approach](https://bg.copernicus.org/articles/17/1343/2020/bg-17-1343-2020-discussion.html)| [Access Link](https://www.bgc-jena.mpg.de/geodb/projects/Home.php); upscaled flux measurements globally based on FLUXNET data |
|[GloFlux](https://data.tpdc.ac.cn/en/data/761ff597-830d-4e1a-9999-b99fd6f8d4a2) | ✅ CC BY 4.0 | [Nature Paper on GloFLux](https://www.nature.com/articles/s41597-025-05672-8?utm_source=chatgpt.com)| |

</details>