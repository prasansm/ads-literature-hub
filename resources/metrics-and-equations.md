# Metrics and equations

Let `I` be impressions, `K` clicks, `C` conversions, `S` spend, and `V` conversion value.

## Funnel and business metrics

| Metric | Equation | Meaning |
|---|---:|---|
| CTR | `K / I` | Clicks per impression |
| CVR | `C / K` | Post-click conversions per click |
| Conversion rate per impression | `C / I = pCTR × pCVR` | Joint click-and-conversion probability |
| CPM | `1000 × S / I` | Cost per thousand impressions |
| CPC | `S / K` | Cost per click |
| CPA | `S / C` | Cost per conversion |
| ROAS | `V / S` | Conversion value per unit of spend |
| RPM | `1000 × platform revenue / I` | Platform revenue per thousand impressions |
| Win rate | `auctions won / auctions entered` | Auction competitiveness |
| Fill rate | `impressions served / eligible opportunities` | Inventory utilization |
| Frequency | `impressions / reached users` | Exposures per reached user |

## Ranking objectives

For a CPC bid, a simplified quality-adjusted score is:

```text
score = pCTR × CPC_bid × quality
```

For a CPA bid:

```text
score = pCTR × pCVR × CPA_bid × quality
```

For conversion-value optimization:

```text
expected_value_per_impression
  = pCTR × pCVR × E[conversion_value | conversion]
```

The production objective often also needs calibration, position and examination effects, ad and landing-page quality, predicted negative experience, auction and pricing rules, budgets and pacing, diversity, policy constraints, latency, uncertainty, and long-term marketplace effects. These are not all best represented as simple multiplicative factors; some belong in eligibility, constraints, re-ranking, or the auction.

## Incrementality

```text
incremental_conversion_probability
  = P(conversion | ad shown, context)
  - P(conversion | ad not shown, context)
```

`pCVR` predicts conversion among clicked or exposed users; it does not by itself prove the ad caused the conversion.

## Funnel decomposition

```text
opportunities
  → eligible
  → participated
  → won
  → rendered
  → viewable
  → clicked
  → converted
```

One diagnostic identity is:

```text
conversions
  = opportunities
  × eligibility_rate
  × participation_rate
  × win_rate
  × render_rate
  × viewability_rate
  × pCTR
  × pCVR
```

## Official definitions

- [Google Ads: CTR](https://support.google.com/google-ads/answer/2615875?hl=en)
- [Google Ads: Ad Rank](https://support.google.com/google-ads/answer/1752122?hl=en)
- [Google Ads: bidding](https://support.google.com/google-ads/faq/10286469?hl=en)
- [Google Ads: impression share](https://support.google.com/google-ads/answer/2497703?hl=en-419)
- [IAB Click Measurement Guidelines](https://www.iab.com/guidelines/click-measurement-guidelines/)
- [IAB Ad Impression Measurement Guidelines](https://www.iab.com/guidelines/ad-impression-measurement-guidelines-us-global/)
- [IAB/MRC Retail Media Measurement Guidelines](https://www.iab.com/wp-content/uploads/2024/01/IAB_Retail_Media_Measurement_Guidelines_January2024.pdf)

[Back to the hub](../README.md)
