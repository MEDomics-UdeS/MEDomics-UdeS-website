---
title: "Project: Random forests in a distributed learning context"

type: book

authors:
  - "Vincent Latourelle"
  - "Steven Robidas"
  - Olivier Lefebvre
  - Martin Vallières
---

## Status

Completed (2022)

## Type

Bachelor's

## Team

- Vincent Latourelle<sup>1</sup> (hiver 2022)
- Steven Robidas<sup>1</sup> (hiver 2022)
- [Olivier Lefebvre]({{< relref "/authors/olivier-lefebvre" >}})<sup>1</sup> (hiver 2022)
- [Martin Vallières]({{< relref "/authors/martin-vallieres" >}})<sup>1</sup> (hiver 2022)

<sup>1</sup> Computer science department, Université de Sherbrooke, Sherbrooke (QC), Canada

## Preamble

This final project was realized by Vincent Latourelle and Steven Robidas in the winter 2022 session as part of 
their bachelor's degree in computer science at the Université de Sherbrooke. This work was supervised by 
[Olivier Lefebvre]({{< relref "/authors/olivier-lefebvre" >}}) and 
[Martin Vallières]({{< relref "/authors/martin-vallieres" >}}).

## Introduction

Machine learning is a very useful branch in the medical field. However, medical data cannot necessarily be centralized 
to design accurate models. In order to maintain data privacy in machine learning, some federated learning models, 
which allow training models across multiple organizations without centralizing the data, have been developed.

This project focuses on the random forest model in a horizontal federated context. The papers on which our 
implementation is based are "Federated personalized random forest for human activity recognition"¹ and 
"Federated Extra-Trees With Privacy Preserving"².

## Implementation details

The implementation was done in *Python* and *Docker* was used to run the clients.

{{< figure src="fig_1.png" caption="Class diagram" numbered="true" >}}

## Classes

In this section, the different implemented classes will be described.

### NetworkCreator

Class that allows to distribute the data of a *Dataframe* between the clients to simulate a federated network. 
The *split_dataset* method is used to distribute in three different ways:

- *Unequal_rep*: Distribution dividing the number of data for each client in 2. Example for 5 clients, as a percentage of total data: 50%, 25%, 12.5%, 6.25%, 6.25%.
- 2 clients with *data_repartion* and without *label_repartition*: Separates the data between the two clients by specifying the percentage of data used in the first client. The rest will be in the second client. The distribution of the training targets is preserved.
- 2 clients with *data_repartion* and with *label_repartition*: Separates the data between the two clients by specifying the percentage of data used in the first client. The rest will be in the second client. The distribution of training targets for client 1 is specified in dictionary form. For example, if the dictionary *'B': 25, 'M':75}* is passed as a parameter, 25% of the data will be from the target 'B' and 75% from the target *'M'*.
- Otherwise: The data is separated between all the clients while keeping the proportions between the training targets.

### ServerManager

Class that manages communications (GET and POST) between the master and the clients.

### Client

Class that manages the operations of the clients in the construction of a federated random forest.

### Master

Class that serves as the entry point of the framework to call the different distributed training algorithms 
(only RandomForest for the moment). This class contains 2 main methods, *train* and *test*.

The *train* method allows to train a model using the *type* and *distribution* parameters.

- *type*: Type of training model. Only *rf* for the moment.
- *distribution*: training method:
  - *Federated*: Train a model in a distributed way.
  - *Localised*: Train a model at each client and return the list of models.
  - *Centralized*: trains a centralized model.

The *test* method allows to obtain the different types of accuracy:

- *type*: Type of training model. Only rf for the moment.
- *distribution*: test method:
  - *Federated*: Returns the *accuracy* of the model trained in a distributed way. The model is sent to the clients and they test it with their test set and return the value to the master.
  - *Localised*: Trains a model at each client and returns the *accuracy* on their own test set.
  - *Centralized*: Returns *the accuracy* of the centralized model on a test set.

### FederatedRandomForest

Class that manages the training process of a random forest in federated mode.

### RandomForest

Class that contains a collection of decision trees in order to make a prediction on the set of these trees using a 
majority vote.

### Node

Class that represents a node of a decision tree.

{{< figure src="fig_2.png" caption="Sequence diagram" numbered="true" >}}

## Flow of the algorithm

1. Le _NetworkCreator_ répartit les données entre les _K_ clients présents dans le
_ServerManager_.
2. Le _Master_ appel la fonction train de sa _FederatedRandomForest_.
3. La _FederatedRandomForest_ demande à un client la liste des _features_ présents dans son ensemble d’entrainement.
4. The _FederatedRandomForest_ builds _n_ trees with clients:
<ol type="a">
  <li>La <i>FederatedRandomForest</i> sélectionne au hasard un certain nombre de <i>features</i>.</li>
  <li>Elle envoie les <i>features</i> sélectionnés aux clients.</li>
  <li>Les clients sélectionnent chacun une valeur située entre l’intervalle des valeurs
  possibles pour chacun des <i>features</i> obtenus du master, c’est-à-dire une valeur située entre le minimum et le maximum inclusivement pour un <i>feature</i> donné. Ils renvoient ensuite ces valeurs au master <i>FederatedRandomForest</i>). Les clients séparent initialement leur ensemble d’entrainement en fonction des nœuds présents dans l’arbre actuellement en construction.</li> <li>La <i>FederatedRandomForest</i> choisit au hasard une valeur entre le minimum et le maximum des valeurs obtenus des clients pour chaque <i>feature</i>. Elle renvoie ensuite ces valeurs aux clients.</li>
  <li>Les clients choisissent la valeur qui sépare le mieux leur ensemble d’entrainement (à l’aide de Gini) parmi les valeurs obtenues de <i>FederatedRandomForest</i>. Les clients séparent initialement leur ensemble d’entrainement en fonction des nœuds présents dans l’arbre actuellement en construction. Ils renvoient ensuite cette valeur à la <i>FederatedRandomForest</i> ainsi que le nombre de données dans leur ensemble d’entrainement.</li>
  <li>La <i>FederatedRandomForest</i> fait un vote majoritaire pondéré par le nombre de données de chaque client. Elle crée un nœud avec l’attribut sélectionné et construit récursivement les arbres de gauche et de droite.</li>
  <li>Les étapes <i>a</i> à <i>f</i> seront donc répétées jusqu’à ce qu’une certaine profondeur d’arbre soit atteinte ou que le nombre de données chez les clients est insuffisant pour continuer à faire des séparations.</li>
  <li>Lorsque ces critères sont remplis, la <i>FederatedRandomForest</i> demande aux clients d’envoyer la classe majoritaire actuelle. La <i>FederatedRandomForest</i> effectue ensuite un vote majoritaire pondéré par le nombre de données totales dans l’ensemble d’entrainement du client pour construire la feuille de l’arbre.</li>
</ol>

5. La FederatedRandomForest envoie la forêt construite aux clients.

## Usage

The details of the usage are presented in the _Readme_. (links to GitHub)

## Results

All results were obtained with an average of executions of the algorithm.

{{< figure src="fig_3.png" caption="Accuracy of the model as a function of the distribution of training targets in client 1" numbered="true" >}}

The results shown in Figure 3 were obtained by varying the distribution of training targets in client 1 from a distribution of 15% 'B' target and 85% 'M' target to 85% 'B' target and 15% 'M' target. The initial distribution of the data was 60% 'B' and 40% 'M'. It is possible to observe a very low accuracy when the amount of 'M' is very high for client 1. Our hypothesis is that this configuration gathers all the data whose target is 'M' in the first client, which negatively impacts the learning in federated mode. À
50% target 'B' and above, the federated model seems to perform very well, outperforming local training and achieving similar results to centralized training.

{{< figure src="fig_4.png" caption="Accuracy of the model as a function of the number of clients with unequal data distribution" numbered="true" >}}

The results shown in Figure 4 are the result of training with clients that have an unequal amount of data, distributed using '_unequal_rep_' from _NetworkCreator_. It is possible to observe a trend where the minimum correctness of local training decreases and the average correctness of local training also decreases, as clients have less and less data. The federated mode accuracy seems to closely follow the centralized mode accuracy. These results can be explained by the fact that client 1 has as much decisional weight as all the other
as all the other clients. Thus, in federated mode, this distribution is similar to training a centralized random forest, but with half the data.

{{< figure src="fig_5_a.png" caption="" numbered="false" >}}

{{< figure src="fig_5_b.png" caption="Accuracy as a function of number of customers" numbered="true" >}}

Accuracy was measured by increasing the number of clients from 2 to 140. We can observe a significant decrease in the local and federated models as the number of clients increases. However, the federated model is more resilient than the local models. Indeed, the federated model produces reasonable correctness (about 88%) compared to the local models (about 50%).

{{< figure src="fig_6.png" caption="Accuracy as a function of the number of clients, up to 20 clients" numbered="true" >}}

With figure 6, it is possible to see in more detail the impact of the number of clients, up to 20 clients. We observe that the federated model seems on average to be a good compromise between the centralized model and the local models.

{{< figure src="fig_7.png" caption="Accuracy as a function of the number of data per client, for 2 clients" numbered="true" >}}

Figure 7 shows the change in accuracy by number of data in the first client (in percent). The distribution of data does not seem to have a significant impact on the performance of the model.

## Future work and conclusion

The solution currently allows heterogeneity only when two clients are used. It would therefore be necessary to add the possibility of having heterogeneity at more than two clients to simulate a real situation of federated learning. It would also be interesting to analyze the performance of the model with real data from different environments instead of centralized data that are artificially separated. The _framework_ can only train random forests for the moment and other models would have to be added to have a complete solution.

In summary, we have designed a federated learning framework and a federated _random forest_ algorithm based on (1) and (2). We then analyzed the impact of different variations on the performance of the model (heterogeneity and number of clients). It was possible to observe that the distributed _random forest_ model generally performed better than the local models,
regardless of the variations made.

## Bibliography

(1) Songfeng Liu, Jianyan Wang, Wenliang Zhang, « Federated personalized random forest
for human activity recognition », AIMS Press, November 22, 2021,
<https://www.aimspress.com/article/doi/10.3934/mbe.2022044?viewType=HTML>

(2) Yang Liu, Mingxim Chen, Wenxi Zhang, Junbo Zhang, Yu Zheng, « Federated Extra-Trees
With Privacy Preserving », Arxiv, February 18, 2020, <https://arxiv.org/abs/2002.07323>
