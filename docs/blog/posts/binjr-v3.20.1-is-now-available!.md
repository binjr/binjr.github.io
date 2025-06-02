---
draft: false
date:
  created: 2024-11-10
  updated: 2024-11-10
image: assets/images/binjr_card.png
tags:
  - News
  - Releases
  - v3.20.1
authors:
  - binjr
categories:
  - binjr
  - New releases
comments: true
---
# [binjr v3.20.1](https://github.com/binjr/binjr/releases/tag/v3.20.1) is now available! 🎉
Released on Sun, 10 Nov 2024

> This is an interim release which fixes a regression introduced in v3.20.0 that severely impacts the peformances of the CSV and Log files adapters.

<!-- more -->

### What's new?
* _[Dependencies]_ Rolled back embedded OpenJDK runtime to 21.0.5
* _[Fixed]_ Bad performances when using the CSV and Logs adapters caused by a regression in OpenJDK 23.0.1 when using Shenandoah GC.
* _[Fixed]_ An error is raised in the installer when clicking on the 'back' button on the install verification dialog.

### Links
* [Download]( https://binjr.eu/download/latest_release/)
* [Getting starting](https://binjr.eu/documentation/getting-started/)
* [Report an issue](https://github.com/binjr/binjr/issues)
