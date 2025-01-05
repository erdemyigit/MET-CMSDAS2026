---
title: "Handling Anomalous MET Events"
teaching: 20
exercises: 10
questions:
- "What is anomalous MET?"
- "How to identify these events?"
objectives:
- "Learn about anomalous MET"
- "Learn about the Noisy event filters and their implementation."
keypoints:
- "Large MET in an event may be caused by detector noise, cosmic rays, and beam-halo particles. Such MET with uninteresting origins is called false MET, anomalous MET, or fake MET and can be an indication of problematic event reconstruction."
- "Events with anomalos mets can be rejected using the Noisy event filters."
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

## What is anomalous MET? 

Anomalous MET refers to events where the measured MET deviates from what is expected due to various factors, such as reconstruction failures, detector malfunctions, or background noise.
These anomalous MET events can arise from:
- **Detector Issues:** Malfunctions or mismeasurements in detectors, such as the electromagnetic calorimeter (ECAL) or hadronic calorimeter (HCAL), leading to spurious energy deposits.
- **Reconstruction Failures:** Errors in reconstructing particle tracks or energy, including issues with jets, leptons, or unclustered energy, that result in inaccurate MET calculations.
- **Non-collision Origins:** Spurious signals from sources unrelated to the particle collision, such as beam-halo particles, cosmic rays, or other environmental factors.
- **Dead or Malfunctioning Detector Cells:** Areas of the detector that fail to register energy deposits correctly, leading to underestimation of the MET.

In such events, the MET value may be much higher than expected and does not reflect true missing energy from invisible particles (like neutrinos or dark matter candidates).

## Noisy event filters

To identify false MET, several algorithms have been developed that analyze factors such as timing, pulse shape, and signal topology.
When fake MET is detected, the corresponding events are typically discarded.
These cleaning algorithms, or filters, run in separate processing paths, and the outcome (success or failure) is recorded as a filter decision bit.
Analyzers can use this decision bit to filter out noisy events. These filters are specifically designed to reject events with unusually large MET values caused by spurious signals.

{% include links.md %}

