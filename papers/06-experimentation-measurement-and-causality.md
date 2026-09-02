# Experimentation, measurement, and causality

Prediction asks what will happen; ads measurement asks what happened because the ad was shown. The distinction is central to bidding, attribution, and advertiser value.

## Causal foundations and online experiments

- [Counterfactual Reasoning and Learning Systems: The Example of Computational Advertising](https://www.jmlr.org/papers/v14/bottou13a.html) — Bottou et al., *JMLR 2013*. Causal reasoning, importance weighting, policy-generated data, and feedback loops. `seminal`
- [The Unfavorable Economics of Measuring the Returns to Advertising](https://academic.oup.com/qje/article-abstract/130/4/1941/1914592) — Lewis and Rao, *QJE 2015*. Explains why advertising lift often requires enormous experiments. `seminal`
- [Ghost Ads: Improving the Economics of Measuring Online Ad Effectiveness](https://journals.sagepub.com/doi/10.1509/jmr.15.0297) — Johnson, Lewis, and Nubbemeyer, *Journal of Marketing Research 2017*. Constructs auction-aware experimental control groups.
- [A Comparison of Approaches to Advertising Measurement](https://www.kellogg.northwestern.edu/faculty/gordon_b/files/fb_comparison.pdf) — Gordon et al., *Marketing Science 2019*. Compares observational estimates with randomized advertising experiments.

## Attribution and incrementality

- [A Causal Framework for Digital Attribution](https://research.google/pubs/a-causal-framework-for-digital-attribution/) — Kelly, Vaver, and Koehler, 2018. Frames attribution as a causal decision problem.
- [Incrementality Bidding and Attribution](https://arxiv.org/abs/2208.12809) — Lewis and Wong. Connects causal lift, bidding, attribution, and experimentation.
- [Robust Causal Inference for Incremental ROAS with Randomized Paired Geo Experiments](https://research.google/pubs/robust-causal-inference-for-incremental-return-on-ad-spend-with-randomized-paired-geo-experiments/) — Chen and Au, *Annals of Applied Statistics 2022*. Geo-experiment design and robust iROAS estimation.
- [Bias Correction for Paid Search in Media Mix Modeling](https://research.google/pubs/bias-correction-for-paid-search-in-media-mix-modeling/) — Chen et al., 2018. Addresses search-ad targeting bias in observational media-mix models.

## Evaluation checklist

Track randomization unit, interference, auction effects, novelty, power, delayed conversions, multiple testing, guardrails, sample-ratio mismatch, and practical significance—not only p-values.

[Back to the hub](../README.md)
