---
title: "Eric Driscoll, PhD"
permalink: / # Need this if it's the home page in lieu of index.html
#layout: single # Not needed, covered by defaults for pages
classes: wide # each project element looks better this way, and the long work "astrophotography" is less likely to be truncated
author_profile: true
#date: 2016-03-23T11:48:41-04:00 # Says "updated on DATE" in footer
# https://mmistakes.github.io/minimal-mistakes/docs/layouts/#headers
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/unsplash-image-1.jpg
  # makes buttons on the banner
  # actions:
  #   - label: "Download"
  #     url: "https://github.com/mmistakes/minimal-mistakes/"
  #   - label: "Learn More"
  #     url: "https://github.com/mmistakes/minimal-mistakes/"
  #   - label: "Another Button"
  #     url: "https://github.com/mmistakes/minimal-mistakes/"
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
excerpt: "Welcome! These are some ongoing projects and activities that I spend my time on."


feature_row:
  - image_path: /assets/images/astro/gallery/2023-07-11-Sadr-Region-200-mm-thumb.jpg
    alt: ""
    title: "Astrophotography"
    excerpt: "A collection of my images and some technical info on the process."
    url: "/astro"
    btn_label: "View"
    btn_class: "btn--primary"

  - image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: ""
    title: "Modular Synthesis"
    url: "/synth"
    btn_label: "View"
    btn_class: "btn--primary"
    excerpt: "Building devices that turn electricity into sound."

  - image_path: /assets/images/unsplash-gallery-image-3-th.jpg
    title: "Mycology"
    excerpt: "Forays into farming and finding fungi."
    url: "/mycology"
    btn_label: "View"
    btn_class: "btn--primary"

  - image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: ""
    title: "Game Development"
    excerpt: "Progress in learning how to make video games with Unity in C#."
    url: "/games"
    btn_label: "View"
    btn_class: "btn--primary"

  - image_path: assets/images/unsplash-gallery-image-1-th.jpg
    alt: ""
    title: "Backpacking"
    excerpt: "Photographs from a three day trip in the Yosemite wilderness area."
    url: "/backpacking"
    btn_label: "View"
    btn_class: "btn--primary"
---

<!-- <h1><p style="text-align:center">Projects</p></h1> -->
<!-- All features in one row -->
{% include feature_row %}

