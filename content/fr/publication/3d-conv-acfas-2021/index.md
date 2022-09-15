---
title: "Présentation : Réseau de neurones à convolution 3D comme système d’aide à la décision pour de multiples tâches de classification de tumeurs rénales"
date: 2021-05-05
image:
  focal_point: 'top'

type: book
show_date: true

authors:
  - Alexandre Ayotte
---

![ACFAS](featured.png)

## Date

2021-05-05

## Résumé 

**Objectif de la recherche :** Développer un outil interprétable pour la classifications automatique des lésions rénales à partir d’images IRM. La classification est effectuée selon la nature, malignité ou bénignité des tumeurs et selon leur sous-type et leur grade pour les tumeurs malignes.

**Problématique :** Les réseaux de type ResNet 2D sont connus pour obtenir de bons résultats dans ce type de classification. L’extension d’un réseau de neurone de type ResNet 2D à un réseau de type ResNet 3D peut-elle améliorer la précision des classifications?

**Méthodologie :** Un modèle de ResNet 3D a été conçu et ses performances comparées à celles d’un réseau ResNet 2D modifié et pré-entrainé publié en 2020 et à un SVM utilisant uniquement des données cliniques. Les images IRM de 1076 patients, provenant de 5 institutions, ont été utilisées pour entrainer (80%) et tester (20%) les deux réseaux ResNet. Pour le réseau 2D, les données cliniques ont également été utilisées comme entrées.

**Résultats :** Le ResNet 3D obtient de meilleurs résultats dans 2 des 3 tâches. Sa précision est de 79,4%, 82,1% et 55,7% pour la classification de la malignité, du sous-type et du grade respectivement, contre 77,5%, 67,0% et 58,2% pour le modèle n’utilisant que les données cliniques et 77,3%, 76,8% et 66,5% pour le ResNet 2D.

**Discussion :** Malgré le fait que le ResNet 3D proposé ne soit pas pré-entraîné et n’utilise pas les données cliniques, ses performances sont prometteuses. Les données cliniques seront intégrées dans le futur.

## Liens

- [Détails sur l'événement](https://www.acfas.ca/evenements/congres/programme/88/600/614/c)
- [Vidéo de la présentation](https://vimeo.com/542213504/c5040822fa)
