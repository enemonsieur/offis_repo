---
status: 
 (Summarize/Answer) (Revise 1-2-3) (Mindmap)
---

Functional spezialization: 
- Somekind of localization of mental function -> PFC
Functional integration
- All regions are summed up to realize the function -> WM: ACC + Hc + PFC

What we are analyzing is a bit of both. 

# Functional Connectivity
Do two different regions activated in the same time? Is one Bregion activating another one? Both of them? 
What are the 3 types of influences?


How do we measure the connectivity using voxels?
	Find the vCorr within and between subjects?
	1. Seed Voxel Correlation between
	2. SWC within #unclear
		1. Find the covariance/correlation of each voxels within all of the activated voxels of the brian
	- Use the eigenvariate?
- Activation induced Correlation#unclear
	- How does it affects finding the connectivity?
	- What's the activation effect?


1. What's PPI?
	Psychophysiological interafction (PPI) is **a brain connectivity analysis method. It estimates context-dependent changes in effective connectivity (coupling) between brain regions.
	what is effective connectivity?
		- Effective connectivity **describes the causal influences that neural units exert over another**.
		- **The influence that a node exerts over another under a network model of causal dynamics** and is inferred from a model of neuronal integration, which defines the mechanisms of neuronal coupling
	1. How do the variable in PPI have to be? 
		A PPI effect is defined as an interaction between the time series of a brain region (physiological variable) and a (or more) task design variable (psychological variable). Noises of both the physiological and psychological variables go into the interaction term, so that the interaction effect is much noisier than the main effects of task free connectivity (physiological main effect) and task activation (psychological main effect). This makes PPI analysis having lower statistical power than simple connectivity and conventional activation analysis. [Di, Biswal  2017](https://www.frontiersin.org/articles/10.3389/fnins.2017.00573/full)
	2. 
3. What's the #1 function of PPI?
	See how the nodes in the brain interact with each other as the tasks they are handling change
4. What is BSC?
5. What is the single most important thing that differenciate BSC from PPI?
6. What is effective connectivity?
	1. According to the definition of effective connectivity (Karl J. Friston 1994), which refers to the directed effect that one brain region has on another under some model of neuronal coupling, a PPI can be regarded as a condition specific change in effective connectivity, under a simple general linear model (GLM) of interregional coupling.
7. What does PPI measures between conditions?
	1. In order to do so, we need to first clarify why the PPI method always **measure connectivity differences between conditions.**  /... / How PPI can measure the differences between the trial-by-trial dependency in one condition and the moment-to-moment dependency in the remaining time points. 
8. What is functional connectivity?
	1. The term functional connectivity was first defined by Friston (Karl J. Friston 1994) as temporal correlations between spatially remote brain regions.
	2. 
	3. 
	4. 
	5. Assuming that the functional connectivity is the same during the period of scan, e.g. in resting state, it is straightforward to calculate correlation coefficients between two brain regions to represent functional connectivity. In a more general regression form, the model can be expressed as:  
	6. 
9. What's a seed region?
	1. The seed is **typically identified based on anatomical landmarks, coordinates, or the location of brain activity during a separate task**.
	a **seed region** (the physiological variable) and the psychological variable into a regression model. 

10. How's the regression coefficient different frm
11. How do regression coefficient affects the PPI?
12. How does regression coefficient differs in PPI and BSC?
13. Why is correlation and decorrelation important in PPI?
14. How can we model the temporal connection between brain regions?
15.

In most of task fMRI experiments, researchers design different task conditions within a scan run, so that the effect of interest becomes the differences of temporal dependencies between the conditions. We can combine eqs. 1and2to include both the time series of a seed region (the physiological variable) and the psychological variable into a regression model. Most importantly, the interaction term of the psychological and physiological variables can also be included. For the simplest scenario of only one psychological variable (two conditions), the psychophysiological interaction model can be expressed as:
![[Pasted image 20220720123708.png]]
	- Is Y the overall BOLD response?
	- Is  all Beta modelling the difference in response from two different seeds in 2 different conditions?
	
So that the relationship between the seed region xPhysio and test region y is: β2 + β3 ∙ xPsych, which is a linear function of xPsych. Therefore, a significant β3 represent significant task modulations on effective connectivity. Similar to the interpretation of task main effects, the interpretation of the PPI effect depends not only on the PPI itself, but also the on other regressors in the model. In eq. 3the main effect of time series xPhysio is included. We can think about the time series main effect xPhysio and interaction effect xPhysio ∙ xPsych as the second order counterparts of the constant effect and main effect of xPsych in eq. 1.
What are the differences in effect between the Xphysio model and the Xpsychological model.

bold signal and compute it
then they deconvolve the interactions in the neural level and reconvolve that

differnces Event related deconvolve - bad correct estimate of N.activity
block d- is good. 
So show the diff. 

![[Pasted image 20220721175153.png]]
This equation models the BOLDr Y of the prefrontal cortex, using the psychophysical response of the hippocampus (the seed region) XPsych and XPhysio. 
In this model, By combining the change in condition (Remembering  a maze or not. 0 1) with the physiological response of another brain region  (The HDR*)


. Using functional imaging data, researchers can investigate not only which individual brain areas are involved in a task, but also how information flows between brain areas ([Stephan, 2004](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3375893/#nss055-B19); [Friston, 2011](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3375893/#nss055-B10); [Smith _et al._., 2012](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3375893/#nss055-B18)) and how functional areas can change their connectivity to participate in different networks at different times ([Smith _et al._., 2012](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3375893/#nss055-B18)), or under different behavioural circumstances
 PPIs analysis concerns task-specific increases in the relationship between different brain areas’ activity ([Friston _et al._., 1997](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3375893/#nss055-B8)). PPI is a measure of what is generally referred to as functional connectivity—a statistical dependence between activity in between brain areas.