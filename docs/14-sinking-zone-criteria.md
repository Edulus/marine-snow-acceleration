# Sinking Zone Criteria

## Purpose

This document defines how Marine Snow Acceleration should decide whether an ocean area is suitable for in situ sargassum sinking.

It applies to both:

1. spray-based in situ sargassum ballasting,
2. mobile in situ sargassum densification.

The goal is to replace vague phrases like “deep enough” with a transparent, multi-factor screening process.

## Status

Initial criteria framework.

This document is not a deployment authorization. It is a planning and research-screening tool.

## Core Principle

> Sink only where depth, residence time, ecology, law, monitoring, and avoided harm all support the case.

Depth is necessary but not sufficient.

A site can be deep and still unsuitable.

## Working Minimum Depth Standard v0.1

No in situ sargassum sinking shall be proposed in water shallower than:

> **1,000 m**

The preferred minimum for pilot planning is:

> **2,000–3,000 m or deeper**

provided that the site also passes residence-time, oxygen, benthic, legal, and MRV filters.

The 1,000 m threshold is a working floor, not a magic number. It must eventually be replaced or refined by region-specific residence-time analysis.

## Hard Exclusion Criteria

A zone is excluded if any of the following apply.

### 1. Depth Exclusion

Exclude:

- water depth less than 1,000 m,
- continental shelf,
- shallow bank,
- shelf edge where deposition could spread onto shallow habitat,
- slope zones where biomass could concentrate unpredictably.

### 2. Oceanographic Exclusion

Exclude:

- strong upwelling zones,
- rapid return pathways to surface waters,
- highly energetic mixing zones,
- regions where residence-time modeling suggests fast atmospheric return.

### 3. Oxygen Exclusion

Exclude:

- oxygen-stressed waters,
- oxygen minimum zones unless specifically justified and permitted,
- locations where added organic load could create unacceptable oxygen depletion.

### 4. Ecological Exclusion

Exclude:

- protected marine areas,
- known sensitive benthic habitats,
- coral, sponge, seamount, or unique benthic ecosystems,
- key nursery or migratory areas where vessel operation or sinking would create unacceptable harm.

### 5. Legal and Governance Exclusion

Exclude:

- areas with no plausible permitting pathway,
- disputed jurisdiction zones,
- areas where relevant authorities reject the activity,
- areas where public review cannot occur.

### 6. MRV Exclusion

Exclude:

- areas where treated biomass cannot be tracked,
- areas where sinking cannot be verified,
- areas where baseline and control observations are infeasible,
- areas where benthic or water-column monitoring is impossible at the required scale.

### 7. Avoided-Harm Exclusion

Exclude:

- sargassum patches with no evidence of likely coastal harm,
- patches unlikely to beach or create nearshore decomposition problems,
- areas where sinking does not improve the counterfactual fate of the biomass.

## Desirability Criteria

Zones that pass the exclusion filters should be scored for desirability.

### Depth Score

| Depth | Score | Interpretation |
|---:|---:|---|
| <1,000 m | Excluded | No in situ sinking. |
| 1,000–2,000 m | 1 | Research-only candidate. |
| 2,000–3,000 m | 2 | Conditional pilot candidate. |
| >3,000 m | 3 | Preferred depth class, if other filters pass. |

### Sargassum Density Score

| Condition | Score |
|---|---:|
| Sparse / intermittent biomass | 0 |
| Moderate patch density | 1 |
| Recurring dense patch field | 2 |
| Dense patch field with forecastable recurrence | 3 |

### Avoided Coastal Harm Score

| Condition | Score |
|---|---:|
| No evidence patch would cause coastal harm | 0 |
| Weak drift evidence | 1 |
| Moderate drift evidence | 2 |
| Strong drift evidence linked to affected coastlines | 3 |

### Residence-Time Score

| Condition | Score |
|---|---:|
| Unknown or fast return risk | 0 |
| Uncertain but potentially favorable | 1 |
| Modeled slow return | 2 |
| Validated slow-return pathway | 3 |

### Oxygen and Benthic Score

| Condition | Score |
|---|---:|
| Oxygen or benthic risk high | 0 |
| Risk uncertain | 1 |
| Risk likely manageable | 2 |
| Risk low and monitorable | 3 |

### MRV Feasibility Score

| Condition | Score |
|---|---:|
| Monitoring infeasible | 0 |
| Minimal surface tracking only | 1 |
| Surface plus water-column monitoring feasible | 2 |
| Surface, water-column, and benthic monitoring feasible | 3 |

### Legal / Governance Score

| Condition | Score |
|---|---:|
| No plausible permission | 0 |
| Legally unclear | 1 |
| Research permit plausible | 2 |
| Strong research-governance partner and review pathway | 3 |

### Port / Operations Score

| Condition | Score |
|---|---:|
| Very distant or unsupported | 0 |
| Reachable but operationally difficult | 1 |
| Reachable from plausible base | 2 |
| Near strong base with maintenance/resupply support | 3 |

## Zone Classes

After exclusions, score zones across the desirability criteria.

| Class | Score Range | Meaning |
|---|---:|---|
| Class 0 | Any exclusion triggered | No-sink zone. |
| Class 1 | 1–7 | Low desirability / research only. |
| Class 2 | 8–13 | Conditional candidate. |
| Class 3 | 14–18 | Strong pilot candidate. |
| Class 4 | 19+ | Preferred operational candidate, pending legal and scientific review. |

The scoring scale is provisional. It should be revised as data sources improve.

## Required Data Layers

A GIS-backed screening map should include:

- bathymetry,
- 1,000 m depth contour,
- 2,000 m depth contour,
- 3,000 m depth contour,
- continental shelf and slope masks,
- sargassum density or probability layers,
- drift forecasts,
- surface currents,
- mixed-layer depth,
- upwelling indicators,
- oxygen conditions,
- protected areas,
- benthic habitat sensitivity,
- EEZ and jurisdiction boundaries,
- candidate ports,
- vessel range or steaming-distance bands,
- feasible MRV access zones.

## Candidate Port Categories

Ports should be classified as support nodes, not commitments.

### Western Candidate Support Nodes

- Bridgetown, Barbados
- Fort-de-France, Martinique
- Pointe-à-Pitre, Guadeloupe

### Eastern Candidate Support Nodes

- Praia, Cape Verde
- Mindelo, Cape Verde
- Dakar, Senegal

### Northern Maintenance / Staging Node

- Las Palmas, Canary Islands

Each port should eventually be scored for:

- distance to candidate zones,
- fuel and maintenance capacity,
- vessel repair capacity,
- customs and permitting practicality,
- scientific or regulatory partnership potential,
- weather and seasonal access,
- crew rotation feasibility.

## Operational Rules

### Rule 1: No Sink Below the Floor

No in situ sinking in water shallower than 1,000 m.

### Rule 2: Preferred Depth Is Deeper Than the Floor

Pilot planning should prefer 2,000–3,000 m or deeper, assuming other criteria pass.

### Rule 3: Avoid Shelf and Slope Deposition

Do not sink on shelves, shelf edges, or unstable slope zones unless a specific scientific reason exists and regulators approve.

### Rule 4: Depth Does Not Override Ecology

Deep water does not make benthic impact irrelevant.

### Rule 5: No MRV, No Claim

No carbon-storage claim may be made from a zone where sinking, depth reached, residence time, and ecological effects cannot be monitored.

### Rule 6: Avoided Harm Must Be Demonstrated

The project should prioritize sargassum likely to cause coastal harm if untreated.

### Rule 7: Law Comes First

A zone with no plausible research-permitting pathway is not a pilot candidate, regardless of technical desirability.

## First Map Objective

The first map should not claim to identify deployment sites.

It should identify:

- obvious no-sink areas,
- plausible candidate zones,
- uncertainty areas,
- candidate ports,
- data gaps.

The map should be titled as a preliminary screening map.

## Research Questions

- Is 1,000 m sufficient as a minimum floor, or should the floor be 2,000 m?
- How should residence time be weighted against absolute depth?
- Which bathymetric regions under recurring sargassum patches pass the exclusion filters?
- Which candidate ports create the lowest operating-emissions burden?
- Can candidate zones be monitored cheaply enough for credible MRV?
- How should benthic deposition be spread to avoid concentrated organic loading?
