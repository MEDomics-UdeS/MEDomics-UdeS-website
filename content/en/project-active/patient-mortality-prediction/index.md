---
title: "Project: Prediction of patient mortality"

type: book

authors:
  - Hakima Laribi
  - Martin Vallières
---

## Status

In progress (2022-today)

## Type

Doctorate

## Team

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})<sup>1</sup> (2022-aujourd'hui)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (2022-aujourd'hui)

<sup>1</sup> Computer science department, Université de Sherbrooke, Sherbrooke (QC), Canada

![Project presentation](project.png "Project presentation")

## Description

A goal of care discussion GOC is a communication process that takes place in a hospital setting between a clinician and a patient at the end of life. The purpose of a GOC discussion is to determine the types of care to be administered to the patient so as not to result in more aggressive cares than desired. Nevertheless, the prognoses established by doctors only gaining certainty over time constitute the main constraint delaying the initiation of a GOC discussion. Therefore, the automatic identification of the patients at the end of life when admitted to the hospital would increase the chances to carry out a GOC discussion on time. In this sense, a model based on random forests [R. Taseen, 2021] which attempts to predict patient mortality in the year following their admission to hospital has already been developed. Although the trees constituting the random forests expose relevant informations about the importance of each predictor, no relationship between the patients can be learned. Consequently, we propose a solution based on graphical neural networks for the prediction of patient mortality in the year following their hospital admission. Thus, the predictions at patient level will be made according to all the neighboring and the results obtained can be explained by consulting the connections of the patient. This graph-based approach would infer relationships between patients and thus add interpretability and performance to a model based on random forests.

**Objectives:** 

- Model data graphically to learn connections between patients.
- Develop a prediction method based on graphical neural networks to identify patients with a high risk of mortality.

**Expected results:**

- Improve the precision and accuracy of prediction with a solution based on graphical neural networks.
- A post analysis and interpretation of the results.
