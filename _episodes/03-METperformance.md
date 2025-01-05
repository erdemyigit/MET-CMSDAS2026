---
title: "MET performance"
teaching: 40
exercises: 20
questions:
- "How do we measure the MET performance (i.e. MET scale and MET resolution) ?"
objectives:
- "Learn about MET performance."
- "Measure the resolution and scale of MET for different MET algorithms and calibrations."
keypoints:
- "The performance of MET is studied in events with a well-measured Z boson (decaying to electrons or muons) or an isolated photon, which should have little to no genuine MET."
- "Transverse momentum conservation is used to study MET response and resolution along Z axis."
---

> ## After following the instructions in the setup, make sure you are using the SLC7 singularity shell:
>
> ~~~
> cd $CMSSW_BASE/src/CMSDAS_MET
> cmssw-el7
> cmsenv
> ~~~
> {: .language-bash}
{: .callout}


## MET performance

A well-measured Z boson or photon provides a unique event axis and a precise momentum scale for evaluating MET performance.
To achieve this, the response and resolution of MET are studied in samples where a Z boson decays to a pair of electrons or muons, or in events with an isolated photon.
**Such events should have little to no genuine MET.**
The MET performance is then assessed by comparing the momentum of the vector boson to that of the hadronic recoil system.
The hadronic recoil system is defined as the vector sum of the transverse momenta of all PF candidates, excluding the vector boson (or its decay products in the case of Z boson decay).

{% include links.md %}

