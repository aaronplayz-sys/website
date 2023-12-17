---
layout: post
title: How To Dual Boot Windows
date: 2023-12-16
description: A guide on boot Windows and your choice of Linux Distro.
tags: Linux, Windows, how-to
categories: posts
toc:
  sidebar: left
---

## Assumptions

Before we get started, there are a few things that I assume you have on hand, have the knowledge of and are comfortable doing.

- Know the layout of your UEFI/BIOS menu
- Boot override
- A dedicated drive to install your choice of Linux distribution

## Downloading the ISO

First, you want to navigate to your choice of Linux distribution website and save the `ISO file` somewhere you can `easily find` it. For this guide, I am going to use Nobara Linux as an example.

{% include figure.html path="assets/img/how-to-dual-boot-windows/nobara-homepage.png" class="img-fluid rounded z-depth-1" zoomable=true %}
<div class="caption">
  Nobara homepage
</div>

{% include figure.html path="assets/img/how-to-dual-boot-windows/nobara-downloads.png" class="img-fluid rounded z-depth-1" zoomable=true %}
<div class="caption">
  Nobara's downloads page
</div>

## Flashing the ISO to thumb drive

To keep it simple, we are going to use balena etcher to write our image (the ISO file) to our thumb drive aka USB stick.

Go to [https://etcher.balena.io/](https://etcher.balena.io/) and download the installer, then open the file and install the application as normal, accept all defaults.

{% include figure.html path="assets/img/how-to-dual-boot-windows/balena-etcher-download-page.png" class="img-fluid rounded z-depth-1" zoomable=true %}
<div class="caption">
  balena etcher's download section
</div>

After installing balena etcher, go ahead and insert your thumb drive into your computer, then open the app if it is not yet open already.

{% include figure.html path="assets/img/how-to-dual-boot-windows/balena-etcher.png" class="img-fluid rounded z-depth-1" zoomable=true %}
<div class="caption">
  The application should look like this when open
</div>

Click on "Flash from file" button and locate your downloaded ISO file and click open.

<div class="row mt-3"> 
  <div class="col-sm mt-3 mt-md-0"> 
    {% include figure.html path="assets/img/how-to-dual-boot-windows/flash-from-file.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
  <div class="col-sm mt-3 mt-md-0"> 
    {% include figure.html path="assets/img/how-to-dual-boot-windows/select-file.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
  <div class="col-sm mt-3 mt-md-0"> 
    {% include figure.html path="assets/img/how-to-dual-boot-windows/selected-file.png" class="img-fluid rounded z-depth-1" zoomable=true %}
  </div>
</div>
<div class="caption"> 
  Screenshot's for reference
</div>