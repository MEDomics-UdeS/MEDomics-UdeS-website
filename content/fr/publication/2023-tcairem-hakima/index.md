---
title: "Présentation : Graph neural networks for predicting patient mortality within one year of hospital admission"
date: 2023-10-13
image:
  focal_point: 'top'

type: book

authors:
  - Hakima Laribi
  - Nicolas Raymond
  - Martin Vallières
---

![T-CAIREM](tcairem.png)

## Date

2023-10-13

## Auteurs

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})
- [Nicolas Raymond]({{< relref "/authors/nicolas-raymond" >}})
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})

## Résumé

  **Introduction**

  Predicting long-term patient survival after admission is crucial for improving palliative care and initiating goals of care discussions. Previous research successfully predicted the Hospital-patient One-year Mortality Risk for all causes using routine
  admission data, but overlooked valuable temporal information from a patient’s multiple hospital visits. Our study proposes to
  leverage patients’ longitudinal data to predict one-year mortality risk at admission. Our code is publicly available on: https://
  github.com/MEDomics-UdeS/POYM

  **Methods**

  We analyzed 197,905 hospital visits of 116,002 adult patients admitted to a nonpsychiatric service at the University Hospital
  of Sherbrooke from July 2011 to June 2021. Two models were compared: a previously developed Random Forest (RF) treating patient visits independently, and a new recurrent neural network (LSTM) model considering longitudinal patient data.
  5-folds cross-validation on 82,104 patients admitted between 2011 and 2017 assessed the benefits of temporal analysis.
  Modeled data types were “AdmDemo” (patient demographics and admission characteristics) and “AdmDemoDx” (also incorporating admission and old comorbidities diagnoses). A final LSTM model was trained on admissions between 2011 and
  2017 and tested on a separate holdout set of admissions between 2017 and 2021 (33,898 patients), excluding non-eligible
  end-of-life care visits.

  **Results**

  Our LSTM model demonstrated a raise in performance with an AUROC of 0.93 for “AdmDemoDx” and 0.90 for “AdmDemo”.
  The DeLong statistical test confirmed significant differences (p-values < 0.05) between the RF model and our approach in
  both settings. On the holdout set, our model demonstrated AUROC values of 0.89 for “AdmDemoDx” and 0.85 for “AdmDemo”.

  **Discussion/Conclusion**

  Our findings demonstrate the effectiveness of temporal analysis in predicting one-year mortality from hospitalization data of
  different types. Feature importance analysis revealed that simple data available at admission (AdmDemo) are the most discriminant in identifying high-risk patients. Overall, this study emphasizes the significance of leveraging patients’ longitudinal
  data to advance predictive models and enhance patient care.

## Présentation
<a href="/media/presentations/2023-tcairem-laribi.pptx" download>
<img src="/media/icons/ppt.png" alt="Download PPT" style="width: 50px; height: auto; display: block; margin: 0;">
</a>

## Liens

- [Détails sur l'événement](https://tcairem-conference.ca/)
- [Site web de T-CAIREM](https://tcairem.utoronto.ca/)
