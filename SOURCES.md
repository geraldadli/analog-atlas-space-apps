# Evidence and credits

## Open space-agency data

- NASA EMIT L2B mineral identification: https://doi.org/10.5067/EMIT/EMITL2BMIN.001
- NASA lunar LOLA terrain: https://pds-geosciences.wustl.edu/missions/lro/lola.htm
- NASA Mars MOLA terrain: https://pds-geosciences.wustl.edu/missions/mgs/mola.html
- NASA MODIS supplies surface-temperature and snow screening in the broader notebook. Those patch-scale measurements are not measurements specific to Area A.
- Copernicus GLO-90 supplies initial Earth terrain. GLO-30 supplies the finer follow-up: https://copernicus-dem-30m.s3.amazonaws.com/Copernicus_DSM_COG_10_N27_00_E041_00_DEM/Copernicus_DSM_COG_10_N27_00_E041_00_DEM.tif
- Modified Copernicus Sentinel data (2023 and 2026), accessed through EarthSearch/Sentinel COGs: https://earth-search.aws.element84.com/v1/collections/sentinel-2-l2a
- Sentinel-2 scenes: S2B_37RGL_20231202_0_L2A and S2B_37RGL_20261106_0_L2A.
- Esri World Imagery provides basemap context on slide 4. Acquisition date and absolute positioning accuracy are unverified: https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer

## What the completed run supports

The search sampled 384 geographically stratified Earth patches with fixed seed 20261114. The sample is reproducible with unchanged inputs, but is not an exhaustive or area-weighted global search. A 100 km buffer around a 41-site registry excluded listed analogs; the registry is incomplete and cannot establish novelty.

The initial weighted terrain score uses slope, relief, roughness and low-slope fraction on 1 km and 2 km grids. It is not a probability, a trained machine-learning model, or an operational suitability score. Mineral, temperature and snow evidence are separate follow-up checks. Changing the sample can change the score calibration and shortlist.

Across the broader Ha’il study area, 14 of 16 EMIT observation files passed the scene screen, representing 11 dates. Area A had 9 qualifying dates with repeat hematite and montmorillonite spectral-library signatures. Accepted files do not certify the site. Individual mineral detections also faced quality filters. Independent reconstruction checked the uploaded derived observations, not raw NetCDF quality-mask reprocessing.

The excluded 26 January 2023 file (20230126T111020_2302608_028) had no pixel centres inside the analysis boundary. Another file on that date passed. The excluded 25 May file (20230525T120132_2314508_028) had 3,661 of 94,877 pixels pass the clear-pixel masks: 3.86%, below the 10% threshold. The aggregate audit does not establish which specific mask flags caused those exclusions. Neither exclusion establishes rover suitability or mineral absence.

Area A is centred at 27.576700 N, 41.458478 E and is approximately 200 m square. GLO-30 analysis sampled 36 cell centres: median slope 4.653 degrees and P90 slope 8.787 degrees. GLO-30 and GLO-90 are related products. Small rocks, ledges, soil strength and traction remain unresolved. Satellite mineral matches require field spectroscopy and laboratory confirmation. No harmonized CRISM/M3 mineral comparison was performed.

## Research and field constraints

- du Bray & Stoeser (1985), Al Hufayr quadrangle: https://www.usgs.gov/publications/reconnaissance-geology-al-hufayr-quadrangle-sheet-2741a-kingdom-saudi-arabia
- Abdallah et al. (2020), regional Jabal Aja granites: https://doi.org/10.1111/1755-6724.13825
- Llewellyn et al. (2011), regional conservation context: https://journals.rbge.org.uk/ejb/article/view/1427
- Saudi Arabia tentative-list submission: https://whc.unesco.org/en/tentativelists/6638

Regional geological research exists. The bounded literature search did not establish exact-site novelty. Regional granite is not a demonstrated Martian basalt match. Exact access permissions and conservation boundary overlap remain unverified. A UNESCO tentative-list submission is not World Heritage inscription. Earth cannot reproduce lunar or Martian gravity, atmosphere or radiation.

## Project contribution

The project connects a reproducible terrain shortlist to repeat satellite evidence, explicit exclusions and field-test questions. The demonstrated product is the OSEMN notebook and its exported maps and reports. Slide 3 shows an actual output, not an interactive software screenshot. The proposed benefit is helping teams choose what to investigate before committing to field trials; no operational benefit has yet been measured.

OpenAI Codex assisted with code, analysis and presentation drafting. Satellite images are sourced observations, not AI-generated imagery. This independent Space Apps project is not a NASA endorsement.
