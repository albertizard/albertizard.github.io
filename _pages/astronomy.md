---
layout: single
author_profile: true
permalink: /astronomy/
defaults:
# _pages
- scope:
path: ""
type: pages
values:
header:
  overlay_image: /assets/images/distr9.jpg
title: "Astronomy"
excerpt: " "
show_overlay_excerpt: false
toc: false
#excerp: "Short summary"
#categories:
#  - sql
#  - python
#tags:
#  - sql
#  - python
#  - Poisson
#author_profile: true
---

If we take a look at the Universe at the largest scales (that is, when we zoom out a lot), we see that it's filled with galaxies. These have been evolving since they formed billions of years ago, with stars burning fuel and enriching galaxies with new elements product of their combustion (thank star dust for the calcium in your bones).

However, to understand galaxy formation we need to also understand dark matter and dark energy, the most dominant forms of energy in the Universe whose origin and properties are still a mystery. For over a decade, I researched dark matter and dark energy by means of numerical simulations, which is the equivalent of a laboratory for astrophysicists.

<!-- Simulated data sets are key to understand statistical errors and to mitigate systematic errors.  -->

## Simulating the Universe
<!-- The topic of approximate methods is a growing area in which alternative techniques are used to generate simulated catalogs instead of running computationally expensive full N-body simulations (the latter taking typically thousands of CPUs for many days). -->

Approximate methods allow running massive ensembles of simulations. In my PhD I developed ICE-COLA (Izard et al. [2016](https://ui.adsabs.harvard.edu/#abs/2016MNRAS.459.2327I/abstract){:target="_ blank"}, [2018](https://ui.adsabs.harvard.edu/#abs/2018MNRAS.473.3051I/abstract){:target="_ blank"}), a tool for producing fast cosmological simulation with some unique capabilities.

ICE-COLA is a parallel code for fast cosmological simulations, that reduces both the CPU-time and the storage requirements by 2-3 orders of magnitude with respect to traditional methods based on full N-body simulations and semi-analytic methods. It has the advantage of producing at run time catalogs in the light cone format directly, in which distant objects are seen as they were in the past, and in this way a huge compression factor in the data volume is achieved.

I demonstrated that an approximate method can reach enough accuracy to simulate weak gravitational lensing experiments, enabling multi-probe analysis of galaxy clustering and weak gravitational lensing.

---
<center>
<img src="/assets/images/icecola_wl.jpeg" width="600" height="500">
</center>
<p class="caption">
     Map of the large-scale structure of the Universe as predicted in an ICE-COLA simulation. An observer located in the bottom receives the light that has traveled through the matter distribution. The massive objects that photons encountered in their path deflect their trajectories and create the distortion pattern depicted by the white arrows. This phenomenon is called weak gravitational lensing and is sensitive directly to the total mass (baryonic and dark matter), therefore giving a very unique way to weigh the Universe.
</p>
---

I also developed a pipeline to pin galaxies into simulated dark matter distributions. All these tools together constitute a very efficient methodology to connect fundamental theory to observations and thereby to sample very large cosmological volumes and explore model parameters. The final product are mock galaxy catalogs, very valuable in the preparation of upcoming galaxy surveys.

In my most ambitious simulation effort I generated 500 ICE-COLA simulations covering very large volumes. I used them to develop an analytical model for the observational systematics caused by galaxy neighbors (one example of this being the effect called blending). Mitigating such systematics is imperative for the next generation of experiments that will have high number densities, such as the projects that I have been involved in: the [Euclid](https://www.euclid-ec.org){:target="_ blank"} space mission, the [Nancy Grace Roman Space Telescope](https://roman.gsfc.nasa.gov/){:target="_ blank"}, and the [Vera C. Rubin Observatory](https://www.lsst.org){:target="_ blank"}. This large data set of 500 ICE-COLA simulations has also been used to model the observations of the [Dark Energy Survey](https://www.darkenergysurvey.org/) [in this paper](https://ui.adsabs.harvard.edu/abs/2021arXiv210704602F/abstract).


## How I did it

In my research I developed end-to-end data pipelines for simulated data, starting from developing new simulation codes in C/C++ and MPI (Message Passing Interface), running the simulations in high-performance computing environments (distributed computing clusters), storing and transforming Terabytes of data, to finally analysing and modeling the data using advanced statistical and machine learning methods.

<!-- My simulations served to prepare for future cosmological experiments, that are currently producing the most accurate maps of the large-scale structure of the Universe (such as the [Dark Energy Survey](https://www.darkenergysurvey.org/) and [Euclid](https://www.esa.int/Science_Exploration/Space_Science/Euclid)). The ultimate goal of these missions is to better understand the properties of the elusive dark matter and dark energy components of the Universe. -->

## My interest in astronomy
* N-body simulations
* Approximate methods for the generation of simulated galaxy catalogs
* The large-scale structure of the Universe
* Modified gravity theories
* Weak-gravitational lensing
* Galaxy clustering
* Covariance matrices
* Observational systematics in galaxy surveys
* Numerical methods
