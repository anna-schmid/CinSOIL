_Last updated: 2025-08-11_

# Notes

## What can I find here? 

Here is where I collect all the Data sources that I explored. Currently exploring Soil Data, Elevation Data, potentially further Satellite Data, Weather Data and Carbon Flux Data. 


## Satellite Data
### Satellites Spectral Information 
According to [Vaudour et al., 2022](../papers/Vadour-2024.pdf):

Since 1972 until the mid 2010s: 
- Mainly used __multipectral sensors__ (i.e. sensors with a discrete number of spectral bands)
- Landsat satellites equipped with Thematic Mapper (TM), Enhanced Thematic Mapper (ETM+), and, more recently, Landsat 8 Operational Land Imager (OLI) sensors with 30 m resolution
- Additionally Satellite Pour l’Observation de la Terre (SPOT) equipped with the sensor Haute Résolution Visible (HRV) with 20 m resolution


Since 2000s: __Hyperspectral satellite__ 
-  from the Hyperion sensor with 30 m resolution onboard the satellite Earth Observing 1 (2000–2017), and from the Compact High-Resolution Imaging Spectrometer (CHRIS) with 17m resolution onboard the Project for On-Board Autonomy (PROBA-1) micro-satellite (2001–ongoing)
- PRecursore IperSpettrale della Missione Applicativa (PRISMA) with 239 spectral bands between 400 and 2505 nm has delivered images with 30 m resolution (since 2019)
- Hyperion, CHRISPROBA, simulated PRISMA and PRISMA 
- Environmental Mapping and Analysis Program (EnMAP) (for the assessment of SOC content) (launched 2022)

Also for field-scale approaches with higher spatial resolution:
-IKONOS with 4m resolution, PlanetScope with 3m resolution and Worldview 2 with 2.5m resolution

Since 2015/2017: __MultiSpectral Instrument__ 
- Sentinel-2A, followed by Sentinel-2B 
- Sentinel-2 (S2) _time-series equipped_ with the MultiSpectral Instrument (MSI, 13 spectral bands) provided not only wide spatial coverage over swaths of 290 km, but also 10 to 20 m resolution (10 spectral bands) and a 5-day revisit
- In addition, some authors used Sentinel-1 synthetic aperture radar (SAR), either sperately or directly as covariates within their modeling\
- Over very large areas or national scales, maybe MODIS with 250 or 500 m resultion or Sentinel-3 equipped with the Ocean and Land Colour Instrument (OLCI) with 300 m resolution


#### ![USECASE CINSOIL](https://img.shields.io/badge/USECASE%20CINSOIL-green)

[Copernicus Sentinel-2 imagery](https://sentinels.copernicus.eu/web/sentinel/sentinel-data-access/sentinel-products/copernicus-sentinel-2-msi-level-2h-and-level-2f-1).

## Soil Data

### Overall Characteristics of Soil Data

#### Soil Types and Agroeceosystems 
- Soil types refer tot the World Reference Base (WBR) and the US Soil Taxonomy
- Soils are typically cambisols, and luvisols and, to a lesser extent, regosols, leptosols, stagnosols, chernozems and the so-called “inceptisols” of the US Soil Taxonomy
- The most frequent qualiier is "haplic"

#### Spatial Scales, Sample Size and Density
- Most studies at the scale of small regions, some hundreds km^2
- The total sample size ranged from 32 to 1753 topsoil samples, most of them being collected from the 0–10 cm or 0–20 cm topsoil. The median sample size varies from 85 for field and farm, to 100 for small regions, 264 for large regions and reaches 625 samples for very large region
- Datasets of measured topsoil SOC contents refer to mineral soils with annual crop systems with an average value of ~15 g•kg^(-1) a range of 30 g•kg^(-1) in median
- Mineral and organic soils are usually processed seperately 
- Analytical methods used for SOC measurements are far from being homogenous among laboratories and countries, and specifically in the context of the satellite-derived SOC studies, with 50% using dry combustion, 30% wet oxidation, and others unspecified. The Walkley–Black method, common in the past, tends to underestimate SOC. Dry combustion (automated dry combustion ADC) with a CHN analyzer is now the standard, but results need correction (usually by a factor of 1.33) for wet oxidation. This correction factor varies based on factors like climate and soil type. Additionally, CN analyzers measure total carbon, including carbonates, which must be subtracted to find the actual SOC in calcareous soils.
(least biased method to this point is ADC, with some exceptions for very organic soils)

### Potential Soil Data

Big:
- [ESDAC](https://esdac.jrc.ec.europa.eu/resource-type/datasets) --> [Overview of all Datasets on ESDAC](https://esdac.jrc.ec.europa.eu/resource-type/datasets-list)
- [ISRIC World Soil Information](https://www.isric.org/explore/wosis)

##### Big Scale Actual Datasets
| Data Set              | License | Overview. | Remarks  | 
|-----------------------|---------|-----------|----------|
|[LUCAS topsoil database](https://esdac.jrc.ec.europa.eu/projects/lucas)| Access via ESDAC registration | ~19k samples across EU+UK; SOC, texture, pH, nutrients, and other topsoil properties.; mainly 0–20 cm depth; 2009/2012/2015/2018 | |
[World Soil Information Service (WoSIS)](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3ca32c74-a47b-496d-9943-9db04d7918b5)| | | |
|[SOTER-based soil parameter estimates (SOTWIS) for Central and Eastern Europe, version 2.0](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/f9f23e4f-903a-4dfe-bfc4-0e6bf362b09a) (ISRIC)| | | |
|[WoSIS latest - Organic matter](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3ca32c74-a47b-496d-9943-9db04d7918b5) (ISRIC) | | | |
|[cup4soil](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3cc719a6-cbf5-4bc8-94c3-cd7d2b3db3c3) (ISRIC)| | |
|[SPADE 14](https://esdac.jrc.ec.europa.eu/content/spade-14#tabs-0-description=0) (ESDAC) | commercial use allowed | 1078 soil profile data from 28 countries | | |
|[Harmonized World Soil Database v2.0](https://www.fao.org/soils-portal/data-hub/soil-maps-and-databases/harmonized-world-soil-database-v20/en/)|Open license, but non-commercial use (needs specific approval from FAO)| | |
|[International Soil Carbon Network (ISCN)](https://iscn.fluxdata.org/data/)| Open-access (?), community-driven soil carbon database| Soil data from over 70'000 locations globally | |  
|[National Resources Conservation Service (NRCS)](https://websoilsurvey.sc.egov.usda.gov/App/HomePage.htm) --> [Web Soil Surves (WSS)](https://websoilsurvey.sc.egov.usda.gov/App/WebSoilSurvey.aspx) | Generally open access (Lab Data Mart) | USA | [Access Lab Data Mart](https://ncsslabdatamart.sc.egov.usda.gov) |
|[Rapid Carbon Assessment](https://www.nrcs.usda.gov/resources/data-and-reports/rapid-carbon-assessment-raca) | | USA | [RaCA Download](https://nrcs.app.box.com/s/upx5xhlwis7saunfiysclfrhl5vxxudn) |
| [Gridded Soil Survey Geographic (gSSURGO) Database](https://www.nrcs.usda.gov/resources/data-and-reports/gridded-soil-survey-geographic-gssurgo-database) | Public domain | USA | |


##### Regional, National Monitoring Networks and Datasets
| Data Set              | License | Overview. | Remarks  | 
|-----------------------|---------|-----------|----------|
|[NABODAT, Swiss Soil Dataset](../data/Swiss_Soil_Dataset_V7.pdf)| Non-commercial Creative Commons license (further inquieries ongoing)| 42’000 survey sites, ranging back to 1953 | |
|[French National Soil Data Centre](https://recherche.data.gouv.fr/en/dataset/soil-geographical-data-base-for-france-at-1-1000000)| Etalab Open License 2.0 (commercial use ok) | Topsoil measurements (SOC, nutrients, pH, texture, etc.)| |
|[German Soil Inventory (BZE)](https://www.thuenen.de/en/institutes/climate-smart-agriculture/projects/agricultural-soil-inventory-bze-lw) --> [Open Agrar](https://www.openagrar.de/receive/openagrar_mods_00054877)| CC BY 4.0 | | |
|[ITACyL](https://suelos.itacyl.es/base_datos)| commercial use allowed (as far as I can tell)| Castilla y León | |
|[Countryside survey of topsoil in Great Britain](https://www.ukso.org/static-maps/countryside-survey-topsoil.html)| | | |
|[BORIS](https://www.umweltbundesamt.at/boris)| [Access via form](https://www.umweltbundesamt.at/umweltthemen/boden/boris/boris-datenzugang#c4688)/Commercial use potentially allowed | Austria |  |
| [AboD.at](https://www.ages.at/en/environment/soil/abodat-soil-data-austria/abodat)| | Austrian Soil Data | Nothing of interest found so far, either not found or not available|
|[Databank Ondergrond Vlaanderen (DOV)](https://www.dov.vlaanderen.be/geonetwork/srv/api/records/037427b6-d9ad-43ec-9c1e-b423396266d6) | | Soil organic carbon stock maps for Belgium | Keywords: GEMET, INSPIRE|
|[Data.Gov.Be](https://data.gov.be/en/datasets/7e7ad301-6bf9-4e0d-9935-40e32fc37cf3) | | Digital soil map of the Flemish Region | |
| [CARBIOSOL Wallonie](https://geoportail.wallonie.be/catalogue/47e4ea34-fe00-4712-b795-4a85fdab7dd7.html)| Open access | Total Organic Carbon (TOC) contents and stocks of agricultural soils in Wallonia | |
| [GisSol](https://www.gissol.fr/donnees) --> [GisSol DataVerse](https://entrepot.recherche.data.gouv.fr/dataverse/gissol) | etalab 2.0 | France | |
| [INFOSOLO](https://data.isric.org/geonetwork/srv/api/records/25d0cf4d-1865-4d2a-be32-40a1b2483936) | CC BY 4.0 | Portugal, soil data from a set of 9934 horizons/layers studied in 3461 soil profiles across the country between 1966 and 2014 | [Download](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/25d0cf4d-1865-4d2a-be32-40a1b2483936) |

SSLs:
- [GEOCRADLE (Soil Spectral Library (SSL))](http://datahub.geocradle.eu/dataset/regional-soil-spectral-library)


#### And some more things to check out: 

Link-Dump:

- [BonaRes data repository (Germany)](https://www.bonares.de/service-portal/data-repository)
- [Environmental Information Data Centre](https://eidc.ac.uk/finddata) - seems to have many open license datasets
- [SoilGrids — global gridded soil information](https://www.isric.org/explore/soilgrids): ML-based global gridded soil dataset --> not for validation, but maybe comparison?
- [Belgian Soil Sampling (LUCAS verification)](https://catalogue.ejpsoil.eu/collections/metadata:main/items/10.5281-zenodo.15114209)
- [Soil Organic Carbon Stock Maps for Belgium](https://www.dov.vlaanderen.be/geonetwork/srv/api/records/037427b6-d9ad-43ec-9c1e-b423396266d6)
- [Stocks de carbone (0-30 cm) des sols du réseau RMQS, France](https://entrepot.recherche.data.gouv.fr/dataset.xhtml?persistentId=doi:10.15454/RURZXN)
- “Caring for Soil” mission of the European Commission
- WorldSoils (http://www.world-soils.com/, accessed on 7 Aug 2025) of the European Space Agency (ESA)
- STEROPES of the European Joint H2020 Program SOIL (https://ejpsoil.eu, accessed on 07 Aug 2025) - more importantly check out https://ejpsoil.eu/soil-data/ and https://catalogue.ejpsoil.eu (this looks like a catalogue listing a set of datasets around soil data in Europe (coming from [Vaudour et al., 2022](../papers/Vadour-2024.pdf))).

#### ![USECASE CINSOIL](https://img.shields.io/badge/USECASE%20CINSOIL-green)

So far, used the [LUCAS topsoil database](https://esdac.jrc.ec.europa.eu/projects/lucas).

## Climate Data

| Data Set              | License | Overview. | Remarks  | 
|-----------------------|---------|-----------|----------|
|[ERA-5 Land](https://www.ecmwf.int/en/era5-land) | open access | wind, temp, snow, soil temp, surface precssure, solar rad, prec, soil water; worldwide | | 
|[Worldclim](https://worldclim.org/data/index.html) | commercial use is not allowed without prior permission | avg min/max temp, total prec: spatial resolution is 2.5 minutes (~21 km2 at the equator), 5 minutes (~85 km2) or 10 minutes (~340 km2): monthly data for 1950-2024 | downscaled from CRU-TS-4.09 by the Climatic Research Unit |
|[TerraClimate](https://www.climatologylab.org/terraclimate.html) | public domain | Maximum temperature, minimum temperature, vapor pressure, precipitation accumulation, downward surface shortwave radiation, wind-speed: monthly, 4km spatial resolution, 1958-2019 | combining high-spatial resolution climatological normals from the WorldClim dataset, with coarser spatial resolution, but time-varying data from CRU Ts4.0 and the Japanese 55-year Reanalysis (JRA55) |
|[CHIRPS](https://www.chc.ucsb.edu/data/chirps3) | CC BY 4.0 | 40+ year, high-resolution quasi-global rainfall dataset | |
|[CHIRTS-monthly](https://www.chc.ucsb.edu/data/chirtsmonthly) | CC BY 4.0 |
|[CHIRTS-ERA5](https://www.chc.ucsb.edu/data/chirts-era5)| CC BY 4.0 | bias-corrected and downscaled version of the ERA5 temperature product made to be compatible with the CHIRTS product | |
|[NASA POWER](https://registry.opendata.aws/nasa-power/) | CC BY 4.0 | Solar and meteorological data derived from satellite observations and models | |
|[E-OBS](https://www.ecad.eu/download/ensembles/download.php)| Strictly non-commercial | ENSEMBLES daily gridded observational dataset for precipitation, temperature and sea level pressure in Europe | | 


#### ![USECASE CINSOIL](https://img.shields.io/badge/USECASE%20CINSOIL-green)

So far, used [ERA-5 Land](https://www.ecmwf.int/en/era5-land) dataset, that, in its consolidated version, covers the period from January 1950 to 2-3 months before the present. In addition, the ERA5-Land-T version delivers non-checked close to Near-Real-Time (NRT) daily updates. ERA5-Land-T is synchronized with the close to NRT daily updates provided by the ERA5 climate reanalysis (ERA5T). Currently, ERA5-Land dataset contains only one (9 km) high resolution realisation (HRES).

It provides information on wind, temperature, snow cover, soil temperature, surface pressure, surface solar radiation, total precipitation, and soil water.


## Carbon Flux Data

| Data Set              | License | Overview. | Remarks  | 
|-----------------------|---------|-----------|----------|
|[ICOS FLUXCOM-X](https://www.icos-cp.eu/data-products/fluxcom-x-global-fluxes-collection) | CC BY 4.0 | Global exchange fluxes for CO2 as GPP, NEE, and water vapor as transpiration and evapotranspiration for the years 2001 until 2021. Depending on the spatial resolution of the data the temporal resolutions are: 0.5 degree: monthly; 0.25 degree: daily, monthly diurnal cycle; 0.05 degree: monthly | |
|[ICOS Carbon Tracker Europe](https://www.icos-cp.eu/data-products/high-resolution-near-real-time-co2-fluxes-over-europe-carbon-tracker-europe-2017-2025) | CC BY 4.0 | Collection of hourly CO2 fluxes for 2017-2025 | |
|[ICOS Biosphere-atmosphere exchange fluxes for CO2](https://www.icos-cp.eu/data-products/biosphere-atmosphere-exchange-fluxes-co2-vegetation-photosynthesis-and-respiration) | CC BY 4.0 | Biosphere-atmosphere exchange fluxes for CO2 simulated with the Vegetation Photosynthesis and Respiration Model VPRM for the European domain. | |
|[FLUXNET](https://fluxnet.org/about/)| open access | | [Access to FLUXNET2015, the most recent dataset](https://fluxnet.org/data/fluxnet2015-dataset/); planned to be fully operational by December 2025|
|[FLUXCOM](https://www.fluxcom.org)| CC BY 4.0 | [Scaling carbon fluxes from eddy covariance sites to globe: synthesis and evaluation of the FLUXCOM approach](https://bg.copernicus.org/articles/17/1343/2020/bg-17-1343-2020-discussion.html)| [Access Link](https://www.bgc-jena.mpg.de/geodb/projects/Home.php); upscaled flux measurements globally based on FLUXNET data |
|[GloFlux](https://data.tpdc.ac.cn/en/data/761ff597-830d-4e1a-9999-b99fd6f8d4a2) | CC BY 4.0 | [Nature Paper on GloFLux](https://www.nature.com/articles/s41597-025-05672-8?utm_source=chatgpt.com)| |


## Typology

### Digital Elevation Models

| Data Set              | License | Overview. | Remarks  | 
|-----------------------|---------|-----------|----------|
|[Copernicus DEM](https://dataspace.copernicus.eu/explore-data/data-collections/copernicus-contributing-missions/collections-description/COP-DEM) | Free access to 30/90m res (GLO-30/90), 10m special access (EEA-10) | Global Digital Surface Model (DSM); Data were acquired through the TanDEM-X mission between 2011 and 2015. The datasets were made available for use in 2019 and will be maintained until 2026. | Access via [Copernicus Browser](https://browser.dataspace.copernicus.eu/) or [API](https://dataspace.copernicus.eu/analyse/apis) |
|[NASA SRTM](https://cmr.earthdata.nasa.gov/search/concepts/C1220566448-USGS_LTA.html) | | | Access via [Earth Explorer](https://earthexplorer.usgs.gov) | 
|[OpenTopography](https://opentopography.org) | open access| Centralized access to a diverse collection of topographic data. See [Data Catalogue](https://portal.opentopography.org/dataCatalog?group=global) | |

