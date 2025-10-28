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

### Exploring the Quality of fMRI Data

{: .text-justify}
Of course, perfect test–retest reliability is neither expected nor necessarily desirable when studying a dynamic system like the human brain, which naturally changes from one measurement to the next. The real challenge lies in distinguishing genuine physiological variability from non-physiological noise and other confounding sources. Over the years, I have investigated the reliability of both task-based and resting-state data across multiple projects—two of which are highlighted here.

<img align="right" src="/assets/pub_images/repro_2017.png" width="317 px" style="padding: 10px">
{: .text-justify}
When I joined the Talavage lab at Purdue, I was provided with a challenging dataset. After a year attempting to make sense of it, I realized that was not possible: the data was unreliable. This have motivated me to explore the reliability of fMRI in greater depth over the years.

My first dive into it is summarized in one of the [publications](https://www.sciencedirect.com/science/article/abs/pii/S105381191001284X) from my Ph.D. Thesis work where I evaluated the test–retest reliability of an auditory sentence comprehension task. This was of interest to my hosting lab, as one of its research focus was the neural correlates of speech comprehension in cochlear implant users. This project introduced me to the field of [quality assurance](https://www.frontiersin.org/research-topics/33922/demonstrating-quality-control-qc-procedures-in-fmri/magazine), tought me multiple ways to assess test–retest reliability (e.g., [dice coefficient](https://en.wikipedia.org/wiki/Dice-S%C3%B8rensen_coefficien), [intra-class correlation coefficient](https://en.wikipedia.org/wiki/Intraclass_correlation), etc.), and exposed me to one of the main interpretational challenges in fMRI: the importance of correctly identifying sources of individual differences that persist despite high group-level reproducibility. As for the proposed task, our findings demonstrated that the task performed well at the group level, suggesting it could serve as a reliable protocol for future population-level studies.

<img align="left" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img01.png" width="317 px" style="padding: 10px">
Another deep dive into reproducibility came from a study examining how patterns of resting-state functional connectivity evolve during a one-hour scan. Unlike task-based fMRI, resting-state scans require little from participants—simply to stay still, remain awake, and let their minds wander. This simplicity makes the approach ideal for clinical populations and easier to acquire than task-based data.

By the time I entered this area, it was well established that resting-state connectivity, averaged over several minutes, is reliable across sessions and carries meaningful phenotypic information (e.g., traits, symptoms). Yet, emerging evidence suggested these connectivity patterns fluctuate substantially within a single scan—raising a fundamental question: is this variability meaningful or merely noise?

In this first exploration of time-varying connectivity, I focused on two key questions: (1) how scan duration affects the reliability of average connectivity estimates, and (2) whether the observed variability exhibits meaningful spatial structure. The first question is practical—fMRI is expensive, and participants can only remain still for so long—while the second probes whether the variability reflects genuine neural dynamics.

Our results showed that reliability improves with scan length, with at least 10 minutes of data needed for stable estimates. We also identified distinct spatial patterns: the most stable connections were interhemispheric links between homologous regions, while the most variable involved cross-network, non-homologous connections in frontal and occipital cortex—regions supporting higher-order cognition.

**References:**
* Gonzalez-Castillo J and Talavage TM “[Reproducibility of fMRI activations associated with auditory sentence comprehension](https://pmc.ncbi.nlm.nih.gov/articles/PMC3008333/pdf/nihms-244051.pdf)”. NeuroImage (2011)

### Multi-Echo fMRI

### Optimization of Acquisition Parameters for fMRI

### Realtime fMRI 

