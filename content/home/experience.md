---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 10

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
  - title: Senior Researcher
    company: Institute for Quantum Computing, Baidu Research
    company_url: 'https://quantum.baidu.com/'
    # company_logo: org-gc
    location: Shenzhen, China
    date_start: '2020-08-12'
    date_end: ''
    description: |2-
        Research on quantum error processing and 
        lead the development of [QEP](https://quantum-hub.baidu.com/qep/tutorial-overview) toolkit, 
        which manipulates quantum errors inherent in quantum devices using software solutions.

  - title: Postdoc
    company: Shenzhen Institute for Quantum Science and Engineering, SUSTech
    company_url: 'https://siqse.sustech.edu.cn/'
    # company_logo: org-x
    location: Shenzhen, China
    date_start: '2019-06-20'
    date_end: '2020-07-31'
    description: Research on quantum information theory and quantum verification.

design:
  columns: '2'
---
