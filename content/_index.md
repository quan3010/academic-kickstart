---
# Leave the homepage title empty to use the site title
title:
date: 2024-01-01
type: landing

sections:
  - block: hero
    content:
      title: Quan Nguyen
      image:
        filename: avatar.jpg
      text: |
        Assistant Professor in Computer Science at Thompson Rivers University
        
        My research focuses on **Learning Analytics**, **Generative AI in Education**, and **Data Science Education**.
    design:
      columns: '1'
      background:
        color: ''
        image:
          filename: ''
          filters:
            brightness: 0.3
          size: cover
          position: center
          parallax: false
        text_color_light: false
  
  - block: markdown
    content:
      title: About Me
      text: |
        I am a tenure-track Assistant Professor in the Computer Science department at Thompson Rivers University. My research centers on the impact of generative AI on the learning behavior and outcomes in computer science education. Before joining TRU, I was a Postdoctoral Fellow at the UBC Master of Data Science, where I developed and taught a variety of data science courses, including those on statistical inference, machine learning, and technical communication.
        
        Prior to UBC, I worked as a Postdoctoral Fellow in Learning Analytics at the School of Information, University of Michigan. My work has been recognized with competitive grants and multiple best paper awards at prominent conferences, including LAK18 and HCI International 2017.
        
        I hold a PhD in Learning Analytics from The Open University UK, and a BSc and MSc in Economics from Maastricht University, Netherlands.
    design:
      columns: '1'
  
  - block: collection
    id: publications
    content:
      title: Featured Publications
      text: ''
      count: 5
      filters:
        folders:
          - publication
        featured_only: true
    design:
      view: citation
      columns: '1'
  
  - block: collection
    id: events
    content:
      title: Recent & Upcoming Events
      subtitle: Talks, Awards, and Recognitions
      text: ''
      count: 5
      filters:
        folders:
          - event
    design:
      view: compact
      columns: '1'

  - block: markdown
    content:
      title: Research Interests
      text: |
        - **Learning Analytics**: Analyzing student behavioral data to understand learning patterns
        - **Generative AI in Education**: Investigating how AI can support teaching and learning
        - **Data Science Education**: Developing curricula and pedagogical approaches for data science
        - **Student Success Modeling**: Building predictive models while ensuring fairness and equity
    design:
      columns: '1'
  
  - block: markdown
    content:
      title: Contact
      text: |
        - **Email:** [lnguyen@tru.ca](mailto:lnguyen@tru.ca)
        - **Twitter:** [@Quannguyen3010](https://twitter.com/Quannguyen3010)
        - **GitHub:** [quan3010](https://github.com/quan3010)
        - **Google Scholar:** [Quan Nguyen](https://scholar.google.co.uk/citations?user=2ELBBq4AAAAJ&hl=en)
        - **CV:** [View CV](https://drive.google.com/file/d/1nAxA2flz-hjFaie8ZBzqqpmtM6FWJbwo/view?usp=sharing)
    design:
      columns: '1'
---
