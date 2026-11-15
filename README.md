# Analog Atlas
**Moon Base Rocket Science — Gerald Adli (solo)**
NASA Space Apps Jakarta 2026

Find Earth locations worth investigating for Moon and Mars mission rehearsals.

**Challenge:** Identify Earth Locations that Analog the Permanent Moon Base Locations and Mars.

## Demo
[Open the 7-slide presentation](demo.pdf)

## Try it
1. Download [Hail_Investigation_OSEMN.ipynb](Hail_Investigation_OSEMN.ipynb) and open it in Kaggle.
2. Run all cells. The default `RUN_HAIL_16 = False` shows saved evidence and the reviewed Area A result without Earthdata credentials. This is review mode, not a fresh satellite run.
3. To reproduce the 16-granule extraction, enable Internet, add `EARTHDATA_USERNAME` and `EARTHDATA_PASSWORD` to Kaggle Secrets, enable both secrets for the notebook, and set `RUN_HAIL_16 = True`. Allow several GB of downloads. Quality masks remain unchanged.

For the broader Earth search, run [Discovery_OSEMN.ipynb](Discovery_OSEMN.ipynb) in Kaggle or Colab. It downloads terrain and previews datasets before ranking 384 sampled patches. Internet is required. Earthdata credentials are needed only for protected satellite follow-up. A fixed seed repeats the sample only when inputs and settings are unchanged.

Both notebooks bundle their helper code. No extra project files are needed. For local review, run `pip install -r requirements.txt`, then `jupyter lab`. Live Ha’il authentication uses Kaggle Secrets.

## Result
Area A in Ha’il, Saudi Arabia, has hematite and montmorillonite spectral signatures on 9 qualifying dates. Across the wider study area, 14 of 16 EMIT files passed the scene screen. The other two failed coverage or clear-pixel requirements.

Area A is a candidate for field investigation, not a validated rover course. Minerals, access, small obstacles and traction need field checks. Regional research exists; exact-site novelty is unproven. Terrain scores are resemblance scores, not suitability probabilities.

## Data and disclosure
[Sources and scientific limits](SOURCES.md)

NASA LOLA, MOLA, EMIT and MODIS support the analysis, alongside Copernicus terrain and imagery. OpenAI Codex assisted with code, analysis, documentation and presentation layout. Satellite images are observed data. Derived results are calculations from SI-assisted code, not synthetic measurements. Notebook metadata records this assistance.
