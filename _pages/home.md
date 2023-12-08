---
title: "Eric Driscoll, PhD"
permalink: / # Need this if it's the home page in lieu of index.html
#layout: single # Not needed, covered by defaults for pages

classes: wide # each project element looks better this way, and the long word "astrophotography" is less likely to be truncated
toc: false

author_profile: true
#date: 2016-03-23T11:48:41-04:00 # Says "updated on DATE" in footer
# https://mmistakes.github.io/minimal-mistakes/docs/layouts/#headers
header:
  overlay_color: "#000"
  overlay_filter: "0.6"
  # boosted saturation, and scaled down by factor of 0.5
  overlay_image: /assets/images/banner/b1-sat-0.5.jpg
  #overlay_image: /assets/images/unsplash-image-1.jpg

  # makes buttons on the banner
  # actions:
  #   - label: "Download"
  #     url: "https://github.com/mmistakes/minimal-mistakes/"
  #   - label: "Learn More"
  #     url: "https://github.com/mmistakes/minimal-mistakes/"
  #   - label: "Another Button"
  #     url: "https://github.com/mmistakes/minimal-mistakes/"
  #caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "Welcome! These are some ongoing projects and activities that I spend my time on."


feature_row:
  - image_path: /assets/images/astro/gallery/2023-07-11-Sadr-Region-200-mm-thumb.jpg
    title: "Astrophotography"
    excerpt: "A collection of my images and some technical info on the process."
    url: "/astro"
    btn_label: "View"
    btn_class: "btn--primary"

  - image_path: assets/images/synth/synth_saw_scope-thumb.jpg
    title: "Modular Synthesis"
    url: "/synth"
    btn_label: "View"
    btn_class: "btn--primary"
    excerpt: "Turning electricity into music with analog(ish) circuits."

  - image_path: /assets/images/mycology/pink_PXL_20210417_155058451-thumb.jpg
    title: "Mycology"
    excerpt: "Forays into farming and finding fungi."
    url: "/mycology"
    btn_label: "View"
    btn_class: "btn--primary"

  - image_path: /assets/images/games/unity-ml-agents-donut-collector/ml-agents-01-thumb.png
    title: "Game Development"
    excerpt: "Video games I've created with Unity in C#."
    url: "/games"
    btn_label: "View"
    btn_class: "btn--primary"

  - image_path: assets/images/backpacking/yosemite-2023/PXL_20230904_230827011-thumb.jpg
    title: "Backpacking"
    excerpt: "Photographs from a three day trip in the Yosemite wilderness area."
    url: "/backpacking"
    btn_label: "View"
    btn_class: "btn--primary"
---

<!-- <h1><p style="text-align:center">Projects</p></h1> -->
<!-- All features in one row -->
# Projects

{% include feature_row %}

# Academic Publications
{% include_relative publication-list.md %}
