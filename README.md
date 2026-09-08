# Proposal for Expanding DRT Service Areas in Gyeonggi Province

> A public-data machine-learning framework for identifying candidate areas for demand-responsive transit (DRT) service expansion.

**Main project period:** Mar. 2025 - Jun. 2025  
**Domain:** Transportation data analysis  
**Core methods:** XGBoost · Public data · Geospatial analysis  
**Decision target:** Candidate DRT service areas

---

## Overview

This project analyzed where demand-responsive transit service could be expanded in Gyeonggi Province. The core idea was to learn the characteristics of currently served areas from demographic, infrastructure, and existing-service data, then identify unserved areas with similar characteristics as candidate DRT service zones.

The model output was treated as a **decision-support signal**, not as an automatic deployment rule. Candidate areas were interpreted together with surrounding infrastructure, spatial context, and existing transport-service structure.

## Problem

Fixed-route public transportation is not equally effective in all areas, especially where demand is spatially dispersed or accessibility is limited. Because DRT operates within predefined service zones, service expansion becomes a spatial prioritization problem involving population needs, public facilities, mobility infrastructure, and existing service coverage.

## Data & features

The project integrated public-data variables such as:

- Senior population
- Medical / welfare facilities
- Daily-life infrastructure
- Bus stops and existing transport access
- Businesses / factories
- Existing DRT service information
- Other local demographic and infrastructure indicators

## Modeling framework

1. Construct spatial analysis units from public geospatial data.
2. Integrate demographic, infrastructure, and existing-service variables.
3. Train an **XGBoost** classifier to learn the characteristics associated with currently served areas.
4. Estimate service-area suitability for unserved locations.
5. Rank candidate areas using model probability.
6. Review high-priority locations using surrounding spatial and policy context.

## Main analytical interpretation

The project used machine-learning output to identify **candidate DRT service areas** rather than treating prediction probability as a final policy decision. The intended use is to narrow the search space for planners before operational feasibility review.

![Model results](assets/figure-01-model-results.svg)

![Probability-ranking workflow](assets/figure-02-probability-map.svg)

![Candidate-site review](assets/figure-03-candidate-site.svg)

## Repository note: later analytical extension

This repository also documents a later Big Data Systems extension of the same decision problem. That extension used a 1 km × 1 km grid representation and reported the following XGBoost metrics:

| Metric | Value |
|---|---:|
| Accuracy | 0.7866 |
| Precision | 0.7518 |
| Recall | 0.1936 |
| F1-score | 0.3079 |
| ROC-AUC | 0.6531 |

An earlier project-stage experiment reported AUC **0.70349** under a different setup. Because the data and analysis design differ across stages, these values are presented separately rather than as a direct before-after comparison.

## Limitations

Model probability alone is not sufficient for real-world DRT deployment. Road-network feasibility, actual travel demand, operating cost, fleet availability, local policy constraints, and field validation would still be required.

## Public outputs

- [`outputs/ddokbus-project-public-excerpt.pdf`](outputs/ddokbus-project-public-excerpt.pdf) - public-safe technical excerpt covering the analysis and decision framing.
- [`outputs/PROJECT_OUTPUTS.md`](outputs/PROJECT_OUTPUTS.md) - source provenance, version notes, and verified analytical evidence.

---

**Junha Won** · Ajou University  
[Portfolio detail](https://juna0926.github.io/Portfolio/projects/ddokbus.html) · [Portfolio](https://juna0926.github.io/Portfolio/) · [GitHub](https://github.com/Juna0926)
