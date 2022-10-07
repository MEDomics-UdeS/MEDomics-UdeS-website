---
title: "Projet : Exploration des niveaux de complexité des caractéristiques radiomiques"

type: book

authors:
  - Mahdi Ait Lhaj Loutfi
  - Martin Vallières
---

![Résumé du projet](resume.svg "Résumé du projet")

## État

En cours (2021-aujourd'hui)

## Type

Maîtrise

## Équipe

- [Mahdi Ait Lhaj Loutfi]({{< relref "/authors/mahdi-ait-lhaj-loutfi" >}})<sup>1</sup> (2021-aujourd'hui)
- [Martin Lepage](https://www.usherbrooke.ca/recherche/specialistes/details/martin.lepage)<sup>2</sup> (2021-aujourd'hui)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (2021-aujourd'hui)

<sup>1</sup> Départment d'informatique, Université de Sherbrooke, Sherbrooke (QC), Canada

<sup>2</sup> Départment de médecine nucléaire et radiobiologie, Université de Sherbrooke, Sherbrooke (QC), Canada

## Problématique et objectif

Les progrès récents de la technologie « omique » ont créé des opportunités pour caractériser les processus biologiques corrélés aux phénotypes tumoraux. Nous prévoyons que la modélisation intégrante des données d'oncologie disponibles donnera une capacité à faire des prédictions phénotypiques tumorales précises, ce qui permettrait à son tour de mieux surveiller et d'adapter des traitements particuliers à chaque patient (c'est-à-dire « oncologie de précision »). Pour potentiellement améliorer les analyses radiomiques (i.e. : L'extraction quantitative de données exploitables à partir de tous types d'images médicales), on peut extraire des caractéristiques radiomiques de la région tumorale d'images médicales filtrées avec différents types de filtres (par exemple : le filtrage de texture ou le lissage de texture). Ces caractéristiques peuvent être extraites à l’aide du [logiciel MEDimage](medimage.readthedocs.io/), mais elles exposent des différents niveaux de complexité, ce qui nous mène à investiguer dans ce projet, le spectre de complexité d’images médicales pour la résolution de plusieurs problèmes en oncologie de précision et étudier ces différents types de complexité, qui changent à cause de la grande variété dans les modalités d’images.

## Base de données

Nous avons déjà a priori une large base de données sur laquelle l’analyse des niveaux de complexités va être portée. Elle contient des multiples combinaisons de modalités d’image et de problèmes de prédictions (13 combinaisons en tout), comme le montre le tableau ci-dessous:

![Bases de données (Images médicales)](bd.svg "Bases de données des images médicales")

## Niveaux de complexité à étudier

![Niveaux de compléxité (Complexité croissante)](complexite.svg "Niveaux de compléxité dans le sens croissant")
