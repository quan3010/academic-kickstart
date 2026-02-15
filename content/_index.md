---
title: ""
date: 2024-01-01
type: landing

sections:
  - block: resume-biography-3
    content:
      username: admin
    design:
      css_class: dark
      background:
        color: black
        image:
          filename: stacked-peaks.svg
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false

  - block: collection
    content:
      title: News
      count: 5
      filters:
        folders:
          - events
    design:
      view: date-title-summary

  - block: collection
    content:
      title: Featured Publications
      text: |-
        [See all publications on Google Scholar](https://scholar.google.co.uk/citations?user=2ELBBq4AAAAJ&hl=en)
      count: 5
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: citation
---
