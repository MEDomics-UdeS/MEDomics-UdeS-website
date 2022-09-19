---
title: "Thesis Defense: Electric Power Fuse Identification with Deep Learning"

event: Simon Giard-Leroux's Thesis Defense
event_url: https://bit.ly/3zSvNew

location: Local D4-2011, Faculté des sciences, Université de Sherbrooke
address:
  street: 2500, Boulevard de l'Université
  city: Sherbrooke
  region: QC
  postcode: 'J1K 2R1'
  country: Canada

summary: Simon Giard-Leroux's Thesis Defense
abstract:

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2022-09-09T14:00:00Z'
date_end: '2022-09-09T16:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2022-08-10T00:00:00Z'

authors: 
  - Simon Giard-Leroux

tags: []

# Is this a featured talk? (true/false)
featured: false

# image:
#   caption: 
#   focal_point: 

# url_code: ''
# url_pdf: ''
# url_slides: ''
# url_video: ''

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides:

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects:
---

**Description:**

**Speaker:** Simon Giard-Leroux, M. Sc. student in Computer Science, Department of Computer Science, 
Faculty of Science, Université de Sherbrooke

**Abstract:** In the electrical power industry, arc flash studies are performed by engineers to evaluate the incident 
energy to which a person working on equipment would be exposed if an accident caused a short circuit. This energy can 
vary according to several parameters, one of the main ones being the duration of the arc, which depends on how 
quickly the protective equipment supplying the equipment where the fault occurs is cut off. It is therefore important 
to correctly identify the protective equipment in an electrical network, including the types of fuses, which can be 
difficult to identify with the naked eye from photos of electrical installations. However, they can be identified by 
their physical characteristics, such as their color or shape. This observation task must currently be done manually, 
so a more automated solution would be advantageous.

In parallel, the field of object detection using deep learning has experienced a remarkable growth in the last few 
years in order to localize and identify the type of different objects in images. By applying a supervised learning 
strategy, it is possible to train and optimize an object detection model based on neural networks that can identify 
fuses in new images never seen before. In this dissertation, we will discuss the use of deep learning-based object 
detection techniques to automate the identification of electrical fuses, including the Faster R-CNN, RetinaNet and 
DETR models. We will pose the problem of fuse identification in the context of arcing studies, describe the principles 
behind the object detection techniques used in deep learning, and propose a methodology to optimize a final detection 
model that can be used in industry with a high identification performance, allowing to significantly accelerate the 
work of electrical engineers in this task. 

A paper detailing our methodology to achieve a final AP50 performance of 91.06% has been submitted for publication to 
the journal _IEEE Transactions on Industrial Informatics_ and is currently under review. This result demonstrates 
that fuses can be adequately predicted in new electrical survey photos. The developed code, the dataset of more than 
12,000 fuses and a user interface to use the final model in an industrial context are shared openly with the 
scientific community.

**Jury member, president**Pierre-Marc Jodoin, Professor, Department of Computer Science, Faculty of Science, Université de Sherbrooke

**Jury member, research director:** Martin Vallières, Professor, Department of Computer Science, Faculty of Science, Université de Sherbrooke

**Jury member, research co-director:** François Bouffard, Professor, Department of Electrical and Computer Engineering, McGill University

**Jury member, external evaluator:** Christian Gagné, Professor, Department of Electrical and Computer Engineering, Université Laval

All interested persons are cordially invited.

Teams link: <https://bit.ly/3zSvNew>

[Contact](mailto:pierre-marc.jodoin@usherbrooke.ca)
