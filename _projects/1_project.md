---
layout: page
title: krtexas
description: R package for nonparametric regression via tree-guided feature aggregation
img: assets/img/krtexas_logo.png
importance: 1
category: R packages
related_publications: true
---

**krtexas** (Kernel Regression with Tree-EXploring AggregationS) is an R package implementing nonparametric regression for predictors organized in a known hierarchical tree structure — for example, taxonomic trees, brain region hierarchies, or geographical hierarchies.

<div class="row align-items-center mt-3 mb-3">
    <div class="col-sm-2" style="max-width: 80px;">
        {% include figure.liquid loading="eager" path="assets/img/cornell_logo.png" 
        title="Cornell University" class="img-fluid rounded" %}
    </div>
    <div class="col-sm-9">
        <small>Developed at the <a href="https://stat.cornell.edu">Department of Statistics 
        and Data Science</a>, Cornell University, with 
        <a href="https://stat.cornell.edu/people/martin-t-wells">Martin T. Wells</a> 
        and <a href="https://stat.cornell.edu/people/y-samuel-wang">Y. Samuel Wang</a>.</small>
    </div>
</div>

The method, KR-TEXAS, simultaneously performs nonparametric regression and learns the correct level of feature aggregation, selecting relevant variables along the way {% cite manage2026nonparametric %}. It's built on a penalized Nadaraya–Watson estimator with adaptive weights, enabling joint model selection and aggregation in nonlinear settings.

This is motivated by applications like microbiome and genomic data analysis, where predictors naturally form a tree structure (e.g. species vs. genus level) and choosing a fixed resolution by hand sacrifices interpretability, statistical efficiency, or predictive performance. KR-TEXAS learns the optimal resolution directly from the data.

The package is co-authored with Y. Samuel Wang and Martin T. Wells, and accompanies the manuscript *Nonparametric Regression via Tree-Guided Feature Aggregation*.

<div class="row">
    <div class="col-sm-2" style="max-width: 80px;">
        {% include figure.liquid loading="eager" path="assets/img/krtexas_logo.png" title="krtexas logo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

You can install the package directly from GitHub:

```r
# install.packages("devtools")
devtools::install_github(
  "sithijamanage/krtexas",
  build_vignettes = TRUE
)
```

Source code, documentation, and a full vignette walkthrough are available on [GitHub](https://github.com/sithijamanage/krtexas).