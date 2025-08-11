---
date:
  created: 2025-08-11
  updated: 2025-08-11
draft: false
image: assets/images/SisyphusCI.png
tags:
  - aarch64
  - macOS
authors:
  - fthevenet
categories:
  - binjr
  - news
comments: true
---

# ARM64 builds for macOS and Linux are (finally) coming!



At long last, native binjr application bundles for machines with ARM64 CPUs are coming! 

This will be welcome news mostly to mac users, as all new macBooks have come equipped with Apple silicon CPUs for a quite a while now.  
ARM64 builds for Linux are also coming, by the way, but Windows users will have to wait a little more, unfortunately. While everything is in place on our end and aarch64 OpenJDK builds for Windows are available right now, that is sadly not yet the case for JavaFX, binjr's only other arch-specific dependency.

And if you're running Intel or AMD based machines, don't worry: x86_64 builds are not going anywhere for now.

<!-- more -->

I know it's been a long time coming, and as a matter of fact, it has been possible for users to build from source and run binjr on ARM-based macOS and Linux themselves [for over three years now!](https://github.com/orgs/binjr/discussions/116)  
So why has it taken so long for us to add prebuilt binaries to our download page? Quite simply, because of the lack of option for [ARM-based runners on Azure Pipelines](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/hosted), the Continuous Integration platform that binjr's uses to produce the binary builds for download. While GitHub had been offering macOS and Linux aarch64 runners for FOSS projects for a while, and since both platforms are owned by Microsoft, I thought it reasonable to hope that the Azure CI would start doing the same sooner or later. Well... It's now been years and given that there are no signs things are about to change any time soon, I have finally decided to bite the bullet and migrate the build logic from Azure Pipelines to GitHub Actions.

This is not the first time I have done something like that, far from it. Originally, there weren't any one single CI platform that provided  hosted builder VMs for all three OSes that binjr targets—even without factoring different CPU architectures into the equation. So I had to write the complex build and release logic a first time for [Travis](https://www.travis-ci.com/), that took care of Linux and macOS builds, and a second time for [AppVeyor](https://www.appveyor.com/), to make Windows binaries. And then somehow orchestrate both to be triggered from a single GitHub release...

The fundamental concepts were rigorously the same between Travis and AppVeyor, and their APIs and configuration syntax had **a lot** in common, so you'd be forgiven to think that once you had one working, getting the other up and running would be a piece of cake.  
Well, as usual the Devil's in the details and it's the slight differences amongst the mass of identical things that made this particular task such a slog. The choice of YAML as a vessel for their configuration DSL (or lack thereof, rather) made this all the more painful, with it's inherent lack of discoverability, wonky validation tooling and frankly baffling syntax idiosyncrasies. But I eventually got all that working reasonably well, and moved on.

A few years down the line, well before GitHub Actions even existed, Microsoft started Azure Pipelines, which offered the ability to run on all three OSes (Windows, mac and Linux) from a single set of build jobs, at no cost for FOSS projects. This sounded like the perfect opportunity to get rid of the quirks induced by having to carefully orchestrate two completely separate build platforms to create a single release. Sure, having to rewrite all that YAML was going to suck, but _"hey"_, I thought to myself, _"this one finally does everything I need, so at least it'll be the last time I have to deal with any of that!"_. Famous last words... and very dumb ones at that.

Anyway, five years on and here we are again. I have written yet another True Final Form for that damn build code.The last one! Until next time, at least.

![SisyphusCI](https://binjr.eu/assets/images/SisyphusCI.png)
