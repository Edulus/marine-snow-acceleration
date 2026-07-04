# Sargassum Mapping and Ground-Truth Framework

## Purpose

This document defines the mapping-data spine for Marine Snow Acceleration.

The project depends on being able to distinguish:

1. where sargassum is currently located,
2. how dense or extensive a patch may be,
3. where it is likely to drift,
4. whether it is likely to beach on a target coast,
5. whether it overlaps an approved sinking zone,
6. how satellite detections are validated by ground truth.

This document supports:

- `docs/15-operations-map-spec.md`
- `docs/16-mexico-quintana-roo-coastal-protection-branch.md`
- `docs/14-sinking-zone-criteria.md`

## Status

Initial framework with source leads.

## Core Principle

> No forecasted patch, no avoided-beaching claim. No ground truth, no biomass-confidence claim.

For the Mexico / Quintana Roo branch, this matters especially because the project must show that treated offshore biomass plausibly would have affected Cancún, Tulum, Holbox, Cozumel, Playa del Carmen, or the Riviera Maya if untreated.

## Primary Operational Mapping Products

### 1. USF Optical Oceanography Lab — SaWS

**Name:** Satellite-based Sargassum Watch System (SaWS)

**Institution:** University of South Florida Optical Oceanography Laboratory.

**Use in project:** Primary operational source candidate for satellite-observed sargassum location and abundance across the tropical Atlantic, Caribbean Sea, and Gulf of Mexico.

**Relevant capabilities:**

- near-real-time sargassum detection and tracking,
- clickable regional maps,
- daily satellite-observed sargassum and ocean-variable updates,
- monthly sargassum outlook bulletins,
- Google Earth-compatible products,
- regional products including Cancun, Yucatan, Caribbean, Central Atlantic, Cape Verde, and West Africa regions,
- high-resolution Sentinel-2 products for selected coastal regions, including Cancun.

**Method notes:**

SaWS uses satellite data and numerical models to detect and track pelagic sargassum. Its customized satellite products include the Floating Algae Index (FAI) for detecting floating algae and related surface material.

**Source:** https://optics.marine.usf.edu/projects/saws.html

### 2. CariCOOS Sargassum Tracker

**Name:** Sargassum Tracker

**Institution:** Caribbean Coastal Ocean Observing System (CariCOOS).

**Use in project:** Regional operational context for Caribbean sargassum tracking, outlooks, and stakeholder-facing visualization.

**Relevant capabilities:**

- satellite images,
- forecasts and outlooks,
- regional sargassum tracker interface,
- connection to USF long-term outlook products,
- Caribbean-facing communication layer.

**Important limitation:**

CariCOOS / USF outlook material is designed for general bloom condition and future bloom probability. It should not be treated as a precise beach-level forecast unless paired with higher-resolution modeling and local validation.

**Source:** https://www.caricoos.org/sargassum

### 3. NOAA Sargassum Resources

**Name:** NOAA sargassum resources and response pages.

**Use in project:** Governance, response, forecasting, emergency-management, and coastal-impact context.

**Relevant capabilities:**

- background on sargassum from open ocean to shore,
- Sargassum Inundation Event framing,
- links to forecasting and management resources,
- disaster-response and coastal-management context,
- research on social and economic impacts of beaching.

**Source:** https://oceanservice.noaa.gov/news/sargassum/

### 4. NOAA / USF Sargassum Inundation Reports

**Use in project:** Candidate input for likely-beaching risk and avoided-coastal-harm screening.

**Relevant capability:**

Sargassum Inundation Reports use satellite-observed sargassum location, proximity to shore, and statistical methods to estimate likelihood of beaching events.

**Source lead:** USF SaWS page and NOAA CoastWatch resources.

### 5. Scientific Algorithm and Research Products

**Use in project:** Methodological backbone for turning satellite imagery into maps, percent cover, biomass estimates, and uncertainty bounds.

Important research areas:

- Floating Algae Index (FAI),
- Alternative Floating Algae Index (AFAI),
- MODIS / VIIRS products,
- Sentinel-3 OLCI products,
- Sentinel-2 high-resolution coastal validation,
- deep-learning detection refinements,
- drift and transport modeling,
- satellite-to-beach forecast validation.

## Primary Ground-Truth Sources

Satellite maps are not enough. They need validation.

Ground truth should include:

### 1. Shipboard and Research-Cruise Observations

Use:

- direct visual observations,
- transect photography,
- net tows,
- biomass samples,
- species confirmation,
- wet mass and dry mass sampling,
- carbon content estimates.

Purpose:

- validate satellite detections,
- calibrate percent cover to biomass,
- estimate conversion from satellite signal to tonnes,
- measure uncertainty.

### 2. Aerial and Drone Surveys

Use:

- high-resolution patch imagery,
- nearshore coverage checks,
- subpixel patch validation,
- surface morphology assessment,
- local response verification.

Purpose:

- validate patchiness below medium-resolution satellite scale,
- reduce false positives and false negatives near shore,
- support coastal-risk assessment.

### 3. Coastal and Shoreline Surveys

Use:

- beaching records,
- shoreline tonnage estimates,
- beach line length affected,
- cleanup volume,
- timing and severity records,
- municipal and hotel-zone reports.

Purpose:

- connect offshore detections to real coastal harm,
- validate drift-to-landfall models,
- estimate avoided cleanup and avoided ecological harm.

### 4. Citizen Science and Local Observations

Use:

- time-stamped beach reports,
- photographs,
- local environmental-agency reports,
- hotel / tourism-sector observations,
- municipal cleanup records.

Purpose:

- fill spatial and temporal gaps,
- improve coastal receptor records,
- support Mexico / Quintana Roo avoided-beaching claims.

### 5. High-Resolution Satellite and Airborne Imagery

Use:

- Sentinel-2,
- Landsat 8/9,
- commercial high-resolution imagery where available,
- airborne hyperspectral imagery if available.

Purpose:

- verify smaller patches,
- improve nearshore detection,
- validate operational map layers before dispatch.

## Known Limitations

### Medium-Resolution Satellite Limitations

MODIS and VIIRS provide broad synoptic coverage, but may struggle with:

- mixed pixels near shore,
- cloud cover,
- cloud adjacency effects,
- small patches,
- nearshore false positives,
- biomass conversion uncertainty,
- species or material confusion.

### Outlook and Forecast Limitations

Regional outlooks are not automatically beach-specific forecasts.

For operational use, they must be paired with:

- drift modeling,
- wind and current forecasts,
- higher-resolution coastal imagery,
- shoreline reports,
- uncertainty bounds.

### Biomass Conversion Limitations

Turning percent cover into tonnes requires calibration.

The project must not assume a universal conversion factor without:

- local biomass samples,
- wet/dry mass measurement,
- carbon fraction measurement,
- seasonal and regional calibration,
- uncertainty range.

## Mapping Pipeline for This Project

### Step 1: Detect

Use SaWS / satellite products to identify candidate offshore sargassum patches.

### Step 2: Classify

Classify patches by:

- size,
- density,
- persistence,
- proximity to shore,
- location relative to no-sink zones,
- location relative to candidate sinking zones.

### Step 3: Forecast

Use drift modeling to estimate whether a patch is likely to beach.

For Mexico / Quintana Roo, receptors include:

- Cancún / Isla Mujeres,
- Puerto Morelos,
- Playa del Carmen,
- Cozumel,
- Tulum,
- Holbox.

### Step 4: Validate

Validate candidate patches with:

- high-resolution imagery,
- drone or aerial survey if nearshore,
- vessel observations if offshore,
- citizen or shoreline reports for receptor coasts.

### Step 5: Intersect with Sinking-Zone Criteria

A patch is operationally relevant only if:

- it is likely to cause coastal harm if untreated,
- it can be reached in time,
- treatment can occur over a suitable deep-water zone,
- sinking-zone criteria are satisfied,
- monitoring is feasible,
- legal authority exists.

### Step 6: Record Evidence Chain

For each treated patch, preserve:

- satellite source and timestamp,
- patch geometry,
- density estimate,
- drift forecast,
- expected receptor beach,
- uncertainty estimate,
- validation method,
- treatment location,
- release location,
- sinking verification,
- coastal-harm counterfactual.

## Mexico / Quintana Roo Special Requirements

The Mexico branch requires a **patch-to-beach evidence chain**.

Minimum evidence:

1. SaWS or equivalent detection of patch.
2. Drift forecast toward Quintana Roo receptor coast.
3. Confidence score for expected beaching.
4. Identification of likely affected receptor: Cancún, Tulum, Holbox, etc.
5. Confirmation that treatment can occur away from shelf/reef/no-sink zones.
6. Comparison against untreated patches or historical landfall record.
7. Post-event shoreline observations.

## Data Products to Add Later

Recommended future files:

```text
maps/sargassum-data-sources.md
maps/sargassum-products-inventory.csv
maps/ground-truth-sources.csv
maps/mexico-receptor-beaches.geojson
maps/saws-regions-of-interest.md
maps/patch-to-beach-methodology.md
```

## Immediate Research Tasks

- Identify exact SaWS data-access paths for Cancun, Yucatan, Central Atlantic, Cape Verde, and West Africa regions.
- Determine whether SaWS products can be downloaded as images, KML/KMZ, GeoTIFF, CSV, or other GIS formats.
- Identify whether NOAA Sargassum Inundation Reports provide machine-readable outputs.
- Identify CariCOOS data-access endpoints.
- Create a ground-truth source inventory for Mexico / Quintana Roo.
- Identify official Mexican sargassum monitoring records.
- Define minimum patch-to-beach confidence score for funding claims.

## Operational Standard

The project shall not claim avoided beaching or carbon removal from satellite detection alone.

Satellite detection begins the evidence chain. Ground truth, drift modeling, treatment records, sinking verification, and coastal observations complete it.
