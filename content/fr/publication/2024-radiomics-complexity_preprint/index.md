---
title: "Article : Unraveling Radiomics Complexity: Strategies for Optimal Simplicity in Predictive Modeling"
date: 2024-07-05
image:
  focal_point: 'top'

type: book

authors:
  - Mahdi Ait Lhaj Loutfi
  - Martin Vallières
---

![arXiv](featured.png)

## Date

2024-07-05

## Auteurs

  - [Mahdi Ait Lhaj Loutfi]({{< relref "/authors/mahdi-ait-lhaj-loutfi" >}})<sup>1</sup>
  - [Teodora Boblea Podasca]({{< relref "/authors/teodora-boblea-podasca" >}})<sup>2</sup>
  - Alex Zwanenburg<sup>3,4,5,6</sup>
  - Taman Upadhaya<sup>7</sup>
  - Jorge Barrios<sup>8</sup>
  -David R. Raleigh<sup>9</sup>
  - William C. Chen<sup>8</sup>
  - Dante P.I. Capaldi<sup>8</sup>
  - Hong Zheng<sup>10</sup>
  - Olivier Gevaert<sup>11</sup>
  - Jing Wu<sup>12</sup>
  - Alvin C. Silva<sup>13</sup>
  - Paul J. Zhang<sup>14</sup>
  - Harrison X. Bai<sup>15</sup>
  - Jan Seuntjens<sup>16</sup>
  - Steffen Löck<sup>3</sup>
  - Patrick O. Richard<sup>17</sup>
  - Olivier Morin<sup>8</sup>
  - Caroline Reinhold<sup>18</sup>
  - Martin Lepage<sup>19,20</sup>
  - [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1,21</sup>


<sup>1</sup> Department of Computer Science, Université de Sherbrooke, Sherbrooke, QC, Canada

<sup>2</sup> Department of Surgery, Service of Urology, Université de Sherbrooke, Sherbrooke, QC, Canada

<sup>3</sup> OncoRay – National Center for Radiation Research in Oncology, Faculty of Medicine and University Hospital Carl Gustav Carus, TUD Dresden University of Technology, Helmholtz-Zentrum Dresden-Rossendorf, Dresden, Germany

<sup>4</sup> National Center for Tumor Diseases Dresden (NCT/UCC), Germany: German Cancer Research Center (DKFZ), Heidelberg, Germany

<sup>5</sup> Faculty of Medicine and University Hospital Carl Gustav Carus, TUD Dresden University of Technology, Dresden, Germany

<sup>6</sup> Helmholtz-Zentrum Dresden-Rossendorf (HZDR), Dresden, Germany

<sup>7</sup> Department of Radiation Oncology, Cedars-Sinai Medical Center, Los Angeles, CA, USA

<sup>8</sup> Department of Radiation Oncology, University of California San Francisco, San Francisco, CA, USA

<sup>9</sup> Departments of Radiation Oncology, Neurological Surgery, and Pathology, University of California San Francisco, San Francisco, CA, USA

<sup>10</sup> Center for Biomedical Informatics Research, School of Medicine, Stanford University, CA 94305, USA

<sup>11</sup> Department of Medicine, and Department of Biomedical Data Science, Stanford University, Stanford, CA 94305, USA

<sup>12</sup> Department of Radiology, The Second Xiangya Hospital of Central South University, Changsha, 410011, Hunan, China

<sup>13</sup> Department of Radiology, Mayo Clinic Arizona, 13400 E Shea Blvd., Scottsdale, AZ 85259, USA

<sup>14</sup> Department of Pathology and Clinical Medicine, Hospital of the University of Pennsylvania, Philadelphia, PA, USA

<sup>15</sup> Department of Radiology and Radiological Sciences, Johns Hopkins, Baltimore, MD, USA

<sup>16</sup> Princess Margaret Cancer Centre, University Health Network & Departments of Radiation Oncology & Medical Biophysics, University of Toronto, Toronto, ON, Canada.

<sup>17</sup> Division of Urology, Centre Hospitalier Universitaire de Sherbrooke; Université de Sherbrooke Cancer Research Institute, Sherbrooke, QC, Canada

<sup>18</sup> Department of Radiology, McGill University Health Center, Director and Co-founder, Augmented Intelligence Precision Health Laboratory (AIPHL) of the Research Institute of the McGill University Health Center, Montreal, QC, Canada

<sup>19</sup> Département de médecine nucléaire et radiobiologie, Université de Sherbrooke, Sherbrooke, QC, Canada

<sup>20</sup> Centre d’imagerie moléculaire de Sherbrooke, Université de Sherbrooke, Sherbrooke, QC, Canada

<sup>21</sup> Centre de recherche du Centre hospitalier universitaire de Sherbrooke, Université de Sherbrooke, Sherbrooke, QC, Canada

## Résumé

  Background: The high dimensionality of radiomic feature sets, the variability in radiomic feature types and potentially high computational requirements all underscore the need for an effective method to identify the smallest set of predictive features for a given clinical problem. Purpose: To establish a methodology and provide tools for identifying and explaining the smallest set of predictive features radiomic features. Materials and Methods: Radiomic features (a total of 89,714) were extracted from five distinct datasets with different cancer types: low-grade glioma, meningioma, non-small cell lung cancer (NSCLC), and two renal cell carcinoma cohorts (n=2104). These features were categorized into complexity levels, defined by the number of computational steps required for their computation, encompassing morphological, intensity, texture, linear filters-based, and nonlinear filter-based features. For every dataset, models were trained on each complexity level specifically to classify clinical outcomes, and their performance was evaluated using the area under the curve (AUC). The most informative features were identified and their importance was explained. The optimal complexity level and associated most informative features were identified using systematic statistical significance analyses and a false discovery avoidance procedure, respectively. Their predictive importance was explained using a novel tree-based method. Results: MEDimage, a new open-source tool, was designed and implemented to streamline radiomic studies through both code-based and graphical-based approaches, and was applied using our proposed methodology to analyze the datasets. Morphological features were found to be optimal in two cases: for MRI-based meningioma (AUC: 0.65; sensitivity: 64%; specificity: 62%; 95% CI: 0.59, 0.72) and MRI-based low-grade glioma (AUC: 0.68; sensitivity: 68%; specificity: 69%; 95% CI: 0.60, 0.75). Additionally, intensity features were optimal in two instances: for contrast-enhanced CT (CECT)- based renal cell carcinoma (AUC: 0.82; sensitivity: 77%; specificity: 78%; 95% CI: 0.76, 0.88) and CT-based NSCLC (AUC: 0.76; sensitivity: 73%; specificity: 71%; 95% CI: 0.71, 0.80). Texture features were identified as optimal for MRI-based renal cell carcinoma (AUC: 0.72; sensitivity: 71%; specificity: 65%; 95% CI: 0.68, 0.77). Notably, in CECT-based renal cell carcinoma, the tuning of the Hounsfield unit range, which directly affects intensity-based features, led to improved results (AUC: 0.86). Conclusion: Our proposed methodology and software can estimate the optimal radiomics complexity level for specific medical outcomes, potentially simplifying the use of radiomics in predictive modeling across various contexts.


## Liens

  - [Page de l'article](https://arxiv.org/abs/2407.04888)
  - [Article en version PDF](https://arxiv.org/pdf/2407.04888)
