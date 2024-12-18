---
title: "Presentation: 3D convolutional neural network as a decision support system for multiple renal tumor classification tasks"
date: 2021-05-05
image:
  focal_point: 'top'

type: book
show_date: true

authors:
  - Alexandre Ayotte

categories: Presentations
where: ACFAS 2021
---

![ACFAS](featured.png)

## Date

2021-05-05

## Authors

- [Alexandre Ayotte]({{< relref "/authors/alexandre-ayotte" >}})

## Summary 

**Research objective:** To develop an interpretable tool for the automatic classification of renal lesions from MRI images. The classification is performed according to the nature, malignancy or benignity of the tumors and according to their subtype and grade for malignant tumors.

**Problem to tackle:** 2D ResNet networks are known to obtain good results in this type of classification. Can extending a 2D ResNet neural network to a 3D ResNet network improve the accuracy of classifications?

**Methodology:** A 3D ResNet model was designed and its performance compared to a modified, pre-trained 2D ResNet published in 2020 and a SVM using only clinical data. MRI images of 1,076 patients, from 5 institutions, were used to train (80%) and test (20%) both ResNet networks. For the 2D network, clinical data were also used as inputs.

**Results:** The 3D ResNet performed better in 2 of the 3 tasks. Its accuracy was 79.4%, 82.1%, and 55.7% for malignancy, subtype, and grade classification, respectively, compared with 77.5%, 67.0%, and 58.2% for the model using only clinical data and 77.3%, 76.8%, and 66.5% for the 2D ResNet.

**Discussion:** Despite the fact that the proposed 3D ResNet is not pre-trained and does not use clinical data, its performance is promising. Clinical data will be incorporated in the future.

## Links

- [Event Details](https://www.acfas.ca/evenements/congres/programme/88/600/614/c)
- [Presentation Video](https://vimeo.com/542213504/c5040822fa)
