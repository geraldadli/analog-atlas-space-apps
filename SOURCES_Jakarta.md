# Sources, software and evidence limits

## NASA data used

- [LRO LOLA lunar elevation (LDEM_75S_240M)](https://pds-geosciences.wustl.edu/missions/lro/lola.htm): Lunar south-pole terrain reference.
- [Mars Global Surveyor MOLA MEGDR (MEGT44N000HB)](https://pds-geosciences.wustl.edu/missions/mgs/megdr.html): Jezero terrain reference.
- [EMIT L2B mineral identification V001](https://doi.org/10.5067/EMIT/EMITL2BMIN.001): Mineral IDs, fit, band depth and uncertainty.
- [EMIT L2A reflectance V001, MASK companion](https://doi.org/10.5067/EMIT/EMITL2ARFL.001): Quality masks only; no reflectance-cube mineral comparison.
- [MODIS MOD11A1 V061](https://doi.org/10.5067/MODIS/MOD11A1.061): Quality-screened daily day/night surface-temperature samples.
- [MODIS MOD10A1 V6.1](https://doi.org/10.5067/MODIS/MOD10A1.061): Quality-screened snow-index observations.
- [NASA Earthdata Common Metadata Repository](https://cmr.earthdata.nasa.gov/search/site/docs/search/api.html): Catalog search and granule discovery.
- [NASA Earthdata Login](https://urs.earthdata.nasa.gov/): Authorized data access through Kaggle Secrets.

## Partner and other resources used

- [Copernicus DEM GLO-90 and GLO-30](https://registry.opendata.aws/copernicus-dem/): Earth terrain ranking and finer follow-up.
- [Copernicus Sentinel-2 L2A via EarthSearch](https://earth-search.aws.element84.com/v1/collections/sentinel-2-l2a): Scenes S2B_37RGL_20231202_0_L2A and S2B_37RGL_20261106_0_L2A; modified Copernicus Sentinel data (2023, 2026).
- [ESA WorldCover 2021 v200](https://esa-worldcover.org/en/data-access): Surface-cover screening.
- [ESA Catalogue of Planetary Analogues](https://esamultimedia.esa.int/docs/gsp/The_Catalogue_of_Planetary_Analogues.pdf): Known-site exclusion registry.
- [USGS Terrestrial Analog Sites data](https://doi.org/10.5066/P9J72921): Known-site exclusion registry.
- [Natural Earth admin-1](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-1-states-provinces/): Regional labels.
- [Crossref REST API](https://www.crossref.org/documentation/retrieve-metadata/rest-api/): Published metadata screening; no-hit results do not establish novelty.
- [OpenStreetMap](https://www.openstreetmap.org/copyright): Map baselayers, copyright OpenStreetMap contributors.
- [Esri World Imagery](https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer): Basemap context in earlier investigation; date and positioning accuracy unverified. Not used in the Jakarta slides.
- [du Bray and Stoeser (1985), Al Hufayr quadrangle](https://www.usgs.gov/publications/reconnaissance-geology-al-hufayr-quadrangle-sheet-2741a-kingdom-saudi-arabia): Regional geological context.
- [Abdallah et al. (2020), Jabal Aja granites](https://doi.org/10.1111/1755-6724.13825): Regional geology and hematitization.
- [Llewellyn et al. (2011), Jabal Aja](https://journals.rbge.org.uk/ejb/article/view/1427): Conservation context.
- [UNESCO tentative list: Bioclimatic Refugia of Western Arabia](https://whc.unesco.org/en/tentativelists/6638): Access/conservation context; not World Heritage inscription.
- [Python](https://www.python.org/): Programming language.
- [Jupyter](https://jupyter.org/): Notebook environment.
- [Kaggle](https://www.kaggle.com/docs/notebooks): Cloud execution and Secrets.
- [Google Colab](https://colab.research.google.com/): Alternative environment for discovery notebook.
- [NumPy](https://numpy.org/): Arrays and statistics.
- [pandas](https://pandas.pydata.org/): Tables.
- [Rasterio](https://rasterio.readthedocs.io/): Raster extraction.
- [PyProj](https://pyproj4.github.io/pyproj/stable/): Coordinate transforms.
- [Shapely](https://shapely.readthedocs.io/): Spatial masks.
- [Matplotlib](https://matplotlib.org/): Plots.
- [Folium](https://python-visualization.github.io/folium/): Maps.
- [Leaflet](https://leafletjs.com/): Map rendering.
- [Requests](https://requests.readthedocs.io/): HTTP downloads.
- [earthaccess](https://earthaccess.readthedocs.io/): Earthdata authentication and sessions.
- [netCDF4-Python](https://unidata.github.io/netcdf4-python/): EMIT file reading.
- [PyHDF](https://fhs.github.io/pyhdf/): MODIS HDF4 reading.
- [ipywidgets](https://ipywidgets.readthedocs.io/): Optional interactive notebook controls.
- [GitHub](https://github.com/): Public project hosting.
- [OpenAI Codex](https://openai.com/codex/): SI assistance with code, analysis, text and slide preparation.
- [ReportLab](https://www.reportlab.com/): PDF packaging.
- [pypdf](https://pypdf.readthedocs.io/): PDF inspection.
- [Poppler](https://poppler.freedesktop.org/): PDF rendering for review.

## Evidence scope



The search sampled 384 geographically stratified Earth patches with fixed seed 20261114. The sample is reproducible with unchanged inputs, but is not an exhaustive or area-weighted global search. A 100 km buffer around a 41-site registry excluded listed analogs; the registry is incomplete and cannot establish novelty.

The initial weighted terrain score uses slope, relief, roughness and low-slope fraction on 1 km and 2 km grids. It is not a probability, a trained machine-learning model, or an operational suitability score. Mineral, temperature and snow evidence are separate follow-up checks. Changing the sample can change the score calibration and shortlist.

Across the broader Ha’il study area, 14 of 16 EMIT observation files passed the scene screen, representing 11 dates. Area A had 9 qualifying dates with repeat hematite and montmorillonite spectral-library signatures. Accepted files do not certify the site. Individual mineral detections also faced quality filters. Independent reconstruction checked the uploaded derived observations, not raw NetCDF quality-mask reprocessing.

The excluded 26 January 2023 file (20230126T111020_2302608_028) had no pixel centres inside the analysis boundary. Another file on that date passed. The excluded 25 May file (20230525T120132_2314508_028) had 3,661 of 94,877 pixels pass the clear-pixel masks: 3.86%, below the 10% threshold. The aggregate audit does not establish which specific mask flags caused those exclusions. Neither exclusion establishes rover suitability or mineral absence.

Area A is centred at 27.576700 N, 41.458478 E and is approximately 200 m square. GLO-30 analysis sampled 36 cell centres: median slope 4.653 degrees and P90 slope 8.787 degrees. GLO-30 and GLO-90 are related products. Small rocks, ledges, soil strength and traction remain unresolved. Satellite mineral matches require field spectroscopy and laboratory confirmation. No harmonized CRISM/M3 mineral comparison was performed.



## SI disclosure

OpenAI Codex assisted with Python code, debugging, data-analysis workflows, literature-search support, interpretation drafts, documentation and presentation layout/text. Satellite images and source measurements come from the cited agencies and providers, not generative imagery. Derived maps and summaries were calculated by SI-assisted code. Presentation slides visibly disclose SI-generated layout/text. Shared notebooks and the project provenance metadata acknowledge SI assistance. Independent checks reconstructed the uploaded derived repeat-detection results; raw EMIT NetCDF quality masks were not reprocessed during that validation. Field confirmation remains outstanding.

Not used in the reported comparison: CRISM, M3, Diviner, SWIM and NASA POWER. They are proposed extensions, not completed measurements.
