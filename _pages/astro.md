---
title: "Astrophotography"
permalink: /astro # Need this if it's the home page in lieu of index.html
#classes: wide # needed? Nah, looks good as single col
date: 2023-12-02 # Says "updated on DATE" in footer
toc: true
# Define the gallery -- can this be done with liquid over all images in a subdir?
# Long term solution should be to find a more appropriate _include gallery that
# will expand and scroll dynamically so the page doesn't get too cluttered as
# I post more images
gallery:
  - url: /assets/images/astro/gallery/2023-07-29-Veil-21hr.jpg
    image_path: /assets/images/astro/gallery/2023-07-29-Veil-21hr.jpg
    title: Veil Nebula
  - url: /assets/images/astro/gallery/2023-07-11-Sadr-Region-200-mm.jpg
    image_path: /assets/images/astro/gallery/2023-07-11-Sadr-Region-200-mm.jpg
    title: Sadr Region
  - url: /assets/images/astro/gallery/2023-01-21-Pleiades-300-mm.jpg
    image_path: /assets/images/astro/gallery/2023-01-21-Pleiades-300-mm.jpg
    title: Pleiades
  - url: /assets/images/astro/gallery/2023-01-21-comet-2022-ZTF-50-mm.jpg
    image_path: /assets/images/astro/gallery/2023-01-21-comet-2022-ZTF-50-mm.jpg
    title: Comet 2022 ZTF
  - url: /assets/images/astro/gallery/2023-01-21-Barnards-Loop-50-mm.jpg
    image_path: /assets/images/astro/gallery/2023-01-21-Barnards-Loop-50-mm.jpg
    title: Barnard's Loop and Orion
  - url: /assets/images/astro/gallery/2022-11-18-Andromeda-250mm-f7.1-3.6hr.jpg
    image_path: /assets/images/astro/gallery/2022-11-18-Andromeda-250mm-f7.1-3.6hr.jpg
    title: Andromeda Galaxy
  - url: /assets/images/astro/gallery/2022-11-16-Heart-and-Soul-175mm-4hr.jpg
    image_path: /assets/images/astro/gallery/2022-11-16-Heart-and-Soul-175mm-4hr.jpg
    title: Heart and Soul Nebulae
  - url: /assets/images/astro/gallery/2022-11-12-Cygnus-Region-9.5hr-50-mm.jpg
    image_path: /assets/images/astro/gallery/2022-11-12-Cygnus-Region-9.5hr-50-mm.jpg
    title: Cygnus Region
  - url: /assets/images/astro/gallery/2022-07-02-Milky-Way.jpeg
    image_path: /assets/images/astro/gallery/2022-07-02-Milky-Way.jpeg
    title: Milky Way
  - url: /assets/images/astro/gallery/2022-07-02-M8-M20-Lagoon_and_Trifid-Nebulae-300-mm.jpeg
    image_path: /assets/images/astro/gallery/2022-07-02-M8-M20-Lagoon_and_Trifid-Nebulae-300-mm.jpeg
    title: Lagoon and Trifid Nebulae
---
<!-- Page title shows here, left aligned, defined in front matter -->
My photos of (mostly) outer space and some posts about technical stuff.

## Gallery
{: .text-left}
{% include gallery %}


## Astro Posts
{: .text-left}
{% include list-posts-in-category category = 'astro' %}
{: .text-left}
