# Bidding, budgeting, and pacing

These systems choose how aggressively to participate and distribute finite advertiser budgets across traffic, time, campaigns, and opportunities.

## Core papers

- [Budget Optimization in Search-Based Advertising Auctions](https://arxiv.org/abs/cs/0612052) — Feldman et al., *ACM EC 2007*. Bid optimization under advertiser budget constraints. `seminal`
- [Bid Optimization in Broad-Match Ad Auctions](https://research.google/pubs/bid-optimization-in-broad-match-ad-auctions/) — Even-Dar et al., 2009. Optimization when keywords match multiple query classes.
- [Handling Forecast Errors While Bidding for Display Advertising](https://research.google/pubs/handling-forecast-errors-while-bidding-for-display-advertising/) — Lang, Moseley, and Vassilvitskii, *WWW 2012*. Robust bidding under traffic and outcome forecast uncertainty.
- [Budget Pacing for Targeted Online Advertisements at LinkedIn](https://www0.cs.ucl.ac.uk/staff/w.zhang/rtb-papers/linkedin-pacing.pdf) — Agarwal et al., *KDD 2014*. Global budget pacing layered over local auction decisions. `production`
- [AdWords and Generalized Online Matching](https://people.eecs.berkeley.edu/~vazirani/pubs/adwords.pdf) — Mehta et al., *JACM 2007*. The theoretical foundation for online budgeted allocation. `seminal`

## System questions

- Bid strategy: CPC, CPA, ROAS, value, or incremental-value objectives
- Hard versus soft budgets and campaign-level constraints
- Smooth delivery versus opportunity-sensitive spend
- Traffic, price, conversion, and value forecasting
- Cold start, seasonality, delayed feedback, and non-stationarity
- Coupling between bidder, ranker, auction, and pacing controller

[Back to the hub](../README.md)
