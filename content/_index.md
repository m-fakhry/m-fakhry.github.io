---
# Leave the homepage title empty to use the site title
title: ""
date: 2025-02-13
type: landing

design:
  # Default section spacing
  spacing: "2rem"
  # background:
  #   # Choose a color such as from https://html-color-codes.info
  #   color: 'navy'
  #   # Text color (true=light, false=dark, or remove for the dynamic theme color).
  #   text_color_light: false

# blocks: can be found in here https://bootstrap.hugoblox.com/blocks/ and https://hugoblox.com/blocks/
# bootstrap: markdown, people, about.biography, about.avatar, testimonials, skills, logos, pricing, accomplishments, contact, experience, features, hero, collection, portfolio, slider, tag_cloud
# tailwind: biography, resume-biography, resume-experience, resume-skills, resume-awards, resume-languages, cta-button-list, cta-card, hero, markdown, experience, skills, awards, languages
# stats, features, cta-image-paragraph, testimonials, cta-button-list

# collection: citation, article-grid, date-title-summary ---- citation, card, list, compact, masonry, showcase, article-grid
# experinece: Timeline, list
# Skills: Progress, list 
# portfolio: card, masonry, showcase
# posts: card, list, compact, masonry, showcase
# publications: card, list, compact, masonry, showcase
# people: card, list
# gallery: masonry, Slideshow
# contact: form, details 
# about: default, resume


# finally, I found these blox on the hugo lib in my mac "/Users/mohamedghalwash/Library/Caches/hugo_cache/modules/filecache/modules/pkg/mod/github.com/\!hugo\!blox/hugo-blox-builder/modules/blox-tailwind\@v0.3.1/layouts/partials/" and can also be found in https://github.com/HugoBlox/hugo-blox-builder/tree/main/modules/blox-tailwind/layouts/partials
# resume-biography-3, resume-experience, resume-skills, resume-awards, resume-biography, resume-languages, 
# cta-card, cta-button-list, cta-image-paragraph, collection, features, markdown, testimonials, hero, stats

# views: article-grid, card, citation, date-title-summary

# to get details about a certain blox: https://github.com/HugoBlox/hugo-blox-builder/blob/main/modules/blox-tailwind/layouts/partials/blox/

sections:

  #############################
  ######## About Me ###########
  #############################
  - block: resume-biography-3 # resume-biography-3
    id: about
    content:
      username: mohamed-ghalwash
      text: ""
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      # css_class: light
      avatar:
        shape: rounded   # circle | square | rounded
        size: large    # small | medium | large | xl | xxl
      background:
        color: Gainsboro  
        # text_color_light: false
        # image:
        # gradient: 
      biography:
        style: 'text-align: justify; font-size: 1em;'

  #############################
  ###### Publications #########
  #############################
  - block: collection
    id: publications # this will be used in the menubar
    content:
      title: Publications # this is the title when publication in the home page 
      filters: # Filter on criteria
        folders: # The folders to display content from
          - publications 
        featured_only: false
      count: 4 # Choose how many pages you would like to display (0 = all pages)
    design:
      view: date-title-summary # citation, article-grid, date-title-summary
      # css_class: dark
      background:
        color: LightGrey
        # text_color_light: false
      columns: 4

  #############################
  ###### Invited Talks ########
  #############################
  - block: collection
    id: talks # this will be used in the menubar
    content:
      title: Invited Talks # this is the title when publication in the home page 
      # Filter on criteria
      filters:
        # The folders to display content from
        folders:
          - talks 
        featured_only: false
    design:
      view: article-grid
      columns: 4
      # css_class: light
      # background:
      #   color: gray
      background:
        color: Gainsboro

  #############################
  ########## Awards ###########
  #############################
  # icons can be found here https://github.com/tailwindlabs/heroicons/blob/master/optimized/24/solid/academic-cap.svg
  - block: features
    id: awards
    content:
      title: Awards  
      items:
        - name: Publication Awards
          icon: star
          description: Ain Shams University. Class 31 - For my publication in Lancet Diabetes and Endocrinology. 2023/01
        - name: Publication Awards
          icon: star
          description: Ain Shams University. Class 30 - For my publication in Diabetes Care. 2022/07
        - name: Patent Plateau Award
          icon: bars-4
          description: IBM Research. Completing four USA/international patents. 2021/06
        - name: Patent Plateau Award
          icon: bars-4
          description: IBM Research. Completing four USA/international patents. 2019/06
        - name: Best Graduate Paper
          icon: trophy
          description: ACM Future of Computing. Golden Prize. 2013/05
        - name: Student Travel Award
          icon: ticket
          description: IEEE International Conference on Bioinformatics and Biomedicine. Awarded for presenting a paper in the conference. 2012/07
        - name: Best Graduate Paper
          icon: trophy
          description: ACM Future of Computing. Golden Prize. 2012/05
        - name: Graduate Scholarship
          icon: academic-cap
          description: Ministry of Higher Education, Egypt. Awarded for pursuing PhD in United States of America. 2009/08-2013/08
    design:
      spacing:
        padding: [1rem, 0, 3rem, 0]   # top, right, bottom, left — match Publications/Talks
      background:
        color: LightGrey  

  #############################
  ######### Services ##########
  #############################
  - block: markdown
    id: services
    content:
      title: Services
      subtitle: Synergetic Activities to the Research Community
      text: |-
        **Editorial Board Member**

        <div class="space-y-2 mb-6">
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://home.liebertpub.com/publications/big-data/611/editorial-board">Big Data</a>
            <span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2020 - 2024</span>
          </div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://www.jsmcentral.org/Bioinformatics/editors.php">SM Bioinformatics, Genomics and Proteomics</a>
            <span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2016 - Present</span>
          </div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://www.inderscience.com/jhome.php?jcode=ijdmb">International Journal of Data Mining and Bioinformatics</a>
            <span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2015 - Present</span>
          </div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://www.sciedupress.com/journal/index.php/jbei">Journal of Biomedical Engineering and Informatics</a>
            <span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2016 - 2019</span>
          </div>
        </div>

        **Session Chair**

        <div class="space-y-2 mb-6">
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://ieeexplore.ieee.org/xpl/conhome/6724379/proceeding">International Conference of Data Mining (ICDM)</a>
            <span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2013</span>
          </div>
        </div>

        **PC Member**

        <div class="space-y-2 mb-6">
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>IEEE Big Data</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2017, 2018, 2019, 2020, 2021, 2022</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>NeurIPS</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2017, 2018, 2019, 2022, 2023-2026</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>AMIA</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2018, 2019, 2020, 2021, 2022</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>SDM</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2017, 2018, 2019, 2020</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>ICLR</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2018, 2019, 2020</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>IJCAI</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2018, 2019, 2020</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>International Journal of Medical Informatics</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2020, 2021</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>ICML</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2022</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>AAAI</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2020</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>International Conference on Decision Support System Technology</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2015</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>Conference of Artificial Intelligence in Medicine (AIME), 1st Workshop on Matrix Computations for Biomedical Informatics</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2015</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>International Conference on BioInformatics and BioEngineering (BIBE)</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2015</span></div>
        </div>

        **Reviewer**

        <div class="space-y-2 mb-6">
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://www.hindawi.com/journals/bmri/">BioMed Research International Journal</a>
          </div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5">
            <a href="https://www.springer.com/journal/10994">Machine Learning Journal</a>
            <span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">special issue for Health and Medicine</span>
          </div>
        </div>

        **Ad-hoc Reviewer**

        <div class="space-y-2">
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>SDM</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2012, 2013, 2014</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>KDD</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2013, 2014, 2015</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>ICDM</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2012, 2015</span></div>
          <div class="flex flex-wrap justify-between gap-x-4 gap-y-0.5"><span>BigData</span><span class="text-sm text-gray-500 dark:text-gray-400 whitespace-nowrap">2013, 2015</span></div>
        </div>
    design:
      background:
        color: Gainsboro

  - block: collection
    id: students
    content:
      title: PostGraduate Students  
      count: 0 # show all students
      filters:
        folders:
          - students
        author: ""
        category: ""
        tag: "" # MSC, PHD
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      order: asc # desc, asc
    design:
      view: article-grid # card, date-title-summary, article-grid
      columns: 4
      spacing:
        padding: [10, 0, 0, 0]   # top, right, bottom, left — match Publications/Talks
      background:
        color: LightGrey

  #############################
  ########## Courses ###########
  #############################

  - block: features
    id: courses 
    content:
      title: Courses  
      items:
        - name: Logic Design
          icon: book-open
          description: CSAI 102. Zewail City of Science, Technology and Innovation
        - name: MLOps
          icon: book-open
          description: DSAI 406. Zewail City of Science, Technology and Innovation
        - name: Speech Recognition
          icon: book-open
          description: DSAI 456. Zewail City of Science, Technology and Innovation
        - name: Reinforcement Learning
          icon: book-open
          description: DSAI 402. Zewail City of Science, Technology and Innovation
        - name: Programming Language (C++)
          icon: book-open
          description: Comp 104. Ain Shams University.
        - name: Formal Syntax and Semantics
          icon: book-open
          description: Comp 303. Ain Shams University.
        - name: Compiler Design
          icon: book-open
          description: Comp 304. Ain Shams University.
        - name: Bioinformatics
          icon: book-open
          description: Comp 402. Ain Shams University.
        - name: Parallel Computing
          icon: book-open
          description: Comp 403. Ain Shams University.
        - name: Mathematics for Machine Learning
          icon: book-open
          description: Comp 603. Ain Shams University.
        - name: Deep Learning
          icon: book-open
          description: Comp 612. Ain Shams University.
        - name: Advanced AI 
          icon: book-open
          description: CIS 702. The Arab Academy for Science, Technology and Maritime Transport.
    design:
      background:
        color: Gainsboro  

  #############################
  ####### Experience ##########
  #############################
  - block: resume-experience # resume-biography-3
    id: experience
    content:
      username: mohamed-ghalwash
      text: ""
    design:
      # css_class: light
      # background:
      #   color: light-grey
      # biography:
      #   style: 'text-align: justify; font-size: 0.8em;'
      background:
        color: LightGrey  
  
  #############################
  ########## Skills ###########
  #############################
  - block: resume-skills
    id: skills
    content:
      username: mohamed-ghalwash
      title: Skills & Hobbies
    design:
      show_skill_percentage: false
      background:
        color: Gainsboro

  #############################
  ######## Projects ###########
  #############################
  - block: portfolio
    id: projects
    content:
      title: Projects
      count: 6
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: Software
          tag: Software
        - name: AI Research
          tag: AI Research
      default_button_index: 0
      archive:
        link: /projects/
    design:
      spacing:
        padding: ['3rem', 0, '6rem', 0]
      # css_class: light
      columns: 3
      fallback_icon: code-bracket
      background:
        color: LightGrey

  #############################
  ########## Grants ###########
  #############################
  - block: collection
    id: grants
    content:
      title: Grants
      # Same "projects" folder, filtered down to entries tagged "Grant"
      filters:
        folders:
          - projects
        tag: "Grant"
        count: 0
    design:
      spacing:
        padding: ['3rem', 0, '6rem', 0]
      view: article-grid # date-title-summary
      fill_image: false
      columns: 3
      background:
        color: Gainsboro

  #############################
  ########### Map #############
  #############################
  - block: map
    id: map
    content:
      title: Fun
      subtitle: Places I've visited
      markers:
      - lat: 60.169856
        lng: 24.938379
        title: Helsinki — Visit for a JDRF meeting
      - lat: 60.451813
        lng: 22.26663
        title: Turku
      - lat: 59.329323
        lng: 18.068581
        title: Stockholm
      - lat: 55.604981
        lng: 13.003822
        title: Malmö
      - lat: 51.507218
        lng: -0.127586
        title: London
      - lat: 39.952584
        lng: -75.165222
        title: Philadelphia
      - lat: 40.712775
        lng: -74.005973
        title: New York
      - lat: 41.270927
        lng: -73.777634
        title: Yorktown Heights
      - lat: 42.360082
        lng: -71.05888
        title: Boston
      - lat: 42.652579
        lng: -73.756232
        title: Albany
      - lat: 42.034771
        lng: -72.613627
        title: 1623 Main St — Six flags
      - lat: 40.13606
        lng: -74.436163
        title: Six Flags Great Adventure
      - lat: 39.744012
        lng: -104.838333
        title: '1775 Aurora Ct # A140 — JDRF'
      - lat: 41.851384
        lng: -87.616251
        title: ICNA 2019
      - lat: 38.907192
        lng: -77.036871
        title: Washington — Museums
      - lat: 39.290385
        lng: -76.612189
        title: Baltimore — Visit relatives and friends
      - lat: 28.377186
        lng: -81.57074
        title: Walt Disney World® Resort
      - lat: 49.282729
        lng: -123.120738
        title: Vancouver — NeurIPS
      - lat: 47.606209
        lng: -122.332071
        title: Seattle — AMIA 2023
      - lat: 1.352083
        lng: 103.819836
        title: Singapore — CIKM 2017
      - lat: 25.204849
        lng: 55.270783
        title: Dubai — Family Trip Dec, 2022
      - lat: 21.389082
        lng: 39.857912
        title: Mecca — 2008
      - lat: 24.524654
        lng: 39.569184
        title: Medina — 2008
      - lat: 21.485811
        lng: 39.192505
        title: Jeddah — 2008
      - lat: 33.57311
        lng: -7.589843
        title: Casablanca — Transit
      - lat: 29.760427
        lng: -95.369803
        title: Houston — WSDM 2020
      - lat: 30.04442
        lng: 31.235712
        title: Cairo
      - lat: 31.200092
        lng: 29.918739
        title: Alexandria
      - lat: 25.687243
        lng: 32.639636
        title: Luxor — Dec, 2021
      - lat: 24.088938
        lng: 32.899829
        title: Aswan — Dec, 2021
      - lat: 27.257896
        lng: 33.811607
        title: Hurghada
      - lat: 27.96542
        lng: 34.361777
        title: Sharm El-Sheikh
      - lat: 31.354344
        lng: 27.237316
        title: Marsa Matruh
      - lat: 30.907371
        lng: 29.413579
        title: North Coast
      - lat: 29.593344
        lng: 32.717802
        title: Ras Sedr
      - lat: 28.560892
        lng: 33.947995
        title: Saint Catherine
      - lat: 28.509135
        lng: 34.513634
        title: Dahab
      - lat: 26.750017
        lng: 33.935976
        title: Safaga
      - lat: 30.860722
        lng: 31.010573
        title: Tanta
      - lat: 31.110659
        lng: 30.93878
        title: Kafr El-Shaikh
      - lat: 31.504319
        lng: 31.828163
        title: Ras El-Bar
      - lat: 31.265289
        lng: 32.301866
        title: Port Said
      - lat: 30.596492
        lng: 32.271459
        title: Ismailia
      - lat: 24.979162
        lng: 32.875801
        title: Edfu
      - lat: 41.276789
        lng: 28.730032
        title: Istanbul Airport — March 2023
      zoom: 2
    design:
      background:
        color: LightGrey

  #############################
  ######### Contact ###########
  #############################
  - block: contact-info
    id: contact
    content:
      title: Contact
      visit_title: Visit
      connect_title: Connect
      address:
        lines:
          - El-Khalifa El-Maamoun
          - El Weili, Cairo 4392001
          - Egypt
      email: mohamed.fakhry@gmail.com
      phone: "+20 10 5000 3412"
      office_hours:
        - "Please make an appointment via WhatsApp"
    design:
      background:
        color: Gainsboro

  #############################
  ########## Stats ############
  #############################
  - block: stats
    id: stats
    content:
      title: Impact
      items:
        - statistic: "2,899"
          description: Citations
          icon: hero/document-text
        - statistic: "21"
          description: h-index
          icon: hero/chart-bar
        - statistic: "26"
          description: i10-index
          icon: hero/chart-bar-square
        - statistic: "17"
          description: Scopus h-index
          icon: hero/academic-cap
    design:
      layout: cards
      background:
        color: LightGrey
        
---
