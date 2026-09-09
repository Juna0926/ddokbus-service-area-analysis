# Public Project Outputs

## Source artifacts reviewed

- IE Machine Learning course presentation: `Proposal for Expanding the Service Area of Ddok-Bus in Gyeonggi Province`
- Big Data Systems final report: `경기도 내 똑버스 서비스 입지분석 - PySpark 기반 머신러닝 분류 모델을 활용한 신규 서비스 구역 도출`

## Current authoritative framing

The Portfolio entry represents the **Mar. 2025 - Jun. 2025 main project**:

**demographic + infrastructure + existing-service data → machine-learning suitability analysis → candidate DRT service areas**.

The repository preserves later analytical extensions, but those results are kept separate from the 2025 Portfolio entry so that metrics from different data designs are not mixed.

## Portfolio-aligned representative figure

- Portfolio source: `Juna0926/Portfolio/assets/media/project-drt-detail.webp`
- The README displays this figure as the primary visual summary of the current Portfolio framing.

## Public file

- [`ddokbus-project-public-excerpt.pdf`](ddokbus-project-public-excerpt.pdf) — concise public-safe technical excerpt summarizing model results, probability-ranking interpretation, and spatial review logic.

## Supporting repository evidence

- `assets/figure-01-model-results.svg` — metrics from the later analytical extension.
- `assets/figure-02-probability-map.svg` — probability-ranking and spatial-screening workflow.
- `assets/figure-03-candidate-site.svg` — multi-criteria candidate-review logic.

## Version and result provenance

### Main Portfolio project — Mar. 2025 to Jun. 2025

The Portfolio uses the original service-expansion problem and decision-support framing as the primary project narrative. An earlier project-stage experiment reported AUC **0.70349** under its own setup.

### Later Big Data Systems extension

A later extension used a **1 km × 1 km grid** representation and reported:

- Accuracy: **0.7866**
- Precision: **0.7518**
- Recall: **0.1936**
- F1-score: **0.3079**
- ROC-AUC: **0.6531**

Because the datasets, spatial representation, and analysis design differ, these values are **not a before/after performance comparison**.

## Decision-support note

Model probability is treated as a screening signal for candidate service areas, not an automatic deployment decision. Real-world implementation would additionally require road-network feasibility, demand validation, fleet / operating-cost review, and local policy assessment.

## Public-report cleanup

The working report contained draft comments and student identifiers. The public repository uses a cleaned technical excerpt with those internal drafting notes and identifiers removed.

## Data note

Raw/intermediate spatial datasets are not redistributed because the project integrates several third-party public-data sources with distinct update cycles and usage terms.
