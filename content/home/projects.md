---
# An instance of the Pages widget.
# Documentation: https://wowchemy.com/docs/page-builder/
# https://bootstrap.hugoblox.com/blocks-v1/portfolio/
widget: portfolio

# This file represents a page section.
headless: true

# Change 'active' to 'true' to show this section
active: true
# Order that this section appears on the page.
weight: 50

title: Projects
subtitle: ''

content:
  # Filter on criteria
  filters:
    folders:
      - projects
    tag: ''
    category: ''
    publication_type: ''
    author: ''
    exclude_featured: false
    exclude_future: false
    exclude_past: false
  # Choose how many pages you would like to display (0 = all pages)
  count: 5
  # Choose how many pages you would like to offset by
  offset: 0
  # Page order: descending (desc) or ascending (asc) date.
  order: desc

design:
  # Choose a view for the listings:
  view: Card
  columns: '2'
---