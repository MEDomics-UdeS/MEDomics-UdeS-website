---
title: "Projet : Réseaux de neurones graphiques pour la prédiction de la mortalité des patients dans l’année suivant leur admission à l’hôpital"

type: book

authors:
  - Hakima Laribi
  - Martin Vallières
---

![Présentation du projet](project.svg "Présentation du projet")

## État

En cours (2022-aujourd'hui)

## Type

Doctorat

## Équipe

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})<sup>1</sup> (2022-aujourd'hui)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (2022-aujourd'hui)

<sup>1</sup> Départment d'informatique, Université de Sherbrooke, Sherbrooke (QC), Canada


## Description
Une discussion sur les objectifs de soins DOS est un processus de communication ayant lieu dans un institut hospitalier entre un clinicien et un patient en fin de vie. Le but d’une DOS est de déterminer les types de soins à administrer au patient afin de ne pas résulter en des soins plus agressifs que ce qu’il souhaite. Néanmoins, les pronostics établis par les médecins ne gagnant en certitude qu’avec le temps constituent la principale contrainte retardant l’initiation d’une DOS. De ce fait, l’identification automatique des patients en fin de vie dès leur admission à l’hôpital donnerait plus de chances à une DOS d’être effectuée dans les temps. En ce sens, un modèle basé sur des forêts aléatoires [[R. Taseen, 2021](https://www.researchgate.net/publication/354327628_Expected_clinical_utility_of_automatable_prediction_models_for_improving_palliative_and_end-of-life_care_outcomes_Toward_routine_decision_analysis_before_implementation)] qui tente de prédire la mortalité des patients dans l’année suivant leur admission à l’hôpital a déjà été développé. Bien que les arbres constituant les forêts aléatoires permettent d’exposer des informations pertinentes sur l’importance de chaque variable de prédiction, aucune relation entre les patients ne peut être apprise. Nous proposons donc une solution basée sur des réseaux de neurones graphiques pour la prédiction de la mortalité des patients dans l’année suivant leur admission à l’hôpital. Ainsi, les prédictions au niveau de chaque patient se feront en fonction de tous les patients auxquels il est connecté et les résultats obtenus peuvent être expliqués en consultant les connexions du patient. Cette approche basée sur des graphes permettrait d’inférer des relations entre les patients et rajouterait ainsi de l’interprétabilité et  de la performance à un model basé sur des forêts aléatoires.

**Objectifs :** 

- Modéliser sous forme de graphe les données afin d’apprendre des connexions entre les patients.
- Développer une méthode de prédiction basée sur des réseaux de neurones graphiques afin d’identifier les patients à risque.

**Résultats attendus :**

- Améliorer la précision et la justesse de prédiction avec une solution basée sur des réseaux de neurones graphiques.
- Analyse a posteriori et interprétation des résultats obtenus.
