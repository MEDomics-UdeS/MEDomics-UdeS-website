---
title: "Paper: Development of Error Passing Network for Optimizing the Prediction of VO2 peak in Childhood Acute Leukemia Survivors"
date: 2024-06-27
image:
  focal_point: 'top'

type: book

authors:
  - Nicolas Raymond
  - Hakima Laribi
  - Mehdi Mitiche
  - Martin Vallières
---

![PMLR](featured.png)

## Date

2024-06-27

## Authors

- [Nicolas Raymond]({{< relref "/authors/nicolas-raymond" >}})<sup>1</sup>
- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})<sup>1</sup>
- Maxime Caru<sup>2,3</sup>
- [Mehdi Mitiche]({{< relref "/authors/mehdi-mitiche" >}})<sup>1</sup>
- Valérie Marcil<sup>4</sup>
- Maja Krajinovic<sup>4</sup>
- Daniel Curnier<sup>4</sup>
- Daniel Sinnett<sup>4</sup>
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1,5</sup>

<sup>1</sup> Department of Computer Science, Université de Sherbrooke, Sherbrooke (QC), Canada

<sup>2</sup> Department of Pediatrics, Division of Hematology and Oncology, Pennsylvania State Health Children’s Hospital, Hershey (PA), USA

<sup>3</sup> Department of Public Health Sciences, Penn State University College of Medicine, Hershey (PA), USA

<sup>4</sup> Research Center, Sainte Justine University Health Center, Université de Montréal, Montreal (QC), Canada

<sup>5</sup> Centre de recherche du Centre hospitalier universitaire de Sherbrooke, Sherbrooke (QC), Canada

## Abstract

Approximately two-thirds of survivors of childhood acute lymphoblastic leukemia (ALL) cancer develop late adverse effects post-treatment. Prior studies explored prediction models for personalized follow-up, but none integrated the usage of neural networks to date. In this work, we propose the Error Passing Network (EPN), a graph-based method that leverages relationships between samples to propagate residuals and adjust predictions of any machine learning model. We tested our approach to estimate patients’ \vo peak, a reliable indicator of their cardiac health. We used the EPN in conjunction with several baseline models and observed up to 12.16% improvement in the mean average percentage error compared to the last established equation predicting \vo peak in childhood ALL survivors. Along with this performance improvement, our final model is more efficient considering that it relies only on clinical variables that can be self-reported by patients, therefore removing the previous need of executing a resource-consuming physical test.

## Links

- [Paper in journal](https://proceedings.mlr.press/v248/raymond24a.html)
- [Paper in PDF version](https://raw.githubusercontent.com/mlresearch/v248/main/assets/raymond24a/raymond24a.pdf)
