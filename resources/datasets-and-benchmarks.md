# Datasets and benchmarks

Public ads datasets are usually anonymized and narrower than production data. Check each dataset's license and terms before use.

## Click and conversion prediction

- [Criteo AI Lab datasets](https://ailab.criteo.com/ressources/) — Includes large-scale display-ad click logs and research datasets.
- [Criteo Uplift Prediction Dataset](https://ailab.criteo.com/criteo-uplift-prediction-dataset/) — Treatment, exposure, visit, and conversion labels for uplift and incrementality research.
- [Avazu CTR Prediction](https://www.kaggle.com/c/avazu-ctr-prediction) — Ten days of mobile-ad click data used for CTR-modeling benchmarks.
- [KDD Cup 2012](https://www.kdd.org/kdd-cup/view/kdd-cup-2012-track-2) — Search-ad CTR prediction from Tencent-sponsored-search logs.

## Evaluation guidance

For response models, report both discrimination and calibration. Common measures include log loss, normalized entropy, ROC-AUC or PR-AUC, expected calibration error, calibration plots, and slice-level performance.

Offline ranking metrics do not establish marketplace or causal impact. When possible, pair them with randomized online measures such as incremental conversions, advertiser value, revenue, latency, user guardrails, budget delivery, and long-term effects.

Avoid random row splits when the real deployment predicts future traffic. Prefer chronological splits and document label delay, leakage controls, negative down-sampling, and any correction applied during calibration.

[Back to the hub](../README.md)
