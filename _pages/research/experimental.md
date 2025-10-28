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
One key aspect of trustworthy data is its reliability. Of course, perfect test–retest reliability is neither expected nor necessarily desirable when studying a dynamic system like the human brain, which naturally changes from one measurement to the next. The real challenge lies in distinguishing genuine physiological variability from non-physiological noise and other confounding sources. Over the years, I have investigated the reliability of both task-based and resting-state data across multiple projects—two of which are highlighted here.

<img align="right" src="/assets/pub_images/repro_2017.png" width="317 px" style="padding: 10px">
{: .text-justify}
When I joined the Talavage lab at Purdue, I was provided with a challenging dataset. After nearly two years of attempting to make sense of it, I realized that was not possible: the data was unreliable. This motivated me to explore the reliability of fMRI in greater depth, culminating in this publication, where we report the test–retest reliability of an auditory sentence comprehension task. We focused on this particular cognitive domain because one of the lab’s main research lines examined the neural correlates of speech comprehension in cochlear implant users. Through this project, I was introduced to the field of [quality assurance](https://www.frontiersin.org/research-topics/33922/demonstrating-quality-control-qc-procedures-in-fmri/magazine), learned multiple approaches to assessing test–retest reliability (e.g., [dice coefficient](https://en.wikipedia.org/wiki/Dice-S%C3%B8rensen_coefficien), [intra-class correlation coefficient](https://en.wikipedia.org/wiki/Intraclass_correlation), etc.), and gained firsthand experience with the challenges of interpreting fMRI data—specifically, how meaningful individual differences in activation patterns can persist despite high group-level reproducibility. Ultimately, our findings demonstrated that the task performed well at the group level, suggesting it could serve as a reliable protocol for future population-level studies.

<img align="left" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img02_small.png" width="317 px" style="padding: 10px">
[Functional connectivity](https://en.wikipedia.org/wiki/Resting_state_fMRI#Functional), as measured with [BOLD](https://en.wikipedia.org/wiki/Blood-oxygen-level-dependent_imaging) fMRI, exhibits dynamic behavior at the scale of seconds, with rich spatiotemporal structure both during [resting state](https://en.wikipedia.org/wiki/Resting_state_fMRI) and task scans. What does such dynamicity reflects? To what extent do aberrant patterns of time-varying functional connectivity signal pathology? Those are all open questions. In early studies, we focused on characterizing the [sptio-tempotal structure of this dynamic phenomena](https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full) during the resting state. We were able to show that most stable connections correspond primarily to inter-hemispheric connections between left/right homologous regions; while most variable connections correspond to inter-hemispheric, across-network connections between non-homologous regions in occipital and frontal cortex (e.g., those subserving higher-order cognitive functions). We also demonstrated that well established resting state networks disintegrate on many occasions during a single scan, questioning the interpretability of such networks.



**References:**
* Gonzalez-Castillo J and Talavage TM “[Reproducibility of fMRI activations associated with auditory sentence comprehension](https://pmc.ncbi.nlm.nih.gov/articles/PMC3008333/pdf/nihms-244051.pdf)”. NeuroImage (2011)


