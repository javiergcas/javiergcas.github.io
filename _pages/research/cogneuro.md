---
layout: archive
title: "Cognitive Neuroscience"
permalink: /research/cogneuro
excerpt: "Cognitive Neuroscience Research Portfolio"
author_profile: true
toc: true
sidebar:
    nav: "sidebar_research"
---

Methods are fun, but they are more fun and become useful when they allow you to answer some unkownn, in this case some unkown about the brain. In this section you will find a brief discussion of three cognitive neuroscience questions of great interest to me: 

{% include research_cogneuro.html %}

***

<a id="biological-processes"></a>
### Behavioral Processes behind Time-varying Functional Connectivity

<a href="https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full"><img align="right" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img01.png" width="317 px" style="padding: 10px"></a>

{: .text-justify}
[Functional connectivity](https://en.wikipedia.org/wiki/Resting_state_fMRI#Functional), as measured with [BOLD](https://en.wikipedia.org/wiki/Blood-oxygen-level-dependent_imaging) fMRI, exhibits dynamic behavior at the scale of seconds, with rich spatiotemporal structure both during [resting state]((https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full)) and [task](https://www.sciencedirect.com/science/article/abs/pii/S1053811917306535) scans. What does such dynamicity reflects? To what extent do aberrant patterns of time-varying functional connectivity signal pathology? These remain open questions. In early studies (discussed in greater detail in the [Acquisition](experimental#tvfc_reliability section, we [characterized the spatiotemporal structure of these dynamics during rest](https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full). Once we established that non-random structure predominated, we turned to examine how such dynamics relate to cognition.

<a href="https://www.sciencedirect.com/science/article/abs/pii/S1053811919307207"><img align="left" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img02_small.png" width="317 px" style="padding: 10px"></a>

{: .text-justify}
To address that question, we designed a steady-state multi-task paradigm in which participants engaged twice in each of four distinct mental tasks for three minutes (see the paradigm to your left). By continuously acquiring data as subjects performed and transitioned between tasks, we avoided the confounds introduced by separate task scans—a common practice at the time. Using sliding-window functional connectivity and k-means clustering, we showed that FC patterns were more similar within tasks than across them, and that this structure was disrupted in low-performing subjects. In other words, time-varying FC patterns (at the scale of tens of seconds) can track engagement with specific cognitive demands. This study provided the first direct link between time-varying functional connectivity and cognition. Full details are available in our PNAS publication linked [here](https://www.pnas.org/content/112/28/8762.short). 

{: .text-justify}
A key question remained: what about time-varying functional connectivity in the absence of external task demands? Could these spontaneous fluctuations reflect self-driven cognitive processes—such as planning, recalling, or daydreaming—that occur covertly and unpredictably? Or are they better explained by other mechanisms, such as memory consolidation, internal model updating, or vigilance shifts? Answering this is difficult because, as researchers, we lack direct access to the timing or content of subjects’ thoughts (i.e., their [stream of consciousness](https://en.wikipedia.org/wiki/Stream_of_consciousness_(psychology))) as they rest quietly in the scanner. 

<a href="https://www.sciencedirect.com/science/article/abs/pii/S1053811919307207"><img align="right" src="/files/research/free_thoughts/isft_piechart.png" width="500 px" style="padding: 10px"></a> 

{: .text-justify}
To tackle this, we applied [k-means clustering](https://en.wikipedia.org/wiki/K-means_clustering) to time-varying FC matrices from resting-state scans. From our task studies, we knew this approach could divide scans into periods of distinct cognitive activity, but not reveal their nature. To infer that, we combined hemodynamic deconvolution with reverse inference. Dynamic deconvolution yielded representative activity maps for each time segment, which we then analyzed using the [Neurosynth](https://neurosynth.org/) platform to identify likely cognitive processes. This pipeline produced a list of mental processes consistently associated with distinct FC patterns. Although we could not validate results on a scan-by-scan basis, we compared our findings (see fiure on the right) with prior studies of self-reported mental activity during rest and found strong agreement. We interpreted this convergence as evidence that time-varying functional connectivity during rest reflects, at least in part, the ongoing stream of thoughts, feelings, and sensations that unfold during scanning.

**Selected References:**
* Gonzalez-Castillo J et al. “[Imaging the spontaneous flow of thought: distinct periods of cognition contribute to dynamic functional connectivity during rest](https://www.sciencedirect.com/science/article/abs/pii/S1053811919307207)”. NeuroImage (2019)
* Gonzalez-Castillo J et al. "[Tracking ongoing cognition in individuals using brief, whole-brain functional connectivity patterns](https://www.pnas.org/content/112/28/8762.short)". PNAS (2015)
* Gonzalez-Castillo J, Bandettini PA "[Task-based dynamic functional connectivity: recent findings and open questions](https://www.sciencedirect.com/science/article/abs/pii/S1053811917306535)". NeuroImage (2018)
* Gonzalez-Castillo J et al. "[The spatial structure of resting state connectivity stability on the scale of minutes](https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full)". Frontiers in Neuroscience (2014)

<a id="conscious-correlates"></a>
### Conscious correlates of spontaneous brain activity

<img align="left" src="https://javiergcas.github.io/files/research/free_thoughts/free_thoughts_relationship.png" width="500 px" style="padding: 10px">

{: .text-justify}
Brain activity is not always linked to concurrent external environmental demands or stimuli. In fact, complex dynamical patterns of activity—-and their conscious manifestation as an incessant stream of thoughts, emotions and sensations—-constantly unfold in otherwise apparently idle individuals. Despite their ubiquity and core role for survival, the neurobiological correlates of such inner experiences remain largely unknown. This scientific gap is mostly due to how difficult is to objectively characterize something that is so inherently covert and personal. Nonetheless, recent developments in functional neuroimaging, idiographic/experiential science and artificial intelligence (AI) provide a unique opportunity to build scientific models of the neurobiological, behavioral and clinical correlates of free thought. We are currently in the process of conducting new experiments that combine real-time fMRI, experiential methods and machine learning to learn more about the neural correlates of free thought.

**Selected References:**

* Gonzalez-Castillo J et al. “[How to interpret resting-state fMRI: ask your participants](https://www.jneurosci.org/content/41/6/1130)” Journal of Neuroscience (2021)

* Gonzalez-Castillo J et al. "[In-scanner thoughts shapre Resting-state Functional Connectivity: how participants "rest" matters](https://pmc.ncbi.nlm.nih.gov/articles/PMC11188111/)" BioRxiv (2024)

<a id="localization"></a>
### Localization and Distributed Functions

<img align="left" src="https://javiergcas.github.io/files/research/non_traditional/wide_activity_small.png" width="355 px" style="padding: 10px">

{: .text-justify}
The majority of task-based fMRI studies focus exclusively on interpreting positive BOLD deflections that tightly follow external stimuli or task demands (i.e., those sustained as long as the experimental intervention is in place). Although exclusive focus on positively sustained BOLD responses have proven successful to uncover the neuronal correlates of a myriad of human behaviors; unfortunately, this practice results in true neuronal responses continuously passing undetected in fMRI. As such, current conceptualizations of brain function based on task-based fMRI research are incomplete.

<img align="right" src="https://javiergcas.github.io/files/research/non_traditional/non_traditional_clusters_small.png" width="500 px" style="padding: 10px">

{: .text-justify}
In the past, we have shown how non-conventional BOLD responses, namely negative signal deflections accompanying task performance (negative sustained BOLD) and phasic responses that occur at the onset/offset of experimental events, can be modulated by cognitive demands. Using data with approximately six times higher signal-to-noise ratio than conventional fMRI, we were able to demonstrate that BOLD signal changes correlated with experimental task-timing occur in over 95% of the brain even for the simplest of tasks. These results not only highlight the inadequacy of current dichotomical interpretational models (active/inactive), but also challenge long accepted localizationist views of brain function demonstrating how non-canonical responses ought to be discussed if one is to acquire a full understanding of brain function. Important questions remain such as how to differentiate essential (i.e., signaling regions that are indispensable to accomplish a given task) from accessory activations, or how to report and interpret whole-brain activity maps.

**Selected References:**
* Gonzalez-Castillo J et al. “[Whole-brain, time-locked activation with simple tasks revealed using massive averaging and model-free analysis](https://www.pnas.org/content/pnas/109/14/5487.full.pdf)”. PNAS (2012)
* Gonzalez-Castillo J et al. “[Task Dependence, Tissue Specificity, and Spatial Distribution of Widespread Activations in Large Single-Subject Functional MRI Datasets at 7T](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4635913/pdf/bhu148.pdf)”. Cereb Cortex (2015) 