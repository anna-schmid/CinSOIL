# Notes

## What can I find here? 

Here is where I collect all the Data sources that I explored. Currently exploring Soil Data, Elevation Data, potentially further Satellite Data, Weather Data and Carbon Flux Data. 


Starting key notes to check out: 
- “Caring for Soil” mission of the European Commission
- WorldSoils (http://www.world-soils.com/, accessed on 7 Aug 2025) of the European Space Agency (ESA)
- STEROPES of the European Joint H2020 Program SOIL (https://ejpsoil.eu, accessed on 07 Aug 2025) - more importantly check out https://ejpsoil.eu/soil-data/ and https://catalogue.ejpsoil.eu (this looks like a catalogue listing a set of datasets around soil data in Europe (coming from [Vaudour et al., 2022](../papers/Vaudour_et_al_2022.pdf))).
- World Soil Information Service (WoSIS) - see https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3ca32c74-a47b-496d-9943-9db04d7918b5 from [Batjes et. al. (2024)](../papers/Batjes_2024.pdf).




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


#### $${\color{red}USECASE CINSOIL}$$

As far as I understood, we are currently using [Copernicus Sentinel-2 imagery](https://sentinels.copernicus.eu/web/sentinel/sentinel-data-access/sentinel-products/copernicus-sentinel-2-msi-level-2h-and-level-2f-1).

### Overall Characteristics of Soil Data

#### Soil Types and Agroeceosystems 

