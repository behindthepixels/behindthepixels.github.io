---
title: "Behind the Pixels"
layout: splash
permalink: /projects/
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/Header1.jpg
  caption: 'Rendered with EDXRay'
excerpt: 'Focus on Computer Graphics and Computer Vision.'
intro: 
  - excerpt: 'This page lists several interesting projects developed independently by Edward Liu.'
feature_row1:
  - image_path: /assets/images/edxray/San Miguel 2nd Fl.jpg
    title: "EDXRay"
    excerpt: 'A physically based renderer that features many state of the art algorithms in light transport simulation published in recent years.'
    url: "http://behindthepixels.info/EDXRay/"
    btn_label: "Learn More"
    btn_class: "btn--inverse"
feature_row2:
  - image_path: /assets/images/edxray/Splash .jpg
    title: "EDXFluids"
    excerpt: 'A fully featured fluid simulator. It implements several popular simulation algorithms like PIC/FLIP. Both liquid and smoke are supported.'
    url: "http://behindthepixels.info/EDXFluids/"
    btn_label: "Learn More"
    btn_class: "btn--inverse"
feature_row3:
  - image_path: /assets/images/edxray/edxraster.jpg
    title: "EDXRaster"
    excerpt: 'A highly optimized software renderer using rasterization. All the common stages in modern graphics pipeline are implemented with C++ and SSE.'
    url: "http://behindthepixels.info/EDXRaster/"
    btn_label: "Learn More"
    btn_class: "btn--inverse"
---

{% include feature_row id="intro" type="center" %}

{% include feature_row id="feature_row1" type="left" %}

{% include feature_row id="feature_row2" type="right" %}

{% include feature_row id="feature_row3" type="left" %}