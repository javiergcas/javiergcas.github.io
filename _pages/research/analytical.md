---
layout: archive
title: "NeuroImaging Methods"
permalink: /research/analytical
excerpt: "Neuroimaging Analysis Methods Research Portfolio"
author_profile: true
toc: true
sidebar:
    nav: "sidebar_research"
---

{: .text-justify}
Functional neuroimaging data undergo multiple transformations from acquisition to interpretation. These transformations serve two main purposes: to remove noise and to facilitate interpretation. For example, fluctuations driven by neural activity account for only about 5% of the total signal. The remaining 95% consists of various sources of noise that must be addressed to prevent bias in results and interpretation — this is the “noise removal” part of the process.

{: .text-justify}
Even after noise has been mitigated, functional neuroimaging data remain challenging to interpret due to their high dimensionality (a single scan may include minutes-long recordings across tens of thousands of brain locations) and the many unknowns surrounding brain function. Additional transformations and statistical analyses are therefore applied to render the data interpretable. In practice, extracting meaningful information from neuroimaging data often requires tools from basic statistics, machine learning, and graph theory.

{: .text-justify}
As you will see below, over the years I have contributed to both aspects of the functional neuroimaging analysis pipeline. My work on denoising has focused primarily on multi-echo fMRI. In terms of interpretation, I have leaded multiple projects exploring dynamic (time-varying) functional connectivity and, on several occasions, delved into the world of dimensionality reduction using methods from machine learning (e.g., [t-SNE](https://en.wikipedia.org/wiki/T-distributed_stochastic_neighbor_embedding), [UMAP](https://umap-learn.readthedocs.io/en/latest/)) and topological data analysis (e.g., the [Mapper algorithm](https://tda-mapper.readthedocs.io/en/main/)).

{: .text-justify}
Please explore the sections below for more details.

{% include research_analysis.html %}

---

### Multi-Echo fMRI {#multi_echo}

{: .text-justify}
Functional MRI (fMRI) recordings capture not only fluctuations arising from localized neural activity but also from hardware instabilities, head motion, and physiological processes such as cardiac and respiratory cycles. As a result, fMRI practitioners dedicate considerable effort to isolating this informative component—both through improvements in acquisition protocols and the use of complex preprocessing pipelines. Multi-echo fMRI (ME-fMRI) represents a hybrid approach in which data are both acquired and processed differently.

{: .text-justify}
In essence, ME-fMRI leverages the fact that BOLD effects—those associated with localized neural activity—depend linearly on echo time (an acquisition parameter defining the interval between excitation and signal readout), whereas non-BOLD fluctuations (e.g., motion or scanner instabilities) do not. By acquiring data simultaneously at multiple echo times (rather than a single one, as is typically done), researchers can identify signal components that exhibit the expected linear dependence and regress out the rest. Although ME-fMRI has existed for decades, it gained widespread adoption only recently, following the introduction of [ME-ICA](https://www.sciencedirect.com/science/article/abs/pii/S1053811911014303) by the [Bandettini lab](https://fim.nimh.nih.gov/) (now implemented as [tedana](https://tedana.readthedocs.io/en/stable/)). ME-ICA combines echo-time–dependence analysis with [independent component analysis](https://en.wikipedia.org/wiki/Independent_component_analysis) to automatically remove non-BOLD fluctuations from fMRI data. While not perfect, tedana can markedly improve data quality, and many now view ME-fMRI as a key step toward enabling personalized mental healthcare interventions.

<img align="left" src="https://javiergcas.github.io/files/research/fmri_quality/me_deconvolution_small.png" width="600 px" style="padding: 10px">

{: .text-justify}
Although I contributed to the original study by [Kundu et al.](https://www.sciencedirect.com/science/article/abs/pii/S1053811911014303) describing the ME-ICA procedure, I have since become a fan of and an active contributor to the ME-fMRI community. My work includes leading a [project evaluating the original ME-ICA approach and demonstrating its superior performance when working with cardiac-gated fMRI data](https://www.sciencedirect.com/science/article/abs/pii/S1053811916303639), actively contributing to the [tedana project](https://joss.theoj.org/papers/10.21105/joss.03669) (for example, I co-authored the first version of the dynamic report page during a hackathon), and developing several iterations of a new [multi-echo–based deconvolution algorithm](https://www.sciencedirect.com/science/article/abs/pii/S105381191930669X) (see figure on the left). This last one in collaboration with my long-time collaborator [Dr. Caballero-Gaudes](https://www.bcbl.eu/en/conocenos/equipo/cesar-caballero-gaudes) at the [Basque Center for Brain, Cognition and Language](https://www.bcbl.eu). For more details regarding my contributions to ME-fMRI, please check the references below.

{: .text-justify}
If you’d like to learn more about ME-fMRI in general, I recommend this lecture linked below on the topic that I gave as part of an earlier version of the NIMH fMRI Summer Course.

<iframe width="560" height="315" src="https://www.youtube.com/embed/zkAmT92hLVw?si=_zZAT9OsRq6l-BvH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Selected Publications on Multi-Echo fMRI:**
* Gonzalez-Castillo J, et al. “[Evaluation of Multi-Echo ICA denoising for task based fMRI studies: block designs, rapid event-related designs, and cardiac-gated fMRI](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5026969/pdf/nihms810618.pdf)” NeuroImage (2016)
* Caballero-Gaudes C, Moia S, Panwar PA, Bandettini PA, Gonzalez-Castillo J. “[A deconvolution algorithm for multi-echo functional MRI: multi-echo sparse paradigm free mapping](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6819276/pdf/nihms-1538772.pdf)” NeuroImage (2019)
* DuPre et al. "[TE-dependent analysis of multi-echo fMRI with tedana](https://joss.theoj.org/papers/10.21105/joss.03669)" Journal of Open Source Software (2021)
* Caballero-Gaudes C, Bandettini PA, Gonzalez-Castillo J. "[A temporal deconvolution algorithm for multiecho functional MRI](https://ieeexplore.ieee.org/abstract/document/8363649)" IEEE 15th International Symposium on Biomedical Imaging (2018)
* Uruñuela E, Gonzalez-Castillo J et al. "[Whole-brain multivariate hemodynamic deconvolution algorithm for functional MRI with stability selection](https://www.sciencedirect.com/science/article/abs/pii/S1361841523002700)" Medical Imaging Analysis (2024)

### Time-varying Functional Connectivity {#tvFC}

* Comparing methods

* 

### Dimensionality Reduction {#dimensionality_reduction}

* Manifold Learning

* Topological Data Analysis




The majority of them are driven by two goals: removal of noise 
