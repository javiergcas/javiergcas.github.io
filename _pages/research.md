---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

### What are the neuronal drivers of time-varying functional connectivity?

<img align="right" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img01.png" width="317 px" style="padding: 10px">

{: .text-justify}
[Functional connectivity](https://en.wikipedia.org/wiki/Resting_state_fMRI#Functional) (FC), as measured with [BOLD](https://en.wikipedia.org/wiki/Blood-oxygen-level-dependent_imaging) fMRI, exhibits dynamic behavior at the scale of seconds, with rich spatiotemporal structure both during rest and task scans. What does such dynamicity reflects? To what extent do aberrant patterns of time-varying FC signal pathology? Those are all open questions. In early studies, we focused on characterizing the [sptio-tempotal structure of this dynamic phenomena](https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full). We were able to show that, during rest, most stable connections correspond primarily to inter-hemispheric connections between left/right homologous regions; while most variable connections correspond to inter-hemispheric, across-network connections between non-homologous regions in occipital and frontal cortex (e.g., those subserving higher-order cognitive functions). We also demonstrated that well established resting state networks disintegrate on many occasions during a single scan, questioning the interpretability of such networks.

<img align="left" src="https://javiergcas.github.io/files/research/tvfc/research_tvfc_img02.png" width="317 px" style="padding: 10px">

{: .text-justify}
In addition to studying the region-to-region spatiotemporal structure of time-varying FC during rest, I have also conducted experiments aimed at validating the interpretability of whole-brain dynamic FC patterns as markers of on-going cognition. In particular, using multi-task scans and unsupervised machine learning techniques we demonstrated a direct [link between short-term (tens of seconds long) whole-brain FC patterns and on-going mental processing](https://www.pnas.org/content/112/28/8762.short) at the single-subject level. More recenlty, we have applied the [same methodology to resting-state data](https://www.sciencedirect.com/science/article/abs/pii/S1053811919307207) and demonstrated that it is possible to infer the cognitive nature of a subjects' mental activity at discrete scan segments on the basis of time-varying connectivity and hemodynamic deconvoltion.

**References:**
* Gonzalez-Castillo J et al. “[Imaging the spontaneous flow of thought: distinct periods of cognition contribute to dynamic functional connectivity during rest](https://www.sciencedirect.com/science/article/abs/pii/S1053811919307207)”. NeuroImage (2019)
* Gonzalez-Castillo J et al. "[Tracking ongoing cognition in individuals using brief, whole-brain functional connectivity patterns](https://www.pnas.org/content/112/28/8762.short)". PNAS (2015)
* Gonzalez-Castillo J, Bandettini PA "[Task-based dynamic functional connectivity: recent findings and open questions](https://www.sciencedirect.com/science/article/abs/pii/S1053811917306535)". NeuroImage (2018)
* Gonzalez-Castillo J et al. "[The spatial structure of resting state connectivity stability on the scale of minutes](https://www.frontiersin.org/articles/10.3389/fnins.2014.00138/full)". Frontiers in Neuroscience (2014)

### What are the neuronal correlates of self-driven thoughts and inner experiences?

<img align="left" src="https://javiergcas.github.io/files/research/free_thoughts/free_thoughts_relationship.png" width="500 px" style="padding: 10px">

{: .text-justify}
Brain activity is not always linked to concurrent external environmental demands or stimuli. In fact, complex dynamical patterns of activity—-and their conscious manifestation as an incessant stream of thoughts, emotions and sensations—-constantly unfold in otherwise apparently idle individuals. Despite their ubiquity and core role for survival, the neurobiological correlates of such inner experiences remain largely unknown. This scientific gap is mostly due to how difficult is to objectively characterize something that is so inherently covert and personal. Nonetheless, recent developments in functional neuroimaging, idiographic/experiential science and artificial intelligence (AI) provide a unique opportunity to build scientific models of the neurobiological, behavioral and clinical correlates of free thought. We are currently in the process of conducting new experiments that combine real-time fMRI, experiential methods and machine learning to learn more about the neural correlates of free thought.

**References:**
* Gonzalez-Castillo J et al. “How to interpret resting-state fMRI: ask your participants” Journal of Neuroscience (Accepted)

### What is the true extent of neural activity as measured with fMRI?

The majority of task-based fMRI studies focus exclusively on interpreting positive BOLD deflections that tightly follow external stimuli or task demands (i.e., those sustained as long as the experimental intervention is in place). Although exclusive focus on positively sustained BOLD responses have proven successful to uncover the neuronal correlates of a myriad of human behaviors; unfortunately, this practice results in true neuronal responses continuously passing undetected in fMRI. As such, current conceptualizations of brain function based on task-based fMRI research are incomplete.

<video controls="controls" width="355 px" height="180 px" name="Activity" src="files/research/non_traditional/wide_activity_video01_480.mov"></video>

In the past, we have shown how non-conventional BOLD responses, namely negative signal deflections accompanying task performance (negative sustained BOLD) and phasic responses that occur at the onset/offset of experimental events, can be modulated by cognitive demands. Using data with approximately six times higher signal-to-noise ratio than conventional fMRI, we were able to demonstrate that BOLD signal changes correlated with experimental task-timing occur in over 95% of the brain even for the simplest of tasks. These results not only highlight the inadequacy of current dichotomical interpretational models (active/inactive), but also challenge long accepted localizationist views of brain function demonstrating how non-canonical responses ought to be discussed if one is to acquire a full understanding of brain function. Important questions remain such as how to differentiate essential (i.e., signaling regions that are indispensable to accomplish a given task) from accessory activations, or how to report and interpret whole-brain activity maps.

### How can we improve the informational value of fMRI?

{: .text-justify}
Noise, meaning signal fluctuations of no neuronal origin, accounts for well over 75% of the variance in fMRI data. Elevated noise is the root cause for the low reliability and sensitivity of fMRI studies and a key factor precluding clinical adoption. To minimize these detrimental effects of elevated noise levels, complex pre-processing always precedes statistical analyses. Yet, current pre-processing algorithms are flawed, and superior, multipurpose techniques that can remove non-neuronal variance with minimal human intervention are in great demand. This is particularly true for clinical fMRI, where merging data across subjects is not possible, and manual intervention must be minimized to optimize clinical usability. 

In the past, I have conducted several projects aimed at improving the quality of fMRI. These include optimization of acquisition parameters, improvements in data preprocessing techniques, reliability studies, and design and evaluation of methods based on multi-echo fMRI ([14]; see below).

Regarding data acquisition optimization, I have conducted work aimed at generating novel guidelines for the selection of flip angles (a key imaging parameter in fMRI scanning sequences) for optimization of sensitivity to neuronally driven BOLD signal changes [10]. Until then, the flip angle in fMRI acquisitions was commonly set to be equal to the Ernst angle, which is meant to maximize spatial signal-to-noise ratio. This is a logical choice for static (e.g., anatomical MR imaging), but not for fMRI which studies temporal signal fluctuations. Using a combination of simulations and empirical data, we were able to demonstrate that one can chose flip angles well below the Ernst angle when physiological noise (e.g., cardiac and respiratory fluctuations) are the dominant noise source in fMRI recordings. In this work, we provide strategies to compute optimal flip angles for fMRI studies. These results constitute an important improvement for how to acquire fMRI data, as reductions in flip angle automatically translate into reduction of RF power, limitation of apparent T1-related inflow effects, reduction of through-plane motion artifacts, lower levels of physiological noise, and improved tissue contrast. All of these result in significant improvements in data quality, and even allow faster imaging at higher field intensities as a result of the decrease in RF power. 

In recent years, several groups have turned their attention to multi-echo (ME) fMRI as a technique that can help recover signal in regions characterized by large dropout and that permits automatic removal of most common noise sources in fMRI. In a nutshell, ME-denoising works as follows. First, data is acquired with a ME sequence that generates several concurrent time series per voxel, each with a different echo time. This ME data is subsequently linearly mixed and input to a source decomposition algorithm (e.g., ICA). Resulting components are then automatically classified as noise or signal based on their echo time dependence profile; those classified as noise are regressed out from the data. This approach has been shown to significantly increase the sensitivity of connectivity measures in subcortical regions, the quality of activity maps for both event-related and block designs, as well as to accurately remove non-BOLD signal drifts so that slow changes in BOLD signals, such as those induced by in-scanner pharmacological interventions, can be monitored.

Still, many questions remain regarding how to optimally acquire and process ME data. Moving forward, I would like to continue working on the refinement and evaluation of ME-fMRI techniques, as I believe they can resolve pressing issues such as systematic differences in data quality across scanners/centers, excessive motion artifacts in pediatric populations, or insufficient signal levels in regions near air-filled cavities. I also would devote time to investigate how to best leverage the richness of ME-fMRI in real-time (see research item 4), so that denoising can be accomplished as scanning progresses. Finally, I plan to study the echo-dependence profiles of fMRI derivatives, including graph theory metrics and dynamic aspects of connectivity. The goal here is to carry out echo-dependence analysis directly over these secondary statistics, so that those that best capture BOLD-related phenomena can be readily identified.



### What is the true extent of neural activity?

### Realtime fMRI applications

# Prior Research

### Graduate work at Purdue University

My graduate research had two main components: one was purely methodological and included research on fMRI paradigm reliability and the effects of acoustic noise in fMRI; the second was more neuroscience oriented and focused on different aspects of speech perception and language representations in the brain.

The most methodologically oriented work can be found in the following publications:

  * 2011: [Assesment of tempora state-dependent interactions between auditory fMRI responses to desided and undesired acoustic sources](https://javiergcas.github.io/publication/2011-01-01-Assessment-of-temporal-state-dependent-interactions-between-auditory-fMRI-r)
  * 2012: [Hemodynamic Imaging: Functional Magnetic Resonance Imaging](https://javiergcas.github.io/publication/2012-01-01-Hemodynamic-Imaging%3A-Functional-Magnetic-Resonance-Imaging)
  * 2014: [Auditory neuroimaing with fMRI and PET](https://javiergcas.github.io/publication/2014-01-01-Auditory-neuroimaging-with-fMRI-and-PET)

As for the speech and language representation work, please check those:

  * 2008: [Neuroanatomical distribution of five semantic components of verbs: Evidence from fMRI](https://javiergcas.github.io/publication/2008-01-01-Neuroanatomical-distribution-of-five-semantic-components-of-verbs%3A-Evidence)
  * 2010: [The two-level theory of verb meaning: an approach to integrating the semantics of action with the mirror neuron system](https://javiergcas.github.io/publication/2010-01-01-The-two-level-theory-of-verb-meaning%3A-An-approach-to-integrating-the-semant)
  * 2011: [Reproducibility of fMRI activations associated with auditory sentence comprehension](https://javiergcas.github.io/publication/2011-01-01-Reproducibility-of-fMRI-activations-associated-with-auditory-sentence-compr)

#### Research work at Hewlett-Parckard Labs

Prior to my Ph.D. I did some research at Hewlett Packar Labs in Bristol, UK. That work mostly focused on the development of algorithms for e-commerce applications. The outcome of that work can be found in two conference proceedings:

* 2001: [Description Logics for matchmaking of services](https://javiergcas.github.io/publication/2001-01-01-Description-logics-for-matchmaking-of-services)
* 2001: [A semantic web approach to service description for matchmaking of services](https://javiergcas.github.io/publication/2001-01-01-A-semantic-web-approach-to-service-description-for-matchmaking-of-services)
