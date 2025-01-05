---
title: "MET uncertainty"
teaching: 40
exercises: 20
questions:
- "How to estimate the uncertainty on a composite object such as MET?"
- "How is it estimated?"
objectives:
- "Learn about MET uncertainty sources."
- "Learn How to get the MET uncertainty in MiniAOD analyses."
keypoints:
- "MET is affected by uncertainties associated with all the objects involved in its calculation, including jets, leptons, photons, and unclustered energy."
- "Jets are stochastic objects which its content fluctuates a lot. We measure the jet energy resolution to mitigate this effects."
---

> ## After following the instructions in the setup (if you have not done it yet) :
>
> ~~~
> FIXME
> ~~~
> {: .language-bash}
>
> This will open a jupyter notebook tree with various notebooks. 
{: .callout}


## MET Uncertainty

For analyses sensitive to missing transverse energy — those involving large MET contributions from neutrinos or other signatures — it is necessary to break MET into its individual components.
Since MET is calculated as the vector sum of contributions from jets, electrons, muons, taus, photons, and "unclustered energy" (energy not associated with reconstructed objects), the resolution and scale of each component must be propagated to MET.
These uncertainties are then treated as separate nuisance parameters each arising from a different physics object.

The physics objects that contribute the most are:
- **Jets:** Jet energy scale (JES) and jet energy resolution (JER) uncertainties directly impact MET, as jets typically contribute significantly to the total energy.
- **Unclustered Energy:** Unclustered energy includes contributions from particles not grouped into jets, leptons, or photons. The uncertainty arises from the resolution of individual particle types, such as charged hadrons, neutral hadrons, photons, and hadronic forward (HF) particles.
- **Leptons:** This includes tau leptons, electrons, muons, and photons. Scale uncertainties for these objects need to be propagated to MET, as even small variations can affect its calculation.

The scale and resolution of each component must be systematically varied within their respective uncertainties. These variations are then propagated to the MET calculation to calculate their impact on the analysis.

{% include links.md %}

