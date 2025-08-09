# Notes

## What can I find here? 

Here is where I collect all the Data sources that I explored. Currently exploring Soil Data, Elevation Data, potentially further Satellite Data, Weather Data and Carbon Flux Data. 


### Satellites Spectral Information 
According to [Vaudour et al., 2022](../papers/Vaudour_et_al_2022.pdf):

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

As far as I understood, we are currently using [Copernicus Sentinel-2 imagery](https://sentinels.copernicus.eu/web/sentinel/sentinel-data-access/sentinel-products/copernicus-sentinel-2-msi-level-2h-and-level-2f-1).

### Overall Characteristics of Soil Data

#### Soil Types and Agroeceosystems 
- Soil types refer tot the World Reference Base (WBR) and the US Soil Taxonomy
- Soils are typically cambisols, and luvisols and, to a lesser extent, regosols, leptosols, stagnosols, chernozems and the so-called “inceptisols” of the US Soil Taxonomy
- The most frequent qualiier is "haplic"

#### Spatial Scales, Sample Size and Density
- Most studies at the scale of small regeions, some hundreds km^2
- The total sample size ranged from 32 to 1753 topsoil samples, most of them being collected from the 0–10 cm or 0–20 cm topsoil. The median sample size varies from 85 for field and farm, to 100 for small regions, 264 for large regions and reaches 625 samples for very large region
- Datasets of measured topsoil SOC contents refer to mineral soils with annual crop systems with an average value of ~15 g•kg^(-1) a range of 30 g•kg^(-1) in median
- Mineral and organic soils are usually processed seperately 
- Analytical methods used for SOC measurements are far from being homogenous among laboratories and countries, and specifically in the context of the satellite-derived SOC studies, with 50% using dry combustion, 30% wet oxidation, and others unspecified. The Walkley–Black method, common in the past, tends to underestimate SOC. Dry combustion (automated dry combustion ADC) with a CHN analyzer is now the standard, but results need correction (usually by a factor of 1.33) for wet oxidation. This correction factor varies based on factors like climate and soil type. Additionally, CN analyzers measure total carbon, including carbonates, which must be subtracted to find the actual SOC in calcareous soils.
(least biased method to this point is ADC, with some exceptions for very organic soils)

#### Potential Soil Data

- [LUCAS topsoil database](https://esdac.jrc.ec.europa.eu/projects/lucas)
- [European Soil Data Centre (ESDAC)](https://esdac.jrc.ec.europa.eu)
- [French National Soil Data Centre](https://recherche.data.gouv.fr/en/dataset/soil-geographical-data-base-for-france-at-1-1000000)
- [BonaRes data repository (Germany)](https://www.bonares.de/service-portal/data-repository)
- [WoSIS Soil Profile Database](https://www.isric.org/explore/wosis)
- [World Soil Information Service (WoSIS)](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3ca32c74-a47b-496d-9943-9db04d7918b5) - see from [Batjes et. al. (2024)](../papers/Batjes_2024.pdf).
- [Swiss Soil Dataset](../data/Swiss_Soil_Dataset_V7.pdf)
- [Harmonized World Soil Database v2.0](https://www.fao.org/soils-portal/data-hub/soil-maps-and-databases/harmonized-world-soil-database-v20/en/)
- [Countryside survey of topsoil in Great Britain](https://www.ukso.org/static-maps/countryside-survey-topsoil.html)

More ideas:
- [European HYdropedological Data Inventory (EU-HYDI)](https://publications.jrc.ec.europa.eu/repository/handle/JRC81129)
- [Soil profile analytical database 14 (SPADE 14)](https://esdac.jrc.ec.europa.eu/content/spade-14)
- [German Agricultural Soil Inventory (BZE-LW)](https://www.thuenen.de/en/institutes/climate-smart-agriculture/projects/agricultural-soil-inventory-bze-lw)



Usage of SSLs? 
- [GEOCRADLE (Soil Spectral Library (SSL))](http://datahub.geocradle.eu/dataset/regional-soil-spectral-library)

#### ![USECASE CINSOIL](https://img.shields.io/badge/USECASE%20CINSOIL-green)

So far, used the [LUCAS topsoil database](https://esdac.jrc.ec.europa.eu/projects/lucas).



And some more things to check out: 

- “Caring for Soil” mission of the European Commission
- WorldSoils (http://www.world-soils.com/, accessed on 7 Aug 2025) of the European Space Agency (ESA)
- STEROPES of the European Joint H2020 Program SOIL (https://ejpsoil.eu, accessed on 07 Aug 2025) - more importantly check out https://ejpsoil.eu/soil-data/ and https://catalogue.ejpsoil.eu (this looks like a catalogue listing a set of datasets around soil data in Europe (coming from [Vaudour et al., 2022](../papers/Vaudour_et_al_2022.pdf))).