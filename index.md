---
layout: splash
author_profile: true
#title: Welcome
#image: assets/images/distr9-2.png

permalink: /
#type: pages
title: "Welcome to my personal website!"

header:
  overlay_image: /assets/images/distr9.jpg

hidden: true

feature_row:
  - image_path: /assets/images/IMG_2294.jpeg
    alt: "About AI"
    title: "About AI"
    excerpt: " "
    url: "/about/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - image_path: /assets/images/IMG_2294.jpeg
    alt: "Astronomy"
    title: "Astronomy"
    excerpt: " "
    url: "/astronomy/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - image_path: /assets/images/IMG_2294.jpeg
    alt: "Blog"
    title: "Blog"
    excerpt: ""
    url: "/blog/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
---


<!-- To test site locally: bundle exec jekyll serve -->

<!-- <center> <h1>Welcome to my personal website!</h1> </center> -->


<div id="main" role="main">
  {% include sidebar.html %}

  <div class="archive">

    <!-- <h1 id="page-title" class="page__title">{{ page.title }}</h1> -->

  <!-- <div class="default" markdown="1">Have **fun!** -->
  
    <!-- {% include feature_row %} -->



    <h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "Recent Posts" }}</h3>

    {% if paginator %}
      {% assign posts = paginator.posts %}
    {% else %}
      {% assign posts = site.posts %}
    {% endif %}

    {% assign entries_layout = page.entries_layout | default: 'list' %}
    <div class="entries-{{ entries_layout }}">
      {% for post in posts %}
        {% include archive-single.html type=entries_layout %}
      {% endfor %}
    </div>

    {% include paginator.html %}


  
  </div>

</div> 



