# Operations Map Specification

## Purpose

This document defines the first map product for Marine Snow Acceleration: a preliminary operational-screening map for sargassum sinking zones and support ports.

The map should visualize where in situ sargassum sinking is more or less desirable based on depth, sargassum density, oceanographic suitability, ecological risk, MRV feasibility, legal feasibility, and port accessibility.

The map is a planning tool, not a deployment authorization.

## Status

Initial map specification.

## Core Map Question

> Where do recurring sargassum patches, suitable deep water, feasible monitoring, acceptable ecological risk, legal pathways, and operational support overlap?

## Map Title

Recommended title:

> Preliminary Sargassum Sinking Zone Screening Map

Subtitle:

> Desirability classes for in situ collect-compress-sink operations, subject to source verification and permitting.

## Map Scope

The initial map should cover:

- tropical Atlantic,
- Caribbean approaches,
- West African margin,
- Cape Verde region,
- Antilles / eastern Caribbean,
- candidate support ports.

The map should not imply that the full Great Atlantic Sargassum Belt is treatable.

## Required Layers

### 1. Sargassum Probability / Density Layer

Purpose:

- identify recurring or high-probability sargassum areas,
- distinguish dense patch fields from sparse occurrence,
- support avoided-coastal-harm analysis.

Possible sources:

- USF / Optical Oceanography Lab sargassum products,
- satellite-derived Sargassum Watch products,
- published GASB distribution studies,
- drift-model outputs.

Map styling:

- low density: pale overlay,
- moderate density: medium overlay,
- high density: strong overlay.

### 2. Bathymetry Layer

Purpose:

- identify no-sink shallow areas,
- show depth contours,
- distinguish shelf, slope, and abyssal regions.

Required contours:

- 1,000 m,
- 2,000 m,
- 3,000 m.

Optional contours:

- 4,000 m,
- 5,000 m.

Map styling:

- <1,000 m: no-sink mask,
- 1,000–2,000 m: research-only shading,
- 2,000–3,000 m: conditional candidate shading,
- >3,000 m: preferred depth shading if other criteria pass.

### 3. Shelf and Slope Exclusion Layer

Purpose:

- avoid deposition on shelves and unstable slope zones,
- reduce benthic concentration risk,
- avoid regions where material may be resuspended or transported into shallower ecosystems.

Map styling:

- shelf and slope: red or hatched exclusion overlay.

### 4. Oceanographic Return-Risk Layer

Purpose:

- identify upwelling zones,
- identify rapid return pathways,
- assess whether decomposition products may return to surface exchange quickly.

Possible variables:

- surface currents,
- vertical velocity / upwelling indicators,
- water-mass residence time,
- mixed-layer depth,
- seasonal mixing.

Map styling:

- high return risk: penalty overlay,
- low return risk: favorable overlay.

### 5. Oxygen Risk Layer

Purpose:

- avoid oxygen-stressed waters,
- identify places where added organic load could create unacceptable oxygen demand.

Map styling:

- low oxygen / high risk: exclusion or penalty overlay,
- adequate oxygen reserve: favorable or neutral.

### 6. Benthic Sensitivity Layer

Purpose:

- avoid sensitive deep benthic habitats,
- avoid seamounts, coral/sponge habitat, protected benthic zones, and unique ecosystems.

Map styling:

- protected or sensitive benthic areas: exclusion overlay,
- unknown habitat: uncertainty overlay.

### 7. Legal / Jurisdiction Layer

Purpose:

- show EEZ boundaries,
- identify jurisdictions where research permits may be possible,
- distinguish high-seas governance questions from national EEZ questions.

Map styling:

- EEZ boundaries,
- candidate permitting jurisdictions,
- legally uncertain areas.

### 8. MRV Feasibility Layer

Purpose:

- identify areas where monitoring is plausible,
- consider distance from port, vessel access, sensor deployment, weather, and data availability.

Map styling:

- high MRV feasibility,
- moderate MRV feasibility,
- low MRV feasibility.

### 9. Candidate Port Layer

Purpose:

- mark possible bases for sargassum baler / compressor / sinking vessels,
- show support-node logic,
- estimate steaming distance to candidate zones.

Candidate ports:

#### Western candidate support nodes

- Bridgetown, Barbados
- Fort-de-France, Martinique
- Pointe-à-Pitre, Guadeloupe

#### Eastern candidate support nodes

- Praia, Cape Verde
- Mindelo, Cape Verde
- Dakar, Senegal

#### Northern maintenance / staging node

- Las Palmas, Canary Islands

Port styling:

- primary candidate base: filled circle,
- secondary support node: open circle,
- maintenance/staging hub: square.

### 10. Port Distance Bands

Purpose:

- estimate operational burden,
- approximate fuel/emissions consequences,
- support fleet logistics planning.

Suggested distance bands:

- 0–250 nautical miles,
- 250–500 nautical miles,
- 500–1,000 nautical miles,
- >1,000 nautical miles.

Distance should not by itself determine suitability, but should affect operations score.

## Desirability Classes

The map should classify ocean cells or polygons into five classes.

| Class | Name | Meaning | Suggested color |
|---|---|---|---|
| Class 0 | No Sink | Exclusion triggered | Red / gray hatch |
| Class 1 | Low Desirability | Research-only or poor candidate | Orange |
| Class 2 | Conditional Candidate | Possible but many uncertainties | Yellow |
| Class 3 | Strong Pilot Candidate | Promising if permits and MRV work | Teal |
| Class 4 | Preferred Candidate | Best overlap of criteria | Dark teal / blue |

The first map should include an uncertainty layer. Unknown should not be shown as favorable.

## Scoring Model

Each candidate zone receives a score after exclusions are applied.

```text
Total desirability score =
  depth score
+ sargassum density score
+ avoided coastal harm score
+ residence-time score
+ oxygen / benthic score
+ MRV feasibility score
+ legal / governance score
+ port / operations score
- upwelling / return-risk penalty
- ecological sensitivity penalty
- data uncertainty penalty
```

## Exclusion Rules

Any of the following makes the zone Class 0:

- depth <1,000 m,
- continental shelf,
- unsuitable slope zone,
- protected or sensitive habitat,
- high oxygen-risk zone,
- strong upwelling / fast return pathway,
- no legal pathway,
- no feasible MRV,
- no plausible avoided-harm case.

## Initial Map Products

### Map 1: Orientation Map

Shows:

- broad sargassum belt / patch probability,
- candidate ports,
- broad depth contours.

Purpose:

- communication and project orientation.

### Map 2: Exclusion Map

Shows:

- no-sink zones,
- shallow areas,
- shelf/slope exclusions,
- protected areas,
- high uncertainty zones.

Purpose:

- prevent overbroad claims.

### Map 3: Desirability Map

Shows:

- Class 0–4 zone rankings,
- candidate support ports,
- port-distance bands.

Purpose:

- preliminary operational screening.

### Map 4: Pilot Candidate Map

Shows:

- small number of candidate research zones,
- suggested control areas,
- monitoring feasibility,
- jurisdiction notes.

Purpose:

- future pilot planning.

## Data Requirements

The map project should identify and document data sources for:

- bathymetry,
- sargassum distribution,
- currents,
- mixed-layer depth,
- upwelling risk,
- oxygen conditions,
- benthic habitat,
- marine protected areas,
- EEZ boundaries,
- ports,
- shipping lanes,
- weather/seasonality,
- research-vessel access.

## File Outputs

Recommended future files:

```text
data/README.md
maps/README.md
maps/sinking-zone-screening.geojson
maps/candidate-ports.geojson
maps/desirability-scoring.csv
maps/map-methodology.md
```

The repository does not yet contain these files. They should be added once data work begins.

## Visual Design Principles

- Do not imply exact precision before data supports it.
- Show uncertainty clearly.
- Distinguish no-sink zones from unknown zones.
- Do not use alarming or promotional colors for candidate zones.
- Label the map as preliminary.
- Include data vintage and source notes.
- Include “not for deployment authorization” on early maps.

## Candidate Port Table

| Port | Role hypothesis | Notes to verify |
|---|---|---|
| Bridgetown, Barbados | Western support base | Port capacity, permitting pathway, distance to candidate zones. |
| Fort-de-France, Martinique | Western secondary support | French/EU governance context, vessel support. |
| Pointe-à-Pitre, Guadeloupe | Western secondary support | French/EU governance context, vessel support. |
| Praia, Cape Verde | Eastern support base | Port capacity, proximity to eastern belt. |
| Mindelo, Cape Verde | Eastern support base / maintenance | Port and repair capability. |
| Dakar, Senegal | Mainland eastern support | Larger infrastructure, longer run depending on zone. |
| Las Palmas, Canary Islands | Northern staging / maintenance hub | Strong logistics, farther from dense tropical belt. |

## Open GIS Questions

- Which sargassum probability dataset is best for first-pass screening?
- Which bathymetry dataset should be canonical?
- How should seasonal variation be represented?
- How should port distance be weighted against depth and MRV?
- How should unknown benthic habitat be penalized?
- Should high seas regions be scored separately from EEZ regions?
- Can a map support legal review without implying deployment intent?

## First Implementation Recommendation

Start with a static concept map, then move to a GIS-backed screening map.

Sequence:

1. Create candidate port GeoJSON.
2. Add bathymetry contours.
3. Add sargassum probability / density overlay.
4. Add no-sink mask.
5. Add preliminary desirability classes.
6. Add uncertainty layer.
7. Publish methodology.
8. Review with oceanographer / GIS specialist before using in external materials.
