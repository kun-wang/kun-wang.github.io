---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Detecting and quantifying entanglement on near-term quantum devices"
subtitle: ''
summary: ''
authors:
- admin
- Zhixin Song
- Xuanqiang Zhao
- Zihe Wang
- Xin Wang
doi: "10.1038/s41534-022-00556-w"
tags: 
- quantum entanglement detection
- noisy intermediate-scale quantum
- positive map criterion
categories: 
- research
date: '2022-05-09'
lastmod: '2022-05-09'
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Links
url_pdf: https://www.nature.com/articles/s41534-022-00556-w.pdf
url_source: 'https://arxiv.org/abs/2012.14311'
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
publishDate: '2022-05-09'
publication_types:
- '2'
abstract: "Quantum entanglement is a key resource in quantum technology, and its quantification is a vital task in the current noisy intermediate-scale quantum (NISQ) era. This paper combines hybrid quantum-classical computation and quasi-probability decomposition to propose two variational quantum algorithms, called variational entanglement detection (VED) and variational logarithmic negativity estimation (VLNE), for detecting and quantifying entanglement on near-term quantum devices, respectively. VED makes use of the positive map criterion and works as follows. Firstly, it decomposes a positive map into a combination of quantum operations implementable on near-term quantum devices. It then variationally estimates the minimal eigenvalue of the final state, obtained by executing these implementable operations on the target state and averaging the output states. Deterministic and probabilistic methods are proposed to compute the average. At last, it asserts that the target state is entangled if the optimized minimal eigenvalue is negative. VLNE builds upon a linear decomposition of the transpose map into Pauli terms and the recently proposed trace distance estimation algorithm. It variationally estimates the well-known logarithmic negativity entanglement measure and could be applied to quantify entanglement on near-term quantum devices. Experimental and numerical results on the Bell state, isotropic states, and Breuer states show the validity of the proposed entanglement detection and quantification methods."
publication: '*npj Quantum Information*'
---
