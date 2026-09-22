---
title: FedTransferAD
summary: Federated cross-system microservice anomaly detection with semantic metric
  harmonization. Submitted to ICECE 2026.
show_date: false
reading_time: false
share: false
profile: false
---

**Federated Cross-System Microservice Anomaly Detection with Semantic Metric Harmonization**

<span class="status-label">Submitted · ICECE 2026</span>

Submitted to the [14th International Conference on Electrical and Computer Engineering](https://icece.org.bd/2026/), BUET, Dhaka. This is a submitted manuscript; acceptance and publication are not yet confirmed.

[Read the submitted manuscript (PDF) →]({{< relref "/" >}}uploads/FedTransferAD_ICECE2026.pdf)

## Research question

Can a lightweight federated anomaly detector transfer to a microservice application that never participates in classifier training, even when raw metric names and service counts differ?

## Approach

FedTransferAD maps raw telemetry into seven semantic metric families and summarizes them as a shared 21-dimensional representation. Two source applications train a 22-parameter logistic classifier using sample-weighted Federated Averaging. A third application is held out from classifier training.

The first 25% of each trace supplies a healthy reference for local median/MAD normalization and is excluded from training and evaluation. The target contributes no labels, model updates, or tuning decisions to training. Linear SHAP explains the saved model’s predictions.

## Reported results

The manuscript evaluates the metric-only RCAEval RE1 suite across Online Boutique, Sock Shop, and Train Ticket. Values below are means across three held-out targets, with each target evaluated over three SGD seeds.

| Method | F1 | ROC-AUC | Average precision |
| --- | ---: | ---: | ---: |
| FedTransferAD | 0.8905 | 0.9413 | 0.9601 |
| Centralized pooled baseline | 0.9009 | 0.9395 | 0.9511 |

Federated training remains close to centralized training in F1, with slightly higher ranking metrics in this evaluation. It does not outperform every baseline on every target.

## Scope and limitations

The study uses three benchmark applications and assumes a known-healthy target reference window. Metric mapping is rule-based. The three seeds measure optimization variability on a fixed split, not independent dataset replications. SHAP explains model attribution rather than causal root causes; keeping raw data local is not a formal privacy guarantee.
