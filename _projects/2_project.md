---
layout: page
title: permaBrioche
description: confounding-aware PERMANOVA and Hájek-based effect-size estimation for repeated-measures microbiome data
img: assets/img/permaBriocheLogo.png
importance: 2
category: R packages
giscus_comments: false
---

**permaBrioche** is a statistical framework for confounding-aware PERMANOVA and interpretable distance-based effect-size estimation in repeated-measures and other blocked study designs, developed as part of the BioBakery ecosystem at Harvard's Huttenhower Lab. It's particularly motivated by microbiome and other high-dimensional biological data, where subject-level clustering and longitudinal sampling are common.

<div class="row align-items-center mt-3 mb-3">
    <div class="col-sm-2" style="max-width: 80px;">
        {% include figure.liquid loading="eager" path="assets/img/thchan_logo.png" 
        title="BioBakery / Huttenhower Lab" class="img-fluid rounded" %}
    </div>
    <div class="col-sm-9">
        <small>Developed as part of the <a href="https://github.com/biobakery">BioBakery ecosystem</a> 
        at the <a href="https://huttenhower.sph.harvard.edu/">Huttenhower Lab</a>, 
        Department of Biostatistics, Harvard T.H. Chan School of Public Health.</small>
    </div>
</div>

permaBrioche addresses two well-known limitations of standard PERMANOVA: invalid permutation schemes under subject-level confounding (e.g. longitudinal designs), and upward bias and poor interpretability of the PERMANOVA $$R^2$$ effect size.

<div class="row">
    <div class="col-sm-2" style="max-width: 80px;">
        {% include figure.liquid loading="eager" path="assets/img/permaBriocheLogo.png" title="permaBrioche logo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The package implements design-aware permutation schemes for invariant and variant covariates, a null-centered $$R^2$$ for bias-corrected variance explanation, a Hájek-based distance effect size with direct geometric interpretation, and an optional location–dispersion decomposition in the Euclidean case.

In the Euclidean case, the Hájek effect decomposes as:

$$
\tau = \tau_{\text{location}} + \tau_{\text{dispersion}}
$$

where location captures mean (centroid) shift and dispersion captures change in within-group variability — distinguishing systematic shifts from increased heterogeneity.

You can install the package directly from GitHub:

```r
library(devtools)

devtools::install_github(
  "biobakery/permabrioche",
  build_vignettes = TRUE
)
```

Source code, full vignette walkthroughs, and documentation are available on [GitHub](https://github.com/biobakery/permaBrioche).