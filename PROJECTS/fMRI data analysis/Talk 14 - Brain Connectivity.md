-------------------------
**status**: 
 ( ~~Highlight~~) (ID questions/Blocks) (Summarize/Answer) (Revise 1-2-3) (Mindmap)
 
-----------------------------------------------------------------------------------------

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

We can combine eqs.  to include both the time series of a seed region (the physiological variable) and the psychological variable into a regression model. Most importantly, the interaction term of the psychological and physiological variables can also be included. For the simplest scenario of only one psychological variable (two conditions), the psychophysiological interaction model can be expressed as: 

Equation 3can be illustrated figuratively in Fig. 1D. Combine the two terms with xPhysio,eq.3can be expressed as: y ¼ β0 þ β1⋅xPsych þ β2 þ β3⋅xPsych ⋅xPhysio þ ε ð4Þ So that the relationship between the seed region xPhysio and test region y is: β2 + β3 ∙ xPsych, which is a linear function of xPsych. Therefore, a significant β3 represent significant task modulations on effective connectivity.