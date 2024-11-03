---
title: "Paper: Multi-task Bayesian Model Combining FDG-PET/CT Imaging and Clinical Data for Interpretable High-Grade Prostate Cancer Prognosis"
date: 2024-06-20
image:
  focal_point: 'top'

type: book

authors:
  - Maxence Larose
  - Martin Vallières
---

![arXiv](featured.png)

## Date

2024-06-20

## Authors

  - [Maxence Larose]({{< relref "/authors/maxence-larose" >}})<sup>1</sup>
  - Louis Archambault<sup>1,2</sup>
  - Nawar Touma<sup>2</sup>
  - Raphael Brodeur<sup>1,2</sup>
  - Félix Desroches<sup>1,2</sup>
  - [Nicolas Raymond]({{< relref "/authors/nicolas-raymond" >}})<sup>3</sup>
  - Daphnée Bédard-Tremblay<sup>2</sup>
  -Danahé LeBlanc<sup>1,2</sup>
  - Fatemeh Rasekh<sup>2</sup>
  - Hélène Hovington<sup>2</sup>
  - Bertrand Neveu<sup>2</sup>
  - [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>3</sup>
  - Frédéric Pouliot<sup>2</sup>

<sup>1</sup> Département de physique, de génie physique et d’optique, et Centre de recherche sur le cancer, Université Laval, Québec (QC), Canada.

<sup>2</sup> CHU de Québec – Université Laval et CRCHU de Québec, Québec (QC), Canada.

<sup>3</sup> Department of Computer Science, Université de Sherbrooke, Sherbrooke (QC), Canada.

  ## Abstract

  We propose a fully automatic multi-task Bayesian model, named Bayesian Sequential Network (BSN), for predicting high-grade (Gleason ≥ 8) prostate cancer (PCa) prognosis using pre-prostatectomy FDG-PET/CT images and clinical data. BSN performs one classification task and five survival tasks: predicting lymph node invasion (LNI), biochemical recurrence-free survival (BCR-FS), metastasis-free survival, definitive androgen deprivation therapy-free survival, castration-resistant PCa-free survival, and PCa-specific survival (PCSS). Experiments are conducted using a dataset of 295 patients. BSN outperforms widely used nomograms on all tasks except PCSS, leveraging multi-task learning and imaging data. BSN also provides automated prostate segmentation, uncertainty quantification, personalized feature-based explanations, and introduces dynamic predictions, a novel approach that relies on short-term outcomes to refine long-term prognosis. Overall, BSN shows great promise in its ability to exploit imaging and clinico-pathological data to predict poor outcome patients that need treatment intensification with loco-regional or systemic adjuvant therapy for high-risk PCa.


  ## Links

  - [Paper in arXiv](https://www.medrxiv.org/content/10.1101/2024.06.19.24308396v1)
  - [Paper in PDF version](https://www.medrxiv.org/content/10.1101/2024.06.19.24308396v1.full.pdf)
