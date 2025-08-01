---
title: "Project: Predictive Performance Precision Analysis in Medicine (MED3pa)"

type: book

authors:
  - Olivier Lefebvre
  - Ludmila Amriou
  - Lyna Hiba Chikouche
  - Martin Vallières
---

  ![Method overview](res_meto.svg "Method overview")

## Status

In progress (2021-today)

## Type

Doctorate

## Team

- [Olivier Lefebvre]({{< relref "/authors/olivier-lefebvre" >}})<sup>1</sup> (2021-today)
- [Félix Camirand Lemyre](https://www.usherbrooke.ca/mathematiques/nous-joindre/personnel/corps-professoral/professeurs/felix-camirand-lemyre)<sup>2</sup> (2021-2025)
- [Jean-François Éthier](https://www.usherbrooke.ca/recherche/specialistes/details/jean-francois.ethier)<sup>3</sup> (2021-2025)
- [Ludmila Amriou]({{< relref "/authors/ludmila-amriou" >}})<sup>1</sup> (2024-2025)
- [Lyna Hiba Chikouche]({{< relref "/authors/Lyna-Hiba-Chikouche" >}})<sup>1</sup> (2024-2025)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (2021-today)

<sup>1</sup> Computer science department, Université de Sherbrooke, Sherbrooke (QC), Canada

<sup>2</sup> Mathematics department, Université de Sherbrooke, Sherbrooke (QC), Canada

<sup>3</sup> Medicine department, Université de Sherbrooke, Sherbrooke (QC), Canada

## Description

While predictive models are widely used in healthcare, they often fail to indicate when their predictions should not be trusted. This can lead to critical errors, especially when applied to diverse patient populations. Global performance metrics can mask important variations in reliability across individual patients or subgroups with shared attributes, called patient profiles.

To address this, the MED3pa project introduces a methodology to identify and characterize low-confidence predictions. Instead of using static confidence thresholds or global calibration metrics, the approach uses secondary models that learn from the base model’s errors to predict where it is likely to misclassify. These models — including the Individualized Predictive Confidence (IPC), Aggregated Predictive Confidence (APC), and Mixed Predictive Confidence (MPC) models — produce a confidence score per patient, helping to flag predictions that are more likely erroneous.

The method is validated across multiple datasets: simulated data for conceptual validation, two public clinical datasets (MIMIC-IV and eICU-CRD), and a private real-world hospital dataset. A key evaluation framework called Metrics by Declaration Rate (MDR) is used to analyze how predictive performance changes when the least confident predictions are excluded. This helps assess the benefit of restricting model use to patients for whom the model is more trustworthy.

Overall, the goal is not only to improve predictive accuracy but also to enhance clinical safety by identifying patient profiles where models perform poorly. 



## Objectives

  1. Investigation of model prediction confidence and identification of profiles on which the model has low-confidence predictions. 
  2. Explanation of low-confidence predictions underlying sources.
  3. Improvement of patient coverage through mitigation of low-confidence sources.
