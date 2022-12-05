---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Detecting and Eliminating Quantum Noise of Quantum Measurements"
subtitle: ''
summary: ''
authors:
- Shuanghong Tang
- Congcong Zheng
- admin
tags: 
- twirling
- quantum error mitigation
- measurement error mitigation
categories: 
- research
date: '2022-06-28'
lastmod: '2022-06-28'
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: 'Two Stage Framework'
  focal_point: ''
  preview_only: false

# Links:
url_pdf: https://arxiv.org/pdf/2206.13743
# url_source: 'https://arxiv.org/abs/2206.13743'
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
publishDate: '2022-06-28'
publication_types:
- '2'
abstract: "In this work, we propose a two-stage procedure to systematically address quantum noise inherent in quantum measurements. The idea behind it is intuitive: we first detect and then eliminate quantum noise so that the classical noise assumption is satisfied and measurement error mitigation works. In the first stage, inspired by coherence witness in the resource theory of quantum coherence, we design an efficient method to detect quantum noise. It works by fitting the difference between two measurement statistics to the Fourier series, where the statistics are obtained using maximally coherent states with relative phase and maximally mixed states as inputs. The fitting coefficients quantitatively benchmark quantum noise. In the second stage, we design various methods to eliminate quantum noise, inspired by the Pauli twirling technique. They work by executing randomly sampled Pauli gates before the measurement device and conditionally flipping the measurement outcomes in such a way that the effective measurement device contains only classical noise. We demonstrate the feasibility of the two-stage procedure numerically on Baidu Quantum Platform. Remarkably, the results show that quantum noise in measurement devices is significantly suppressed, and the quantum computation accuracy is substantially improved. We highlight that the two-stage procedure complements existing measurement error mitigation techniques, and they together form a standard toolbox for manipulating measurement errors in near-term quantum devices."
publication: '*arXiv preprint arXiv:2206.13743*'
---
