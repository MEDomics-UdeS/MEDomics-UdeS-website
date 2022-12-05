---
title: "Modélisation prédictive basée sur des représentations sous formes de graphes multi-niveaux des données de santé multimodales"

type: book

authors:
  - Hakima Laribi
  - Martin Vallières
---

![Présentation du projet](Projet.svg "Présentation du projet")

## État

En cours (2022-aujourd'hui)

## Type

Doctorat

## Équipe

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})<sup>1</sup> (2022-aujourd'hui)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (2022-aujourd'hui)

<sup>1</sup> Départment d'informatique, Université de Sherbrooke, Sherbrooke (QC), Canada


## Motivations

Les réseaux de neurones graphiques ont récemment révélé un grand potentiel pour apprendre des représentations de graphes et capturer des relations topologiques entre les nœuds. La convolution spatiale des réseaux de neurones graphiques permet à chaque nœud de reconnaître son voisinage en recevant de l'information via les arêtes et de générer des représentations vectorielles significatives pour la tâche à accomplir. Plusieurs niveaux de graphes peuvent être construits pour explorer différents types de connexions entre les données et apprendre des représentations exhaustives dans des contextes distincts.

Par ailleurs, l’identification de différents niveaux des connexions entre les différentes entités peut résulter en une grande quantité de travail manuel.  La sélection des connexions les plus signifiantes au fur et à mesure de la contruction de la topologie du graphe en fonction des performances prédictives du réseau de neurones graphique épargenrait beaucoup de supervision manuelle et permettrait d’exploiter un grand espace de connexions possibles. L’apprentissage par renforcement se distingue comme une des méthodes d'apprentissage automatique permettant de guider la prise d’action (i.e. l’ajout d’un type de connexion dans le graphe) par des récompenses en fonction de l’état de l’environnement (i.e. performance prédictive du modèle)

Dans ce travail, nous visons à construire une topologie de graphe multi-niveaux pour optimiser les représentations des patients puis à l'améliorer à l'aide de l'apprentissage par renforcement, nous allons également entraîner un réseau de neurones graphique fédéré sur une topologie distribuée du graphe. La figure ci-dessus présente les différentes étapes de notre démarche.

## Hypotheses

- Un graphe au niveau du patient permettrait de co-apprendre les représentations des modalités et pourrait extraire des associations significatives entre les modalités pour améliorer les représentations des patients.
- Un graphe au niveau institution permettrait le partage d'informations entre les patients lors de la résolution d'une tâche de prédiction et pourrait améliorer la précision et l'interprétabilité de la solution.
- Un algorithme d'apprentissage par renforcement explorerait un large espace de structures de graphes et pourrait découvrir des dépendances cachées entre les patients et/ou les modalités, améliorant ainsi la précision et l'interprétabilité de la solution.

## Objectives

- Optimiser les représentations des patients dans une topologie graphique à plusieurs niveaux pour les tâches de prédiction subséquentes.
- Apprendre une topologie graphique à plusieurs niveaux avec des liens hétérogènes entre les modalités et les patients à l'aide de l'apprentissage par renforcement.
- Entraîner les réseaux neuronaux graphiques sur une topologie distribuée du graphe à plusieurs niveaux défini ci-dessus à l'aide de l'apprentissage fédéré.

## Methodology

Pour évaluer les performances de notre solution, nous utiliserons le [jeu de données à plusieurs modalités HAIM](https://physionet.org/content/haim-multimodal/1.0.1/) [[Soenksen et al., 2022](https:/ /www.nature.com/articles/s41746-022-00689-4)] contenant des données de quatre modalités différentes (séries chronologiques, notes, tables, images) pour prédire le diagnostic de pathologie thoracique (Fracture, Lésion pulmonaire, Hypertrophie du médiastin cardiaque, Consolidation , Pneumonie, Poumon, Atélectasie, Pneumothorax, Œdème et Cardiomégalie), durée du séjour à l'hôpital et mortalité dans les 48 heures.
