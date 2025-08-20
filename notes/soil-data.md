---
title: Soil Data Sources
last_updated: 2025-08-18
status: 🚧 Work in progress
---

# Soil Data Sources

Soil datasets are essential as ground reference for CinSOIL analyses and models.  
This file collects datasets, notes, and references related to soil carbon, soil properties, and spectral/biodiversity datasets.  

![CinSOIL Usecase](https://img.shields.io/badge/USECASE%20CINSOIL-green)

---

## 🚧 TODOs / Open Questions
- [ ] Clarify licenses for some datasets (esp. FAO, ITACyL, BORIS, etc.).
- [ ] Search for more **national datasets** (Nordics, Eastern Europe, Africa).
- [ ] Harmonize **metadata**: depth, methods, sample size, lab analysis.
- [ ] Mark datasets useful for **validation** vs. only **comparison** (e.g., SoilGrids).
- [ ] Build “accessibility” overview: ✅ open | ⚠️ unclear | 🔒 restricted.
- [ ] Check dataset update frequency (LUCAS, WoSIS, NABODAT, etc.).

---

## 🌍 Global Datasets

| Dataset | License | Coverage | Notes |
|---------|---------|----------|-------|
| [LUCAS Topsoil](https://esdac.jrc.ec.europa.eu/projects/lucas) | ESDAC registration | EU+UK, ~19k samples (0–20 cm) | SOC, texture, pH, nutrients; campaigns 2009/2012/2015/2018 |
| [WoSIS latest](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3ca32c74-a47b-496d-9943-9db04d7918b5) | ? | Global | Harmonized soil profiles |
| [WoSIS 2023](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/e50f84e1-aa5b-49cb-bd6b-cd581232a2ec) | ? | Global | |
| [SOTER/SOTWIS](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/f9f23e4f-903a-4dfe-bfc4-0e6bf362b09a) | ? | Central & Eastern Europe | Soil parameter estimates |
| [SPADE 14](https://esdac.jrc.ec.europa.eu/content/spade-14#tabs-0-description=0) | ✅ commercial allowed | 1078 soil profiles (28 countries) | |
| [Harmonized World Soil Database v2.0](https://www.fao.org/soils-portal/data-hub/soil-maps-and-databases/harmonized-world-soil-database-v20/en/) | ⚠️ Open, non-commercial only | Global | Needs FAO approval for commercial |
| [ISCN](https://iscn.fluxdata.org/data/) | ? | Global | 70k+ soil carbon locations, community-driven |
| [SoilGrids](https://www.isric.org/explore/soilgrids) | ✅ open | Global | ML-upscaled SOC; ⚠️ not for validation |
| [cup4soil](https://data.isric.org/geonetwork/srv/eng/catalog.search#/metadata/3cc719a6-cbf5-4bc8-94c3-cd7d2b3db3c3) (ISRIC) | ? | Europe | Cup-shaped soil profiles collection |

---

## 🇪🇺 European & Regional

<details>
<summary>Expand regional & national datasets</summary>

| Dataset | License | Coverage | Notes |
|---------|---------|----------|-------|
| [NABODAT](../data/Swiss_Soil_Dataset_V7.pdf) | ✅ open | Switzerland, 42k sites since 1953 | |
| [French National Soil DB](https://recherche.data.gouv.fr/en/dataset/soil-geographical-data-base-for-france-at-1-1000000) | ✅ Etalab 2.0 | France | SOC, nutrients, texture, pH |
| [GisSol](https://www.gissol.fr/donnees) → [Dataverse](https://entrepot.recherche.data.gouv.fr/dataverse/gissol) | ✅ Etalab 2.0 | France | |
| [Stocks de carbone (RMQS)](https://entrepot.recherche.data.gouv.fr/dataset.xhtml?persistentId=doi:10.15454/RURZXN) | ? | France | SOC stocks (0–30 cm) |
| [German Soil Inventory (BZE)](https://www.thuenen.de/en/institutes/climate-smart-agriculture/projects/agricultural-soil-inventory-bze-lw) | ✅ CC BY 4.0 | Germany | |
| [BonaRes Data Repository](https://www.bonares.de/service-portal/data-repository) | ✅ open | Germany | Soil & agronomic research repository |
| [ITACyL](https://suelos.itacyl.es/base_datos) | ⚠️ unclear | Spain (Castilla y León) | |
| [Countryside Survey (UK)](https://www.ukso.org/static-maps/countryside-survey-topsoil.html) | ? | UK | Topsoil survey |
| [BORIS](https://www.umweltbundesamt.at/boris) | ⚠️ restricted | Austria | Form required; maybe commercial use allowed |
| [AboD.at](https://www.ages.at/en/environment/soil/abodat-soil-data-austria/abodat) | ? | Austria | Sparse info |
| [Databank Ondergrond Vlaanderen (DOV)](https://www.dov.vlaanderen.be/geonetwork/srv/api/records/037427b6-d9ad-43ec-9c1e-b423396266d6) | ? | Belgium | SOC stock maps |
| [CARBIOSOL Wallonie](https://geoportail.wallonie.be/catalogue/47e4ea34-fe00-4712-b795-4a85fdab7dd7.html) | ✅ open | Belgium (Wallonia) | TOC contents & stocks |
| [Data.gov.be](https://data.gov.be/en/datasets/7e7ad301-6bf9-4e0d-9935-40e32fc37cf3) | ? | Belgium | Digital soil map of Flanders |
| [INFOSOLO](https://data.isric.org/geonetwork/srv/api/records/25d0cf4d-1865-4d2a-be32-40a1b2483936) | ✅ CC BY 4.0 | Portugal | 9,934 horizons, 3,461 profiles (1966–2014) |
| [EJP Soil Catalogue](https://catalogue.ejpsoil.eu) | ? | Europe | Meta-catalogue of EU soil datasets |
| [WorldSoils (ESA)](http://www.world-soils.com/) | ? | Europe, ESA-led | Accessed 7 Aug 2025 |
| [STEROPES (H2020)](https://ejpsoil.eu/soil-data/) | ? | Europe | EU Joint Program soil data hub |
| [Belgian Soil Sampling (LUCAS verification)](https://catalogue.ejpsoil.eu/collections/metadata:main/items/10.5281-zenodo.15114209) | ? | Belgium | Verification dataset |

</details>

---

## 📊 Soil Spectral Libraries (SSLs)

- [GEOCRADLE SSL](http://datahub.geocradle.eu/dataset/regional-soil-spectral-library)  
- [SoilSpectroscopy.org](https://docs.soilspectroscopy.org/#license)  

---

## 🧬 Soil Biodiversity

- [LUCAS Soil Biodiversity DNA](https://esdac.jrc.ec.europa.eu/content/soil-biodiversity-dna-bacteria-and-fungi)  
- [Bacterial & fungal biomass (FAME)](https://esdac.jrc.ec.europa.eu/content/bacterial-fungal-biomass-fatty-acid-methyl-esters)  
- [EJP Soil Knowledge Platform](https://ejpsoil.eu/knowledge-sharing-platform/soil-data-1)  

---

## 🗂 Link Dump / To be sorted

These need triage & classification:  
- [Environmental Information Data Centre (UK)](https://eidc.ac.uk/finddata)  
- [Soil Organic Carbon Stock Maps for Belgium](https://www.dov.vlaanderen.be/geonetwork/srv/api/records/037427b6-d9ad-43ec-9c1e-b423396266d6)  
- “Caring for Soil” — European Commission Mission  
- [EJP Soil Data Hub](https://ejpsoil.eu/soil-data/)  
- [WorldSoils ESA](http://www.world-soils.com/)  
- [STEROPES Project](https://ejpsoil.eu)  

---

## 📚 References

- Vaudour et al., 2022 — Review of satellite-derived SOC studies (`../papers/Vadour-2024.pdf`)  
- [LUCAS Soil, largest expandable dataset for Europe](https://bsssjournals.onlinelibrary.wiley.com/doi/10.1111/ejss.12499)  
- [Mapping SOC with Gaussian Process Regression](https://www.sciencedirect.com/science/article/pii/S0016706119304768)  
- [Mapping topsoil physical properties](https://www.sciencedirect.com/science/article/pii/S0016706115300173)  

---