---
layout: archive
title: "Experimental Desing and Acquisition Optimization"
permalink: /research/experimental
excerpt: "Neuroimaging Acquisition Methods Research Portfolio"
author_profile: true
toc: true
sidebar:
    nav: "sidebar_research"
---

{: .text-justify}
As an engineer entering the world of neuroscience, I initially struggled with the uncertainty and high levels of noise inherent in neuroscience research—particularly in <a href="https://en.wikipedia.org/wiki/Functional_magnetic_resonance_imaging">fucntional MRI</a> (fMRI). Early on, I decided to dedicate part of my time to better understanding the properties of the signals measured with <a href="https://en.wikipedia.org/wiki/Blood-oxygenation-level%E2%80%93dependent_imaging">BOLD fMRI</a>, studying their reliability, and optimizing scanning parameters. Some of these studies are highlighted below.

{% include research_acquisition.html %}



### Exploring the Quality of fMRI Data {#data_quality}

{: .text-justify}
One important aspect of scientific data is its reliability. That said, perfect test–retest reliability is neither expected nor necessarily desirable when studying a dynamic system like the human brain, which naturally changes from one measurement to the next. The real challenge lies in distinguishing genuine physiological variability from non-physiological noise and other confounding sources. Over the years, I have investigated the reliability of both task-based and [resting-state](https://en.wikipedia.org/wiki/Resting_state_fMRI) data across multiple projects—two of which are highlighted here.

<img align="right" src="/assets/pub_images/repro_2017.png" width="500 px" style="padding: 10px">

{: .text-justify}
When I joined the Talavage lab at [Purdue](http://www.puedue.edu), I was provided with a challenging dataset. After a year attempting to make sense of it, I realized that was not possible: the data was unreliable. This early struggle with <i>"bad"</i> data has motivated me to explore the reliability of fMRI in greater depth over the years.

{: .text-justify}
My first exploration of fMRI reproducibility is summarized in one of my PhD thesis publications. In that [study](https://www.sciencedirect.com/science/article/abs/pii/S105381191001284X), I evaluated the test–retest reliability of an auditory sentence comprehension task. This topic was of particular interest to my host lab, which investigated, among other things, the neural correlates of speech comprehension in cochlear implant users. Through this project, I was introduced to the field of [quality assurance](https://www.frontiersin.org/research-topics/33922/demonstrating-quality-control-qc-procedures-in-fmri/magazine), learned multiple methods for assessing test–retest reliability (e.g., [Dice coefficient](https://en.wikipedia.org/wiki/Dice-S%C3%B8rensen_coefficien), [intra-class correlation coefficient](https://en.wikipedia.org/wiki/Intraclass_correlation)), and gained deeper insight into one of fMRI’s main interpretational challenges: correctly identifying sources of individual differences that persist despite high group-level reproducibility. Our findings showed that the proposed task performed well at the group level, suggesting it could serve as a reliable protocol for future population-level studies.

<img align="left" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img01.png" width="400 px" style="padding: 10px">

{: .text-justify}
Another deep dive into reproducibility came from a study examining how patterns of [resting-state functional connectivity (rs-fMRI FC)](https://en.wikipedia.org/wiki/Intraclass_correlation) evolve during a one-hour scan. Unlike task-based fMRI, rs-fMRI scans require little from participants—simply to stay still, remain awake, and let their minds wander. This simplicity makes the approach ideal for clinical populations and easier to acquire than task-based data.

{: .text-justify}
By the time I entered this area, it was well established that rs-fMRI FC, averaged over several minutes, is reliable across sessions and carries meaningful phenotypic information (e.g., traits, symptoms). Yet, emerging evidence suggested these connectivity patterns fluctuate substantially within a single scan—raising a fundamental question: is this variability meaningful or merely noise?

{: .text-justify}
In this first exploration of time-varying FC, I focused on two key questions: (1) how scan duration affects the reliability of average connectivity estimates, and (2) whether the observed variability exhibits meaningful spatial structure. The first question is practical—fMRI is expensive, and participants can only remain still for so long—while the second probes whether the variability reflects genuine neural dynamics.

{: .text-justify}
Our results showed that reliability improves with scan length, with at least 10 minutes of data needed for stable estimates. We also identified distinct spatial patterns: the most stable connections were interhemispheric links between homologous regions, while the most variable involved cross-network, non-homologous connections in frontal and occipital cortex—regions supporting higher-order cognition.

**Publications on Data Quality and Reliability:**
* Gonzalez-Castillo J and Talavage TM “[Reproducibility of fMRI activations associated with auditory sentence comprehension](https://pmc.ncbi.nlm.nih.gov/articles/PMC3008333/pdf/nihms-244051.pdf)”. NeuroImage (2011)
* Gonzalez-Castillo J et al. “[The spatial structure of resting state connectivity stability on the scale of minutes](https://www.frontiersin.org/journals/neuroscience/articles/10.3389/fnins.2014.00138/full)”. Frontiers in Neuroscience (2014)
* Gonzalez-Castillo J et al. "[Variace decomposition for single-subject task-based fMRI activity estimates across many sessions](https://www.sciencedirect.com/science/article/pii/S105381191630578X)" NeuroImage (2017)
* Handwerker DA et al. "[The continuing challenge of understanding and modeling heodynamic variation in fMRI](https://www.sciencedirect.com/science/article/abs/pii/S1053811912001929)" NeuroImage (2012)
* Soltysik DA et al. "[Head-repositioning does not reduce the reproducibility of fMRI activation in a block-design motor task](https://www.sciencedirect.com/science/article/pii/S1053811911002849)" NeuroImage (2011)

### Multi-Echo fMRI {#multi_echo}

{: .text-justify}
Functional MRI (fMRI) recordings capture not only fluctuations arising from localized neural activity but also from hardware instabilities, head motion, and physiological processes such as cardiac and respiratory cycles. In fact, neural fluctuations account for only about 5% of the total signal variance. As a result, fMRI practitioners dedicate considerable effort to isolating this informative component—both through improvements in acquisition protocols and the use of complex preprocessing pipelines. Multi-echo fMRI (ME-fMRI) represents a hybrid approach in which data are both acquired and processed differently.

{: .text-justify}
In essence, ME-fMRI leverages the fact that BOLD effects—those associated with localized neural activity—depend linearly on echo time (an acquisition parameter defining the interval between excitation and signal readout), whereas non-BOLD fluctuations (e.g., motion or scanner instabilities) do not. By acquiring data simultaneously at multiple echo times (rather than a single one, as is typically done), researchers can identify signal components that exhibit the expected linear dependence and regress out the rest. Although ME-fMRI has existed for decades, it gained widespread adoption only recently, following the introduction of [ME-ICA](https://www.sciencedirect.com/science/article/abs/pii/S1053811911014303) by the [Bandettini lab](https://fim.nimh.nih.gov/) (now implemented as [tedana](https://tedana.readthedocs.io/en/stable/)). ME-ICA combines echo-time–dependence analysis with [independent component analysis](https://en.wikipedia.org/wiki/Independent_component_analysis) to automatically remove non-BOLD fluctuations from fMRI data. While not perfect, tedana can markedly improve data quality, and many now view ME-fMRI as a key step toward enabling personalized mental healthcare interventions.

<img align="left" src="https://javiergcas.github.io/files/research/fmri_quality/me_deconvolution_small.png" width="600 px" style="padding: 10px">

{: .text-justify}
Although I contributed to the original study by [Kundu et al.](https://www.sciencedirect.com/science/article/abs/pii/S1053811911014303) describing the ME-ICA procedure, I have since become a fan of and an active contributor to the ME-fMRI community. My work includes leading a [project evaluating the original ME-ICA approach and demonstrating its superior performance when working with cardiac-gated fMRI data](https://www.sciencedirect.com/science/article/abs/pii/S1053811916303639), actively contributing to the [tedana project](https://joss.theoj.org/papers/10.21105/joss.03669) (for example, I co-authored the first version of the dynamic report page during a hackathon), and developing several iterations of a new [multi-echo–based deconvolution algorithm](https://www.sciencedirect.com/science/article/abs/pii/S105381191930669X) (see figure on the left). This last one in collaboration with my long-time collaborator [Dr. Caballero-Gaudes](https://www.bcbl.eu/en/conocenos/equipo/cesar-caballero-gaudes) at the [Basque Center for Brain, Cognition and Language](https://www.bcbl.eu). For more details regarding my contributions to ME-fMRI, please check the references below.

{: .text-justify}
If you’d like to learn more about ME-fMRI in general, I recommend this lecture linked below on the topic that I gave as part of an earlier version of the NIMH fMRI Summer Course.

<iframe width="560" height="315" src="https://www.youtube.com/embed/zkAmT92hLVw?si=_zZAT9OsRq6l-BvH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Publications on Multi-Echo fMRI:**
* Gonzalez-Castillo J, et al. “[Evaluation of Multi-Echo ICA denoising for task based fMRI studies: block designs, rapid event-related designs, and cardiac-gated fMRI](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5026969/pdf/nihms810618.pdf)” NeuroImage (2016)
* Caballero-Gaudes C, Moia S, Panwar PA, Bandettini PA, Gonzalez-Castillo J. “[A deconvolution algorithm for multi-echo functional MRI: multi-echo sparse paradigm free mapping](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6819276/pdf/nihms-1538772.pdf)” NeuroImage (2019)
* DuPre et al. "[TE-dependent analysis of multi-echo fMRI with tedana](https://joss.theoj.org/papers/10.21105/joss.03669)" Journal of Open Source Software (2021)
* Caballero-Gaudes C, Bandettini PA, Gonzalez-Castillo J. "[A temporal deconvolution algorithm for multiecho functional MRI](https://ieeexplore.ieee.org/abstract/document/8363649)" IEEE 15th International Symposium on Biomedical Imaging (2018)
* Uruñuela E, Gonzalez-Castillo J et al. "[Whole-brain multivariate hemodynamic deconvolution algorithm for functional MRI with stability selection](https://www.sciencedirect.com/science/article/abs/pii/S1361841523002700)" Medical Imaging Analysis (2024)

### Optimization of Acquisition Parameters for fMRI {#optimization}

{: .text-justify}
Setting up an fMRI acquisition protocol involves making a large number of decisions. Some are fairly straightforward, such as selecting the scanner field strength and pulse sequence—often constrained by what is available at a given imaging center. The same applies to parameters tied directly to experimental design, such as temporal resolution, spatial resolution, and spatial coverage. However, many other parameters—those more closely related to the physics of MRI signal acquisition, such as echo time, flip angle, or bandwidth—are often treated as less critical and left at their “default” values. News alert: that assumption is not true. These parameters, though sometimes overlooked by non-physicists, can have a substantial impact on data quality.

{: .text-justify}
One particularly important parameter is the imaging [flip angle (FA)](https://mriquestions.com/what-is-flip-angle.html), which defines the amount of rotation (or “flip”) applied to the net magnetization vector by the radiofrequency pulse preceding signal readout. It is common practice to set the flip angle to the Ernst angle for gray matter, under the assumption that this choice maximizes sensitivity in that tissue compartment—typically the main focus of fMRI studies. Although this approach has its advantages, the Ernst angle is only truly optimal when data are dominated by thermal (non-physiological) noise. In our work, we developed a new theoretical model demonstrating that, under conditions where physiological noise dominates, the optimal flip angle can in fact be substantially lower without compromising sensitivity to neural activity.

<img align="center" src="https://javiergcas.github.io/files/research/fmri_quality/flip_angle_small.png" width="1100 px">

{: .text-justify}
The figure to the left [publication](https://www.sciencedirect.com/science/article/abs/pii/S1053811910014503) illustrates the main result from our empirical validation of the model. Even when reducing the flip angle to as low as 9° (compared to an Ernst angle of 77° for this scenario), the percent signal change and spatial profiles of neural activation in the visual and motor cortices remained stable. In other words, we were able to detect these regions of activity with equivalent sensitivity—despite reducing the flip angle by nearly an order of magnitude.



### Realtime fMRI {#realtime}

