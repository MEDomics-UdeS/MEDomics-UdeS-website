---
title: "Presentation : Precision analysis of predictive uncertainty of machine learning models in medical context"
date: 2022-10-20
image:
  focal_point: 'top'

type: book

authors:
  - Olivier Lefebvre

categories: Presentations
where: CIRIUS
---

![CIRIUS](cirius-blanc.png)

## Date

2022-10-20

## Authors

- [Olivier Lefebvre]({{< relref "/authors/olivier-lefebvre" >}})

## Summary

Machine learning is increasingly used in a variety of applications. Machine learning 
  models can be used as decision support tools in critical contexts, such as the medical field. 
  However, it is often complicated to explain the results obtained by a prediction model. 
  It is therefore important that the models are interpretable in order to understand the decisions 
  made by the model and to properly guide users. In this sense, there are various methods to add 
  interpretability to models, such as the SHAP method [S. Lundberg, 2017] that estimates the impact 
  of each attribute on the model prediction. However, when it comes to the performance of a model, 
  the classical method is to simply apply said model on a set of tests, and then calculate global 
  metrics such as accuracy or even the area under the ROC curve. However, these measures do not 
  explain how the model will perform for each individual patient. Indeed, some subgroups of patients 
  may be less well represented by a model, and the overall performance does not allow to detect this. 
  For example, a mortality prediction model trained mainly with medical data from older patients may 
  perform less well for younger patients. We therefore propose the concept of patient-conditional 
  performance. A prediction model would predict an outcome for a patient (e.g., survives or dies), 
  as well as a probability that the prediction provided is wrong. Users would then be better equipped 
  to detect when the model is potentially aberrant and thus make better use of it. This approach would 
  also allow us to identify subgroups of patients for whom our model performs less well, and therefore 
  potentially not use the model for these patients.

## Poster
  ![Poster](cirius-ol.png)

## Links

- [Event Details](https://www.dropbox.com/s/qshut4vilvaja93/Programmation_Cirius_JS_2022.pdf?dl=0)
- [CIRIUS website](https://cirius.ca/)
