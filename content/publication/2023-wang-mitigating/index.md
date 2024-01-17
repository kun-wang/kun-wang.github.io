---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Mitigating quantum errors via truncated Neumann series"
subtitle: ''
summary: ''
authors:
- admin
- Yu-Ao Chen
- Xin Wang
author_notes:
- "Corresponding Author"
doi: "10.1007/s11432-023-3786-1"
tags: 
- quantum error mitigation
- gate error mitigation
- Neumann series
categories: 
- research
date: '2023-07-05'
featured: yes
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: 'Smart'
  preview_only: false

# links:
url_pdf: 'https://arxiv.org/pdf/2111.00691'
url_source: 'https://link.springer.com/article/10.1007/s11432-023-3786-1'
# url_dataset: ''
# url_poster: ''
# url_project: ''
# url_slides: ''
# url_source: ''
# url_video: ''

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2023-07-05'
publication_types:
- '2'
abstract: "Quantum gates and measurements on quantum hardware are inevitably subject to hardware imperfections that lead to quantum errors. Mitigating such unavoidable errors is crucial to explore the power of quantum hardware better. In this paper, we propose a unified framework that can mitigate quantum gate and measurement errors in computing quantum expectation values utilizing the truncated Neumann series. The essential idea is to cancel the effect of quantum error by approximating its inverse via linearly combining quantum errors of different orders produced by sequential applications of the quantum devices with carefully chosen coefficients. Remarkably, the estimation error decays exponentially in the truncated order, and the incurred error mitigation overhead is independent of the system size, as long as the noise resistance of the quantum device is moderate. We numerically test this framework for different quantum errors and find that the computation accuracy is substantially improved. Our framework possesses several vital advantages: it mitigates quantum gate and measurement errors in a unified manner, it neither assumes any error structure nor requires the tomography procedure to completely characterize the quantum errors, and most importantly, it is scalable. These advantages empower our quantum error mitigation framework to be efficient and practical and extend the ability of near-term quantum devices to deliver quantum applications."
publication: '*Science China Information Sciences*'
---
