---
title: "Presentation : Synthetic Data for Accessible Learning in Healthcare: Improving Mortality Prediction with Longitudinal Data"
date: 2024-12-06
image:
  focal_point: 'top'

type: book

authors:
  - Hakima Laribi
  - Nicolas Raymond
  - Martin Vallières

categories: Presentations
where: Pôle universitaire de santé numérique de l’Estrie
---

![Pole](/media/logos/pole_numerique_en.jpg)

## Date

2024-12-06

## Authors

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})
- [Nicolas Raymond]({{< relref "/authors/nicolas-raymond" >}})
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})

## Summary

**Introduction :** 

L’estimation du potentiel de survie à moyen terme des patients après admission permet d’identifier ceux en fin de vie qui pourraient bénéficier de discussions sur les objectifs de soins. De précédentes études ont tenté de prédire le risque de mortalité à un an des patients, mais ont seulement considéré leur admission actuelle sans tenir compte de leurs visites précédentes. Dans ce travail, nous supposons que les données longitudinales des patients impactent leur pronostic, et proposons le modèle Ensemble Long Short-Term Memory (ELSTM) qui intègre l’historique disponible dans ses prédictions. De plus, nous avons généré un ensemble de données synthétiques accessible publiquement pour encourager la recherche dans ce domaine tout en préservant la confidentialité des patients : https://doi.org/10.5281/zenodo.12954672 

**Données :**

Nous avons analysé 250,812 visites appartenant à 123,646 patients adultes admis au CHUS entre le 1er juillet 2011 et le 30 juin 2021. Pour modéliser les variations dans les données disponibles à l’admission à travers différents hôpitaux, nous évaluons deux ensembles de prédicteurs : (i) «AdmDemo», comprenant uniquement les données démographiques et les caractéristiques d'admission, et (ii) «AdmDemoDx», incorporant en plus les diagnostics de comorbidité et  d'admission. Nous avons utilisé la méthode AVATAR [3] pour générer un ensemble de données synthétiques à partir de nos données originales comprenant 123,646 patients et 248,485 visites. 

**Méthodes :**

Notre ELSTM est un modèle ensembliste composé de plusieurs réseaux LSTM [1], chacun entraîné en considérant un certain nombre de visites, allant d'une seule visite jusqu'à toutes les visites du patient. L’évaluation du modèle se fait dans un schéma de validation croisée à 5 plis. Nous comparons notre ELSTM à un modèle de forêt aléatoire précédemment développé [2], qui traite chaque visite indépendamment des autres. Les résultats des deux modèles sont analysés sur les ensembles de données originaux et synthétiques.

**Résultats :**

Notre ELSTM a démontré une augmentation significative des performances en utilisant l’information longitudinale (p-valeur < 0.05). Lorsqu’il a été testé sur les dernières visites des patients, l’ELSTM a atteint des AUROCs de 0.90 pour «AdmDemo» et 0.92 pour «AdmDemoDx». Les augmentations en performances sur l’ensemble de données synthétique correspondaient à celles sur les données originales, avec des AUROCs de 0.91 et 0.93 pour les prédicteurs «Admdemo» et «AdmDemoDx», respectivement. Les métriques de confidentialité ont dépassé les seuils requis, avec par exemple un taux caché de 100%, indiquant que chaque donnée synthétique est plus similaire à une autre donnée originale qu’à celle ayant servi à sa génération.

**Conclusion :**

Nos résultats démontrent l’importance de considérer les données longitudinales des patients pour mieux prédire leur risque de mortalité à un an. De plus, les résultats avec les prédicteurs AdmDemo montrent qu'une bonne performance prédictive peut être atteinte même avec des données d'admission potentiellement auto-déclarées par les patients. Nous avons également montré l’utilité de l’ensemble de données synthétiques dans ce contexte clinique ainsi que ses robustes caractéristiques de confidentialité. Ces données partagées publiquement peuvent être utilisées dans de futures recherches et contribuer à l'objectif plus large d’un apprentissage accessible en santé. 

[1] https://doi.org/10.1162/neco.1997.9.8.1735 
[2] https://doi.org/10.1093/jamia/ocab140 
[3] https://doi.org/10.1038/s41746-023-00771-5 


## Presentation
{{< download-powerpoint file="/media/presentations/2024_pole_laribi.pptx" >}}

## Links

- [Event Details](https://event.fourwaves.com/fr/20241206/pages)
- [Website of the Pôle universitaire de santé numérique de l’Estrie](https://www.usherbrooke.ca/recherche/en/udes/clusters/pole-universitaire-de-sante-numerique-de-lestrie)
