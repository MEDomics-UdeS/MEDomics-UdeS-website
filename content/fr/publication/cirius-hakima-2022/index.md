---
title: "Présentation : Réseaux de neurones graphiques pour la prédiction de la mortalité des patients dans l’année suivant leur admission à l’hôpital"
date: 2022-10-20
image:
  focal_point: 'top'

type: book

authors:
  - Hakima Laribi
---

![CIRIUS](cirius-blanc.png)

## Date

2022-10-20

## Auteurs

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})

## Résumé

  Une discussion sur les objectifs de soins DOS est un processus de communication ayant lieu 
  dans un institut hospitalier entre un clinicien et un patient en fin de vie. Le but d’une 
  DOS est de déterminer les types de soins à administrer au patient afin de ne pas résulter 
  en des soins plus agressifs que ce qu’il souhaite. Néanmoins, les pronostics établis par 
  les médecins ne gagnant en certitude qu’avec le temps constituent la principale contrainte 
  retardant l’initiation d’une DOS. De ce fait, l’identification automatique des patients en 
  fin de vie dès leur admission à l’hôpital donnerait plus de chances à une DOS d’être effectuée 
  dans les temps. En ce sens, un modèle basé sur des forêts aléatoires [R. Taseen, 2021] qui tente 
  de prédire la mortalité des patients dans l’année suivant leur admission à l’hôpital a déjà été 
  développé. Bien que les arbres constituant les forêts aléatoires permettent d’exposer des 
  informations pertinentes sur l’importance de chaque variable de prédiction, aucune relation 
  entre les patients ne peut être apprise. Nous proposons donc une solution basée sur des réseaux 
  de neurones graphiques pour la prédiction de la mortalité des patients dans l’année suivant leur 
  admission à l’hôpital. Ainsi, les prédictions au niveau de chaque patient se feront en fonction de 
  tous les patients auxquels il est connecté et les résultats obtenus peuvent être expliqués en 
  consultant les connexions du patient. Cette approche basée sur des graphes permettrait d’inférer 
  des relations entre les patients et rajouterait ainsi de l’interprétabilité et de la performance 
  à un model basé sur des forêts aléatoires.

## Affiche
  ![Affiche](cirius-hl.png)

## Liens

- [Détails sur l'événement](https://www.dropbox.com/s/qshut4vilvaja93/Programmation_Cirius_JS_2022.pdf?dl=0)
- [Site web du CIRIUS](https://cirius.ca/)
