---
# Documentation: https://docs.hugoblox.com/reference/page-features/

title: "Cross-Platform Comparison of Arbitrary Quantum Processes"
# The @summary content will be accessed when this paper is featured
summary: ''
authors:
- Congcong Zheng
- Xutao Yu
- admin
author_notes:
- 
- "Corresponding Author"
- "Corresponding Author"
doi: "10.1038/s41534-023-00797-3"
tags: 
- quantum estimation
- noisy intermediate-scale quantum
- QCVV
categories: 
- research
- project
date: '2024-01-03'
lastmod: '2024-01-03'
featured: false
draft: false

# Featured image
# To use, place an image named `featured.jpg/png` in your page's folder.
# Otherwise, specify the `filename` option to load an image from your `assets/media/` folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
# Set `preview_only` to `true` to just use the image for thumbnails.
image:
  placement: 1
  caption: ''
  focal_point: ''
  preview_only: false

# Links
url_pdf: https://www.nature.com/articles/s41534-023-00797-3.pdf
url_source: 'https://www.nature.com/articles/s41534-023-00797-3'
url_project: 'https://pypi.org/project/qcompute-qep/'
# url_dataset: ''
# url_poster: ''
# url_slides: ''
# url_video: ''

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: [qep]
publication: '*npj Quantum Information*'
publishDate: '2024-01-03'
publication_types:
- '2'
abstract: "In this work, we present a protocol for comparing the performance of arbitrary quantum processes executed on spatially or temporally disparate quantum platforms using Local Operations and Classical Communication (LOCC). The protocol involves sampling local unitary operators, which are then communicated to each platform via classical communication to construct quantum state preparation and measurement circuits. Subsequently, the local unitary operators are implemented on each platform, resulting in the generation of probability distributions of measurement outcomes. The max process fidelity is estimated from the probability distributions, which ultimately quantifies the relative performance of the quantum processes. Furthermore, we demonstrate that this protocol can be adapted for quantum process tomography. We apply the protocol to compare the performance of five quantum devices from IBM and the Qianshi quantum computer from Baidu via the cloud. The experimental results unveil two notable aspects: Firstly, the protocol adeptly compares the performance of the quantum processes implemented on different quantum computers. Secondly, the protocol scales, although still exponentially, much more favorably with the number of qubits, when compared to the full quantum process tomography. We view our work as a catalyst for collaborative efforts in cross-platform comparison of quantum computers."
---
