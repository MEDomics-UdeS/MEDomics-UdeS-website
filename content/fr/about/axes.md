---
widget: blank
weight: 20
active: true
headless: true
---

# Axes de recherche

With the progress of modern medicine, a large number of medical encounters (e.g. medical visits, exams,
medications, imaging, molecular testing, etc.) are taking place in our healthcare system. In fact, the
amount of new global healthcare data generated in 2020 is expected to have reached 2,314 exabytes [1].
Most of the content of Electronic Health Records (EHR) of our hospitals are recorded via sparse data
tables with a high probability of missing values. The EHR nonetheless possess a vast amount of
heterogeneous data from different sources, most of which is often sub-optimally exploited to characterize
and predict disease behaviour. For example, medical imaging (e.g. magnetic resonance imaging: MRI)
would carry an immense source of potential data for decoding cancer phenotypes [2]. On the other hand,
physicians also describe and write important patient characteristics and symptoms related to disease for
almost every medical encounter via free-form medical text notes. In the recent years, significant progress
in multi-omics technology (e.g. genomics, transcriptomics, etc.) has also created unprecedented
opportunities for characterizing the biological processes correlated with diseases [3]. However,
combining these heterogeneous data sources in a meaningful way for disease prediction is a challenge.
For better precision medicine, therefore, physicians must now make increasingly complex
treatment decisions with an unrealistic number of variables. This is why artificial intelligence (AI)
developments are envisioned to create a data science revolution in medicine. In particular, graphical
neural networks (GNNs) have shown immense potential in learning meaningful and powerful data
representations [4], [5] by combining relational inference of graphical models with the power of deep
learning. However, given that the power of deep learning is strongly associated with data size and that
medical data cannot be easily shared between medical institutions due to patient privacy reasons,
developing powerful GNN models for disease prediction in healthcare is a major challenge. This
research program proposes to develop a framework for privacy-preserving distributed GNN learning
from a network of federated healthcare databases, which will be an important step for the progress of
AI in medicine. Within this federated learning setting: (i) GNN models can be developed from the
databases of multiple healthcare institutions, thereby augmenting the size of the data being analyzed; and
(ii) data is always kept within the confines of each healthcare institution, thereby avoiding data transfer.
