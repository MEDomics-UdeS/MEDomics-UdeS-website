---
title: Predictive modeling based on multi-level graphical representations of multimodal healthcare data

type: book

authors:
  - Hakima Laribi
  - Martin Vallières
---

![Project presentation](Project.svg "Project presentation")

## Status

In progress (2022-today)

## Type

Doctorate

## Team

- [Hakima Laribi]({{< relref "/authors/hakima-laribi" >}})<sup>1</sup> (2022-aujourd'hui)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (2022-aujourd'hui)

<sup>1</sup> Computer science department, Université de Sherbrooke, Sherbrooke (QC), Canada


## Motivations

Graph Neural Networks have recently revealed great potential to learn graph representations and capture topological relationships between nodes. The spatial convolution of GNNs enables each node to acknwoledge its neighborhood by receiving information through edges and generate meaningful vector representations for the task at hand. Several levels of graph can be built to explore different connections types between data and learn exhaustive representations in distinct contexts.  

Furthermore, identifying different levels of connections between different entities can result in a lot of manual work. Selecting the most meaningful connections as the graph topology is constructed based on the predictive performance of the GNN would save a lot of manual supervision and allow exploring a large space of possible relationships. Reinforcement learning stands out as a machine learning method to guide the actions to take (i.e. adding a type of connection to the graph) through rewards that differ according to the state of the environment (i.e. predictive performance of the model).

In this work, we aim to build a multi-level graph topology to optimize patients representations then improve it using Reinforcement Learning, we will also train a federated Graph Neural Networks on a distributed topology of the graph. The figure above presents the different steps of our approach. 

## Hypotheses

- A patient-level graph would enable to co-learn modalities representations and could extract meaningful associations among modalities to improve patients representations.
- An institution-level graph would enable information sharing between patients in solving a prediction task and could improve accuracy and interpretability of the solution.
- A reinforcement learning algorithm would explore a large space of graph structures and could discover hidden dependencies among patients and/or modalities, thereby improving accuracy and interpretability of the solution. 

## Objectives

- Optimize patients representations in a multi-level graph topology for downstream prediction tasks.
- Learn a multi-level graph topology with heterogeneous links across modalities and patients using Reinforcement Learning.
- Train Graph Neural Networks on a distributed topology of the multi-level graph defined above using Federated Learning.

## Methodology

To evaluate the performance of our solution, we will use the [HAIM multimodal dataset](https://physionet.org/content/haim-multimodal/1.0.1/) [[Soenksen et al., 2022](https://www.nature.com/articles/s41746-022-00689-4)] containing data from four different modalities (time series, notes, tabular, images) to predict chest pathology diagnosis (Fracture, Lung Lesion, Enlarged cardio mediastinum, Consolidation, Pneumonia, Lung, Atelectasis, Pneumothorax, Edema and Cardiomegaly), length Of Stay and 48 hours mortality.
