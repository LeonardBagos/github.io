---
title: Home
slug: /
sections:
  - type: GenericSection
    title:
      text: LEONARD BAGOS
      color: text-dark
      type: TitleBlock
      styles:
        self:
          textAlign: center
          fontWeight: 700
    subtitle: Data Analyst
    text: >
      Welcome to my online portfolio! I am a licensed Chemical Engineer turned
      Data Analyst. I have a proven track record of streamlining operations,
      elevating decision-making processes, and optimizing efficiency by crafting
      data-driven dashboards, all of which have significantly contributed to my
      clients' success. Each project in this portfolio reflects a dedication to
      mastery and precision, as I aim to instill confidence in the quality of my
      work.
    actions:
      - label: About Me
        altText: ''
        url: /aboutme
        showIcon: false
        icon: arrowRight
        iconPosition: right
        style: primary
        elementId: ''
        type: Button
      - altText: ''
        showIcon: true
        icon: arrowRight
        iconPosition: right
        style: primary
        elementId: ''
        type: Link
        label: Download CV
        url: 'https://bit.ly/47ku4fv'
    media:
      url: /images/asaa.png
      altText: Unblock your team boost your time to production preview
      elementId: ''
      type: ImageBlock
    badge:
      color: text-primary
      type: Badge
    elementId: ''
    colors: bg-light-fg-dark
    styles:
      self:
        alignItems: center
        flexDirection: row
        padding:
          - pt-16
          - pl-16
          - pb-16
          - pr-16
        justifyContent: center
      subtitle:
        textAlign: center
        fontWeight: 700
      text:
        textAlign: center
    backgroundImage:
      type: BackgroundImage
      altText: altText of the image
      backgroundSize: cover
      backgroundPosition: center
      backgroundRepeat: no-repeat
      opacity: 47
      url: /images/abstract-feature2.svg
  - images:
      - url: /images/sql-5a7a26d6.png
        altText: Empathy logo
        type: ImageBlock
      - url: /images/power bi.png
        altText: Wellster logo
        type: ImageBlock
      - url: /images/tableau.png
        altText: Vise logo
        type: ImageBlock
      - url: /images/python.png
        altText: Telus logo
        type: ImageBlock
      - altText: Contentful logo
        type: ImageBlock
      - altText: Sanity logo
        type: ImageBlock
      - url: /images/excel.png
        altText: Rangle logo
        type: ImageBlock
    motion: move-to-left
    colors: bg-light-fg-dark
    styles:
      self:
        justifyContent: center
      subtitle:
        textAlign: center
    type: ImageGallerySection
    title:
      type: TitleBlock
      text: 'Proficient on the following programs:'
      color: text-dark
      styles:
        self:
          textAlign: center
  - title:
      color: text-dark
      styles:
        self:
          textAlign: center
          fontStyle: italic
          fontWeight: 400
      type: TitleBlock
      text: '"Your Data Analyst, Your Partner"'
    text: |+
      <div style="text-align: center">******</div>

    media:
      url: 'https://youtu.be/h2y98ejwbGI'
      controls: true
      aspectRatio: '16:9'
      styles:
        self:
          padding:
            - pt-2
            - pb-2
            - pl-2
            - pr-2
          borderColor: border-dark
          borderStyle: solid
          borderWidth: 1
          borderRadius: large
      type: VideoBlock
      autoplay: false
      loop: true
      muted: true
      title: Rejection Reduction Dashboard
    badge:
      color: text-primary
      styles:
        self:
          textAlign: center
      type: Badge
    colors: bg-light-fg-dark
    styles:
      self:
        flexDirection: col
        justifyContent: center
      subtitle:
        textAlign: center
    type: GenericSection
  - posts:
      - content/pages/blog/case-study-1.md
      - content/pages/blog/case-study-2.md
      - content/pages/blog/case-study-3.md
      - >-
        content/pages/blog/how-to-write-a-blog-post-that-will-get-you-more-traffic.md
      - content/pages/blog/five-tips-for-starting-a-startup.md
      - content/pages/blog/track-the-right-metrics-for-your-business.md
    showThumbnail: true
    showDate: true
    showAuthor: true
    variant: three-col-grid
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-16
          - pl-16
          - pb-16
          - pr-16
        justifyContent: center
    type: FeaturedPostsSection
    title:
      type: TitleBlock
      text: MY PERSONAL PROJECTS
      color: text-dark
      styles:
        self:
          textAlign: center
          fontWeight: 700
  - title:
      text: Certificates
      color: text-primary
      styles:
        self:
          textAlign: center
      type: TitleBlock
    items:
      - title: Core Track of Data Analytics Course
        subtitle: 'Refocus Digital Academy, March 2023'
        image:
          url: /images/asasa.png
          altText: Placeholder Image
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        colors: bg-dark-fg-light
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
            textAlign: left
        type: FeaturedItem
        actions:
          - type: Button
            label: View Certificate
            altText: ''
            showIcon: true
            icon: arrowRight
            iconPosition: right
            style: secondary
            elementId: ''
            url: >-
              https://drive.google.com/file/d/1xek9tYoa5wL6kXtNEiAr1HebOjlnKYUJ/view?usp=sharing
      - image:
          url: /images/DataScientist.png
          altText: Placeholder image
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        colors: bg-dark-fg-light
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
        type: FeaturedItem
        title: Data Scientist
        subtitle: 'SPARTA Data Science Pathway, Aug 2023'
        actions:
          - type: Button
            label: View Certificate
            altText: ''
            url: >-
              https://drive.google.com/file/d/1g6eMDV4lyAMYhl1Puc1WD9tkTsh2OGQL/view?usp=sharing
            showIcon: true
            icon: arrowRight
            iconPosition: right
            style: secondary
            elementId: ''
      - title: Power BI Data Analyst Certificate
        subtitle: 'Microsoft thru Coursera, Sept. 2023'
        image:
          url: /images/Datacert.png
          altText: Placeholder image
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        colors: bg-dark-fg-light
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
        type: FeaturedItem
        actions:
          - type: Button
            label: View Certificate
            altText: ''
            showIcon: true
            icon: arrowRight
            iconPosition: right
            style: secondary
            elementId: ''
            url: >-
              https://www.coursera.org/account/accomplishments/verify/R7MZGCG865SD
      - type: FeaturedItem
        title: Data Analytics Virtual Internship Program
        subtitle: 'KPMG thru Forage, March 2023'
        image:
          url: /images/Screenshot 2023-04-02 005309.png
          altText: Placeholder text
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        actions:
          - type: Button
            label: View Certificate
            altText: ''
            url: >-
              https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/KPMG%20AU/m7W4GMqeT3bh9Nb2c_KPMG%20AU_iLykWE4TBcoRjmazn_1678122961704_completion_certificate.pdf
            showIcon: true
            icon: arrowRight
            iconPosition: right
            style: secondary
            elementId: ''
        elementId: null
        colors: bg-dark-fg-light
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
    variant: two-col-grid
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-16
          - pl-8
          - pb-16
          - pr-8
        justifyContent: center
      subtitle:
        textAlign: center
    type: FeaturedItemsSection
  - type: GenericSection
    title:
      text: Check out my Power BI Portfolio
      color: text-dark
      styles:
        self:
          textAlign: center
          fontWeight: 700
      type: TitleBlock
    subtitle: Interact with my Power BI Dashboards here..
    actions:
      - type: Button
        label: Visit my portfolio
        altText: ''
        url: 'https://bit.ly/3KoHoaz'
        showIcon: true
        icon: arrowRight
        iconPosition: right
        style: primary
        elementId: ''
    media:
      url: 'https://youtu.be/1B99ZkSaU9k'
      autoplay: false
      loop: true
      muted: true
      controls: true
      aspectRatio: '16:9'
      styles:
        self:
          padding:
            - pt-2
            - pb-2
            - pl-2
            - pr-2
          borderColor: border-dark
          borderStyle: solid
          borderWidth: 1
          borderRadius: large
      type: VideoBlock
      title: Olist Dashboard
    elementId: null
    colors: bg-light-fg-dark
    styles:
      self:
        flexDirection: row
        justifyContent: center
        alignItems: center
      subtitle:
        textAlign: center
  - title:
      text: Check out more Blogs here
      color: text-dark
      type: TitleBlock
      styles:
        self:
          textAlign: center
          fontWeight: 700
    subtitle: Data Storytelling in Medium
    actions:
      - label: Visit the page
        icon: arrowLeft
        iconPosition: left
        style: primary
        type: Button
        showIcon: true
        url: 'https://bit.ly/3GzgzOD'
    media:
      url: /images/x.PNG
      altText: Dope design preview
      type: ImageBlock
    badge:
      color: text-primary
      type: Badge
    colors: bg-light-fg-dark
    styles:
      self:
        alignItems: center
        flexDirection: row-reverse
        justifyContent: center
      subtitle:
        textAlign: center
    type: GenericSection
  - title:
      text: 'If you have problems with your data, let me analyze them for you!'
      color: text-dark
      type: TitleBlock
    subtitle: 'Email: leonardbagos9@gmail.com'
    media:
      fields:
        - name: name
          label: Name
          hideLabel: true
          placeholder: Your name
          isRequired: true
          width: full
          type: TextFormControl
        - name: email
          label: Email
          hideLabel: true
          placeholder: Your email
          isRequired: true
          width: full
          type: EmailFormControl
        - name: message
          label: Message
          hideLabel: true
          placeholder: Your message
          width: full
          type: TextareaFormControl
      action: /.netlify/functions/submission_created
      elementId: contact-form
      styles:
        self:
          padding:
            - pt-6
            - pb-6
            - pl-6
            - pr-6
          borderColor: border-dark
          borderStyle: solid
          borderWidth: 1
          borderRadius: large
      type: FormBlock
      submitButton:
        type: SubmitButtonFormControl
        label: Submit
        showIcon: false
        icon: arrowRight
        iconPosition: right
        style: primary
        elementId: null
    badge:
      label: Contact ME
      color: text-primary
      type: Badge
    colors: bg-light-fg-dark
    type: GenericSection
    styles:
      self:
        alignItems: center
        justifyContent: center
seo:
  metaTitle: Home - Demo site
  metaDescription: This demo site is built with Stackbit
  socialImage: /images/main-hero.svg
  type: Seo
type: PageLayout
---
