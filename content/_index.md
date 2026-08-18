---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-08-18
type: landing

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      headings:
        about: '关于我'
        education: '教育经历'
        interests: '兴趣'
    design:
      # Use the new Gradient Mesh which automatically adapts to the selected theme colors
      background:
        gradient_mesh:
          enable: true

      # Name heading sizing to accommodate long or short names
      name:
        size: md # Options: xs, sm, md, lg (default), xl

      # Avatar customization
      avatar:
        size: medium # Options: small (150px), medium (200px, default), large (320px), xl (400px), xxl (500px)
        shape: circle # Options: circle (default), square, rounded
  - block: markdown
    content:
      title: '📝 关于本站'
      subtitle: ''
      text: |-
        这里是我的个人主页，用来记录和分享：

        - **学习与工作经历**：见「经历」页面
        - **做过的项目**：见「项目」页面
        - **写过的文章**：见「博客」页面

        欢迎通过 [GitHub](https://github.com/gskgskgsk) 与我交流 😃
    design:
      columns: '1'
  - block: collection
    id: news
    content:
      title: '📰 最新动态'
      subtitle: ''
      text: ''
      # Page type to display. E.g. post, talk, publication...
      page_type: blog
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: card
      # Reduce spacing
      spacing:
        padding: [0, 0, 0, 0]
---
