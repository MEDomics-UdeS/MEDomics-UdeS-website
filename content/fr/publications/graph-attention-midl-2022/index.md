---
title: 'Graph Attention Network for Prostate Cancer Lymph Node Invasion Prediction'
authors:
  - Maxence Larose
  - Nawar Touma
  - Martin Vallières
date: '2022-04-22T00:00:00Z'
doi: ''

# Schedule page publish date (NOT publication's date).
publishDate: '2022-04-22T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['1']

# Publication name and optional abbreviated publication name.
publication: Dans *Medical Imaging with Deep Learning 2022*
publication_short: Dans *MIDL 2022*

abstract: This work proposes the use of a graph attention network (GAT) model combining radiomics and clinical data to improve the performance and interpretability of lymph node invasion (LNI) prediction in high-grade prostate cancer (PCa). Experiments were conducted using an in-house dataset of 170 high-grade PCa (Gleason ≥ 8), each with FDG-PET/CT images acquired prior to prostatectomy. To ensure interpretable connections between patients, the graph structure was constructed by merging the most important radiomic shape-based CT feature and first-order intensity-based PET feature to the clinically relevant features. The performance of the GAT model was compared to random forest (RF) and support vector machine (SVM) classifiers. On the 30 patients test set, the models reached {AUC=0.765, bACC= 0.705}, {AUC=0.748, bACC=0.66} and {AUC=0.725,bACC=0.725} for the GAT, RF and SVM models respectively. Even though SVM achieved higher balanced accuracy than GAT, the predictions made by the latter are more interpretable through the graph structure and attention mechanism.

# Summary. An optional shortened abstract.
summary: A graph attention network (GAT) model combining radiomics and clinical data to improve the performance and interpretability of lymph node invasion prediction in high-grade prostate cancer.

featured: true

# links:
#   - name: Custom Link
#     url: http://example.org
url_pdf: https://openreview.net/pdf?id=zIpx-MISaIA
# url_code: '#'
# url_dataset: '#'
# url_poster: '#'
# url_project: ''
# url_slides: ''
# url_source: '#'
# url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# image:
#   caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#   focal_point: ''
#   preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides:
---

{{% callout note %}}
Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

Supplementary notes can be added here, including [code and math](https://wowchemy.com/docs/content/writing-markdown-latex/).
