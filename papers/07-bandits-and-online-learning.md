# Bandits and online learning

Bandits are useful when the serving policy must deliberately collect information—such as learning about a new creative—while limiting opportunity cost. They are not a replacement for the auction score.

## Core reading

- [A Contextual-Bandit Approach to Personalized News Article Recommendation](https://arxiv.org/abs/1003.0146) — Li, Chu, Langford, and Schapire, *WWW 2010*. LinUCB, contextual exploration, and replay evaluation. `seminal`
- [Contextual Multi-Armed Bandits for Causal Marketing](https://arxiv.org/abs/1810.01859) — 2018. Contextual Thompson sampling and off-policy evaluation for marketing treatments.
- [Improved Online Learning Algorithms for CTR Prediction in Ad Auctions](https://research.google/pubs/improved-online-learning-algorithms-for-ctr-prediction-in-ad-auctions/) — Feng, Liaw, and Zhou, *ICML 2023*. Studies CTR learning, UCB mechanisms, regret, and strategic advertisers.
- [Diversity Driven Query Rewriting in Search Advertising](https://www.microsoft.com/en-us/research/publication/diversity-driven-query-rewriting-in-search-advertising/) — Yao et al., *KDD 2021*. A production example of exploration in query-rewrite selection.

## Where bandits fit

Given context `x` and candidate ad `a`, keep the economic score and add an exploration policy:

```text
base_score(a, x) = bid(a) × predicted_outcome(a, x) × quality(a, x)

UCB_score(a, x) = base_score(a, x) + β × uncertainty(a, x)
```

With Thompson sampling, sample uncertain model parameters, compute the ordinary score using that sampled model, then run the auction. Exploration must respect eligibility, policy, budget, pacing, and user-experience constraints.

Good use cases include cold-start ads, creative selection, query rewrites, and learning under sparse feedback. Pure exploitation is usually sufficient when uncertainty is low or experimentation risk is high.

[Back to the hub](../README.md)
