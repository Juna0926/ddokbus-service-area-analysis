# Public Project Outputs

## Source artifacts reviewed

- IE Machine Learning course presentation: `Proposal for Expanding the Service Area of Ddok-Bus in Gyeonggi Province`
- Big Data Systems final report: `경기도 내 똑버스 서비스 입지분석 - PySpark 기반 머신러닝 분류 모델을 활용한 신규 서비스 구역 도출`

## Public-safe evidence included

- `assets/figure-01-model-results.svg` — 2026 XGBoost validation metrics.
- `assets/figure-02-probability-map.svg` — probability-ranking and spatial-screening workflow.
- `assets/figure-03-candidate-site.svg` — final multi-criteria candidate-review logic.

## Version note

The earlier IE Machine Learning presentation reported **AUC 0.70349** under an earlier project setup. The 2026 Big Data Systems report later reported Accuracy 0.7866, Precision 0.7518, Recall 0.1936, F1 0.3079, and ROC-AUC 0.6531. Because the analysis stages and data design differ, these values are **not presented as a direct before/after model improvement**.

## Public-report cleanup

The working report contained draft comments and student identifiers. A cleaned public copy was prepared separately with those internal drafting notes removed. The repository README and figures use only the cleaned analytical content.

## Data note

Raw/intermediate grid datasets are not redistributed because the project integrates several third-party public-data sources with distinct update cycles and usage terms.
