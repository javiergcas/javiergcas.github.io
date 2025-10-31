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
I have contributed to both aspects of the functional neuroimaging analysis pipeline. My work on denoising has focused primarily on multi-echo fMRI. In terms of interpretation, I have leaded projects exploring dynamic (time-varying) functional connectivity and, on several occasions, delved into the world of dimensionality reduction using methods from machine learning (e.g., [t-SNE](https://en.wikipedia.org/wiki/T-distributed_stochastic_neighbor_embedding), [UMAP](https://umap-learn.readthedocs.io/en/latest/)) and topological data analysis (e.g., the [Mapper algorithm](https://tda-mapper.readthedocs.io/en/main/)).

{: .text-justify}
Please explore the sections below for more details.

{% include research_analysis.html %}

---

### <img src="/assets/icons/multi-echo_icon.png" width="32" height="32" alt="Icon"> Multi-Echo fMRI {#multi_echo}

{: .text-justify}
Functional MRI (fMRI) recordings capture not only fluctuations arising from localized neural activity but also from hardware instabilities, head motion, and physiological processes such as cardiac and respiratory cycles. As a result, fMRI practitioners dedicate considerable effort to isolating this informative component—both through improvements in acquisition protocols and the use of complex preprocessing pipelines. Multi-echo fMRI (ME-fMRI) represents a hybrid approach in which data are both acquired and processed differently.

{: .text-justify}
In essence, ME-fMRI leverages the fact that BOLD effects—those associated with localized neural activity—depend linearly on echo time (an acquisition parameter defining the interval between excitation and signal readout), whereas non-BOLD fluctuations (e.g., motion or scanner instabilities) do not. By acquiring data simultaneously at multiple echo times (rather than a single one, as is typically done), researchers can identify signal components that exhibit the expected linear dependence and regress out the rest. Although ME-fMRI has existed for decades, it gained widespread adoption only recently, following the introduction of [ME-ICA](https://www.sciencedirect.com/science/article/abs/pii/S1053811911014303) by the [Bandettini lab](https://fim.nimh.nih.gov/) (now implemented as [tedana](https://tedana.readthedocs.io/en/stable/)). ME-ICA combines echo-time–dependence analysis with [independent component analysis](https://en.wikipedia.org/wiki/Independent_component_analysis) to automatically remove non-BOLD fluctuations from fMRI data. While not perfect, tedana can markedly improve data quality, and many now view ME-fMRI as a key step toward enabling personalized mental healthcare interventions.

<a href="https://www.sciencedirect.com/science/article/abs/pii/S105381191930669X"><img align="left" src="https://javiergcas.github.io/files/research/fmri_quality/me_deconvolution_small.png" width="600 px" style="padding: 10px"></a>

{: .text-justify}
I have been an avid contributor to the ME-fMRI community since 2016. My work in ME-fMRI includes an [early evaluation of the original ME-ICA approach](https://www.sciencedirect.com/science/article/abs/pii/S1053811916303639), contributions to the [tedana project](https://joss.theoj.org/papers/10.21105/joss.03669) (for example, I co-authored the first version of the dynamic report page during a hackathon), and devising, implementing and testing several iterations of a [multi-echo–based deconvolution algorithm](https://www.sciencedirect.com/science/article/abs/pii/S105381191930669X) (see figure on the left). This last one in collaboration with my long-time friend [Dr. Caballero-Gaudes](https://www.bcbl.eu/en/conocenos/equipo/cesar-caballero-gaudes) at the [Basque Center for Brain, Cognition and Language](https://www.bcbl.eu). For more details regarding my contributions to ME-fMRI, please check the references below.

{: .text-justify}
If you’d like to learn more about ME-fMRI in general, I recommend this lecture linked below on the topic that I gave as part of an earlier version of the NIMH fMRI Summer Course.

<iframe width="560" height="315" src="https://www.youtube.com/embed/zkAmT92hLVw?si=_zZAT9OsRq6l-BvH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Selected Publications on Multi-Echo fMRI:**
* Gonzalez-Castillo J, et al. “[Evaluation of Multi-Echo ICA denoising for task based fMRI studies: block designs, rapid event-related designs, and cardiac-gated fMRI](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5026969/pdf/nihms810618.pdf)” NeuroImage (2016)
* Caballero-Gaudes C, Moia S, Panwar PA, Bandettini PA, Gonzalez-Castillo J. “[A deconvolution algorithm for multi-echo functional MRI: multi-echo sparse paradigm free mapping](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6819276/pdf/nihms-1538772.pdf)” NeuroImage (2019)
* DuPre et al. "[TE-dependent analysis of multi-echo fMRI with tedana](https://joss.theoj.org/papers/10.21105/joss.03669)" Journal of Open Source Software (2021)
* Caballero-Gaudes C, Bandettini PA, Gonzalez-Castillo J. "[A temporal deconvolution algorithm for multiecho functional MRI](https://ieeexplore.ieee.org/abstract/document/8363649)" IEEE 15th International Symposium on Biomedical Imaging (2018)
* Uruñuela E, Gonzalez-Castillo J et al. "[Whole-brain multivariate hemodynamic deconvolution algorithm for functional MRI with stability selection](https://www.sciencedirect.com/science/article/abs/pii/S1361841523002700)" Medical Imaging Analysis (2024)

### <img src="/assets/icons/tvfc.png" width="32" height="32" alt="Icon"> Time-varying Functional Connectivity {#tvFC}

{: .text-justify}
What do neuroscientists mean when they talk about [dynamic or time-varying functional connectivity](https://www.sciencedirect.com/science/article/pii/S105381191300579X)? There’s quite a bit to unpack, and I am going to try my best to do so in a few paragraphs. That said, if you have the time and the interest, please check [this talk](https://youtu.be/zr-OSdlU7nY?si=JaCF1yKc2jgWUDvd) before you keep going. It will all make much more sense after that!

<img align="center" src="/files/research/tvfc/static_vs_tvfc.png" width="1100 px">

{: .text-justify}
Let’s start with functional connectivity (FC) itself. The term refers to the observation that groups of spatially non-contiguous brain regions—often referred to as [brain networks](https://en.wikipedia.org/wiki/Large-scale_brain_network)—exhibit higher temporal synchrony with each other than with the rest of the brain. FC between two regions is typically measured using the [Pearson's Correlation](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient) between their respective time series. When this calculation is extended to hundreds of regions spanning the cortex (e.g., those defined by an atlas or parcellation), the result is a matrix of pairwise correlations known as a functional [connectome](https://en.wikipedia.org/wiki/Connectome).

<a href="https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full"><img align="right" src="/files/research/tvfc/tvfc_breakdown.png" width="500 px" style="padding: 10px"></a>

{: .text-justify}
A key point here is that these inter-regional correlations are computed using the entire duration of the scan. This makes sense—assuming the system is in a steady state, more data points yield more reliable correlation estimates.

{: .text-justify}
But what if the system isn’t stationary? Is that “average” view of inter-regional relationships the whole story, or could additional insight be gained by examining how these connections fluctuate from second to second and minute to minute during a scan? While the static connectome has proven highly informative (as evidenced by thousands of studies), there may also be valuable information in these short-term, transient reconfigurations of brain connectivity. Understanding the meaning and potential clinical relevance of such time-varying functional connectivity remains an active and evolving area of research; one to which I have devoted many efforts.

{: .text-justify}
In the early days, my work—like that of many others—focused on establishing the most basic aspects of dynamic functional connectivity (FC). In one of my first studies, we examined the spatial profile of FC dynamicity using hour-long resting-state scans (see more details [here](experimental#tvfc_reliability)). Once we confirmed that FC fluctuations were spatially organized rather than random, I turned my attention to their potential cognitive correlates.

<a href="https://www.pnas.org/doi/abs/10.1073/pnas.1501242112"><img align="left" src="/files/research/tvfc/tvfc_pnas_setup.png" width="500 px" style="padding: 10px"></a>

{: .text-justify}
If dynamic reconfiguration of FC relates to cognition, then engaging in different mental activities should lead to corresponding changes in FC patterns. I demonstrated this in our 2015 [PNAS publication](https://www.pnas.org/doi/abs/10.1073/pnas.1501242112), where participants were asked to mentally switch among four distinct mental activities while being continuously scanned during both engagement and transitions between them. The results confirmed that cognitive state changes indeed induce FC reconfigurations.

{: .text-justify}
A key question, however, remained: what about the spontaneous reconfigurations observed during rest? Could these also reflect self-generated shifts in mental processes—the very essence of mind-wandering? I have devoted, and continue to devote, much of my work to exploring this fundamental question, which may hold clues to how the brain supports conscious experience. That inquiry belongs more squarely within the realm of cognitive neuroscience, so if you’re interested, you can read more about it [here](research/cogneuro#rest_matters).

{: .text-justify}
Alright, back to methods—since that’s the focus of this page. Let me highlight one purely methodological study I’ve conducted on time-varying FC. The first is a method comparison study led by my former mentee, [Dr. Hua (Oliver) Xie](https://scholar.google.com/citations?user=j5xPZdAAAAAJ&hl=en), who was interested in identifying the most effective way to detect and characterize dynamic FC. This was no small task. Once the scientific community embraced the idea that time-varying FC might hold meaningful information, a proliferation of analytical methods emerged—ranging from various flavors of sliding-window correlation and dynamic conditional correlation (DCC) to multiplication of temporal derivatives and jackknife correlation, among others.

<a href="https://www.sciencedirect.com/science/article/pii/S1053811918321815"><img align="right" src="https://javiergcas.github.io/files/research/tvfc/tvfc_methods_comp.jpg" width="500 px" style="padding: 10px"></a>

{: .text-justify}
Oliver and I set out to compare seven of the most widely used methods for estimating time-varying FC (see figure on the right). We evaluated both their mathematical similarities and differences, as well as their practical performance in detecting FC reconfigurations linked to ongoing cognitive dynamics. For the latter, we relied on clustering analyses and evaluation metrics drawn from [unsupervised machine learning](https://www.ibm.com/think/topics/unsupervised-learning).

{: .text-justify}
Our results, reported [here](https://www.sciencedirect.com/science/article/pii/S1053811918321815), showed that all window-based methods performed well for commonly used window lengths (WL ≥ 30 s), with the sliding-window methods (with and without normalization) and the hybrid dynamic conditional correlation with moving average (DCC_MA) approach performing slightly better. For shorter windows (WL ≤ 15 s), DCC_MA and jackknife correlation yielded the most robust results. These findings have since helped researchers make more informed choices about how best to characterize time-varying FC in their own studies.

**Selected Publications on time-varying FC (methods-heavy):**

* Xie H et al. "[Efficacy of different dynamic functional connectivity methods to capture cognitively relevant information](https://www.sciencedirect.com/science/article/pii/S1053811918321815)" NeuroImage (2019)

* Hutchinson et al. "[Dynamic functional connectivity: promise, issues, and interpretations](https://www.sciencedirect.com/science/article/pii/S105381191300579X)" NeuroImage (2013)

* Gonzalez-Castillo J & Bandettini PA. "[Task-based dynamic functional connectivity: Recent findings and open questions]()" NeuroImage (2018)

* Xie et al. "[Whole-brain connectiity dynamics reflect both task-specific and individual-specific modulation: a multitask study](https://www.sciencedirect.com/science/article/pii/S1053811917304494)" NeuroImage (2018)

### <img src="/assets/icons/dimensionality_reduction_icon.png" width="32" height="32" alt="Icon"> Dimensionality Reduction {#dimensionality_reduction}

{: .text-justify}
Humans are remarkably good at spotting patterns in up to three dimensions—perhaps a few more with the right tools. Think of color-coded movies of 3D scatter plots to visualize 5D data, [radar charts](https://en.wikipedia.org/wiki/Radar_chart) and [parallel coordinates](https://en.wikipedia.org/wiki/Parallel_coordinates) to represent a handful of additional dimensions. But what happens when our data lives in 10,000+ dimensions, as in functional neuroimaging? Those tools fail unless we first project the data into a lower-dimensional space that preserves its essential structure.

{: .text-justify}
Take a concrete example from fMRI research. Suppose we record a 25-minute scan and parcellate the brain into 200 regions. To study how functional connectivity evolves over time, we can use a sliding-window correlation approach (see figure above). The resulting matrix has ~900 time points on the X-axis and 19,900 connections on the Y-axis—essentially, the evolution of data in a 19,000-dimensional space. Can you make sense of that directly? Probably not. But when we embed those data into three dimensions, each dot now represents the connectivity pattern of a given time window, and clear structure emerges—four dominant configurations that recur at distinct times during the scan.

{: .text-justify}
This example illustrates how high-dimensional data can be mapped into 2D or 3D while retaining meaningful information. Different dimensionality-reduction methods, however, make different assumptions. In a recent study, I compared three state-of-the-art nonlinear methods—[t-SNE](), [UMAP](), and [Laplacian Eigenmaps]()—to evaluate how well they preserve information about subject identity and cognitive load in functional connectivity data. We found that all can work, but success depends critically on hyperparameter tuning. Importantly, heuristics from other fields do not necessarily apply here, underscoring the need for domain-specific exploration. Because many neuroimagers are new to these methods, the first part of our paper serves as a tutorial introduction. Check it out if you want to learn more on this topic!
tions occured at two different instants of the scan. Want to know all the details, check this publication.

{: .text-justify}
Another powerful approach to dimensionality reduction comes from Topological Data Analysis (TDA), particularly through the Mapper algorithm. I explored this method in collaboration with Dr. Manish Saggar from Stanford University, applying it to a multi-task fMRI dataset I had previously collected to study the cognitive relevance of time-varying functional connectivity. Unlike traditional sliding-window analyses, which collapse data over windows of ~30 seconds, TDA allowed us to capture the large-scale organization of whole-brain activity at the single-participant level without imposing arbitrary spatial or temporal averaging. The resulting low-dimensional representations (see example below) revealed both within- and between-task transitions at much finer time scales (~4–9 s). Moreover, individual differences in these dynamic trajectories predicted task performance.

{: .text-justify}
These projects exemplify how I integrate advanced machine-learning approaches into neuroscience research. For more application-driven work using these and related methods, visit the section on neural correlates of conscious perception in Cognitive Neuroscience Research.


{: .text-justify}
Another approach for dimensionality reduction comes from the world of Topological Data Analysis where a powerful algorithm called Mapper was developed for this purpose. I had the opportunity to learn more about this fascinating method in a collaboration with Dr. Manish Saggar from Stanford Unviersity.

{: .text-justify}
These are two examples of how I integrate the latest advances in machine learning into my research. For more application-based work that relies on these and other methods, make sure to check some of my newest work on the neural correlates of conscious perception in the Cognitive Neuroscience Research section. 