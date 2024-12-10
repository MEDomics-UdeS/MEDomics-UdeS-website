---
title: "Présentation : Améliorer la confiance dans les prédictions médicales : Identifier et traiter l'incertitude dans les prédictions médicales"
date: 2024-12-06
image:
  focal_point: 'top'

type: book

authors:
  - Olivier Lefebvre
  - Martin Vallières
---

![Pole](/media/logos/pole_numerique_fr.jpg)

## Date

2024-12-06

## Auteurs

- [Olivier Lefebvre]({{< relref "/authors/olivier-lefebvre" >}})
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})

## Résumé
**Introduction :**

Les modèles d’apprentissage automatique sont des outils puissants pouvant soutenir la prise de décisions cliniques, en fournissant des prédictions personnalisées pour chaque patient à partir de grandes bases de données. Bien que leurs performances soient souvent jugées satisfaisantes sur la base de métriques globales (justesse, AUROC, etc.) et qu'ils soient bien calibrés, ces modèles restent faillibles.
En effet, des erreurs de classification peuvent se produire pour certains profils de patients caractérisés par des facteurs comme l’âge, l’ethnie ou encore des changements de protocoles de soin, ce qui peut mener à des inégalités de soins. Afin de limiter ces erreurs, nous proposons une méthode pour identifier les patients pour lesquels un modèle de classification binaire est plus susceptible de se tromper, permettant ainsi d’éviter d’appliquer le modèle à ces patients.

**Méthode :**

Notre approche repose sur l’estimation de l’incertitude d’un modèle de classification binaire préalablement entraîné, appelé BaseModel. Nous définissons premièrement une mesure d’erreur pour chaque donnée d’entraînement afin de quantifier la différence entre la prédiction et la valeur réelle. Nous développons ensuite trois modèles d’estimation de confiance du BaseModel; Individualized Predictive Confidence (IPC), Aggregated Predictive Confidence (APC), et Mixed Predictive Confidence (MPC). Le modèle IPC évalue la confiance pour chaque patient individuellement, APC regroupe les patients en profils basés sur des niveaux de confiance similaires, tandis que MPC combine les deux approches pour un compromis optimal entre niveaux de confiance individuels et par profils.
Nous utilisons principalement les mêmes variables que le BaseModel pour ces modèles d’estimation, or il est possible d’en utiliser d’autres pour tester diverses hypothèses. Une fois les patients présentant une incertitude élevée identifiés, nous analysons l’impact du retrait de ces patients sur les métriques. L'efficacité du filtrage est mesurée à l’aide des courbes Metrics by Declaration Rate (MDR), qui montrent comment les métriques évoluent lorsque les patients les plus incertains sont progressivement exclus.

**Résultats :**

Nous avons testé notre approche sur quatre ensembles de données : un ensemble simulé, deux bases cliniques publiques, et un ensemble privé issu du CHUS. 
En général, l’exclusion des patients présentant la plus grande incertitude estimée a permis d'améliorer certaines métriques, comme la justesse balancée qui est passée de 58 % à 66 % pour les données du CHUS après l’exclusion des 10 % les plus incertains. Toutefois, dans certains cas, ce filtrage n’améliore pas les métriques. Dans ces situations, il est préférable de ne retirer aucun patient. Ainsi, l'application de notre méthode doit être adaptée au contexte spécifique et aux objectifs poursuivis.

**Conclusion :**

Notre approche propose un cadre méthodologique pour réduire les erreurs prédictives de modèles d’apprentissage automatique en filtrant de manière proactive les patients pour lesquels le modèle est moins fiable, réduisant ainsi les inégalités de performance entre les différents profils de patients. Cette méthode ne se veut toutefois qu’une première étape, puisque l’objectif ultime est d’améliorer les prédictions pour ces patients plutôt que de les exclure. À terme, nous visons mieux intégrer ces patients lors de l’entraînement du BaseModel pour réduire les disparités de performance.

## Presentation
{{< download-powerpoint file="/media/presentations/2024_pole_lefebvre.pptx" >}}

## Liens

- [Détails sur l'événement](https://event.fourwaves.com/fr/20241206/pages)
- [Site web du Pôle universitaire de santé numérique de l’Estrie](https://www.usherbrooke.ca/recherche/fr/udes/regroupements/pole-sante-numerique)
