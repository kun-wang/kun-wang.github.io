---
# An instance of the Pages widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: collection

# This file represents a page section.
headless: true

# Change 'active' to 'true' to show this section
active: true
# Order that this section appears on the page.
weight: 40

title: Recent Publications
subtitle: ''
content:
  # Filter on criteria
  filters:
    folders:
      - publication
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
  # Control the "See all" link
  # https://bootstrap.hugoblox.com/blocks-v1/collection/
  archive: 
    enable: true
    text: SEE ALL PUBLICATIONS
    link: publication/
design:
  # Choose a view for the listings:
  view: citation
  columns: '2'
---

<!-- {{% callout note %}}
Quickly discover relevant content by [filtering publications](./publication/).
{{% /callout %}} -->
