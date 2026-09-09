# Proposal for Expanding DRT Service Areas in Gyeonggi Province

> A public-data machine-learning framework for identifying candidate areas for demand-responsive transit (DRT) service expansion.

**Main project period:** Mar. 2025 - Jun. 2025  
**Domain:** Transportation data analysis  
**Core methods:** XGBoost · Public data · Geospatial analysis  
**Decision target:** Candidate DRT service areas

---

## Overview

This project analyzed where **Demand Responsive Transit (DRT)** service could be expanded in Gyeonggi Province.

The analysis integrated demographic, infrastructure, and existing-service information and used machine learning to estimate **DRT service-expansion suitability** for currently unserved areas.

The portfolio framing is intentionally decision-oriented:

**demographic + infrastructure + existing-service data → machine-learning suitability analysis → candidate DRT service areas**.

## Portfolio-aligned main figure

![DRT service-area expansion analysis](https://raw.githubusercontent.com/Juna0926/Portfolio/main/assets/media/project-drt-detail.webp)

*Representative figure synchronized with the current Portfolio detail page.*

## Problem

Fixed-route public transportation is not equally effective in all areas, particularly where demand is spatially dispersed or accessibility is limited.

Because DRT operates within predefined service zones, expansion can be framed as a spatial prioritization problem: identify locations whose demographic and infrastructure characteristics suggest that flexible transport service may be useful, then review those candidates with operational and policy context.

## Data

The project integrated public-data variables including:

- senior population
- medical / welfare facilities
- daily-life infrastructure
- bus stops and existing transport access
- businesses / factories
- existing DRT service information
- other local demographic and infrastructure indicators

## Modeling framework

1. Construct spatial analysis units from public geospatial data.
2. Integrate demographic, infrastructure, and existing-service variables.
3. Compare candidate machine-learning models.
4. Use **XGBoost** to estimate DRT service-area suitability.
5. Rank unserved locations using model output.
6. Review high-priority candidate areas using surrounding spatial and policy context.

## Decision-support interpretation

The model output was treated as a **screening and prioritization signal**, not as an automatic deployment rule.

The intended use is to narrow the search space for planners before reviewing road-network feasibility, actual demand, operating cost, fleet availability, and local policy constraints.

## Supporting repository figures

![Model results](assets/figure-01-model-results.svg)

![Probability-ranking workflow](assets/figure-02-probability-map.svg)

![Candidate-site review](assets/figure-03-candidate-site.svg)

## Repository note: later analytical extension

The main portfolio entry represents the **Mar. 2025 - Jun. 2025 project**. This repository also preserves a later Big Data Systems extension of the same decision problem.

That later extension used a 1 km × 1 km grid representation and reported:

| Metric | Value |
|---|---:|
| Accuracy | 0.7866 |
| Precision | 0.7518 |
| Recall | 0.1936 |
| F1-score | 0.3079 |
| ROC-AUC | 0.6531 |

An earlier project-stage experiment reported AUC **0.70349** under a different setup. Because the data and analysis design differ across stages, these results are intentionally kept separate and are **not interpreted as a direct before-after comparison**.

## Limitations

- Model probability does not establish actual transportation demand.
- Road-network feasibility and fleet operations were not fully represented.
- Public datasets differ in spatial resolution and update cycle.
- Field validation and local policy review are required before deployment.

## Public outputs

- [`outputs/ddokbus-project-public-excerpt.pdf`](outputs/ddokbus-project-public-excerpt.pdf) — public-safe technical excerpt covering the analysis and decision framing.
- [`outputs/PROJECT_OUTPUTS.md`](outputs/PROJECT_OUTPUTS.md) — source provenance, version notes, and verified analytical evidence.

---

**Junha Won** · Ajou University  
[Portfolio detail](https://juna0926.github.io/Portfolio/projects/ddokbus.html) · [Portfolio](https://juna0926.github.io/Portfolio/) · [GitHub](https://github.com/Juna0926)