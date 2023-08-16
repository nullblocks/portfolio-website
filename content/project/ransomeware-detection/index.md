---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Ransomeware Detection"
subtitle: "❗❗❗ Research of Major Project ❗❗❗"
summary: "Detecting ransomeware and their families by doing dynamic analyisis & observing paranoia activity . "
authors: []
tags: [ML , python]
categories: []
date: 2023-08-03T02:40:27+05:30
lastmod: 2023-08-03T02:40:27+05:30
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
While doing Research our Guide share two paper related to this approach . 

### Paper1 
Link of paper1 [https://ieeexplore.ieee.org/document/9536608](https://ieeexplore.ieee.org/document/9536608)

Paper In short : It classify the type of ransomeware family (out of 5 family used to train model ) from doing dynamic analysisi or observing paranoia activity / API calls . 

### Paper 2
Link of paper [https://doi.org/10.1016/j.jksuci.2020.06.012](https://doi.org/10.1016/j.jksuci.2020.06.012)

Architecture we are goin to implement / follow 
![](Archi.png)

We can also explore the hybrid approch i.e static and dynamic analysis to find ransomeware and then identify it's family . 