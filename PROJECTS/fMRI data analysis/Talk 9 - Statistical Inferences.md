---
Stat Inference: 
alias: (Summarize/Answer) (Revise 1-2-3) (Mindmap) 
---
FWR: Prob of number of errors we're gonna make, FDR Number of errors we make
- What's the R-Resel is a theoritical voxel that takes the smoothness and the Volume of the data in account to correct for the p-value for multiple "subjects"
**Why do we take FDR rather than FWE?**
	Bc the FWE will often leave no data with significant results. It can be too conservative. 
**What's FDR?**
	FDR-controlling procedures are designed to control the FDR, which is the expected proportion of "discoveries" (rejected null hypotheses) that are false (incorrect rejections of the null).[1] Equivalently, the FDR is the expected ratio of the number of false positive classifications (false discoveries) to the total number of positive classifications (rejections of the null). 
	We can do thatby ordering the p-values
	You can correct the p values by having multiple differe threshold, for each cluster

**Why is FWError more conservative?**

2. What does overcorrection means in the Bonferroni test?
	1. When there's a strong correlation within the data, there's a higher  chance that if one data has a significant t>alpha, the other also are, therefore, Because of the much lower threshold of Bonferroni, Many Positive will be missed = False Negative = conservative

4. what does the 2nd Level Y means??
**5. What is the Level 1 contrast test meausring?**
	1. 
6. how do you know a cluster is stat. significant?
	1. When the p-corrected value of the cluster crosses the k-threshold
7. How does Family wise Error works helps correcting the p-value
8. How do Non-Parametric helps correcting the p-value
9. What does controlling means in the FDR?
- The FWE is a measure of Type 1 errors over multiple tests

What are the different levels of significance?
	Voxel level
	Cluster of voxels?
	Set level? 
w
	1. What does voxel level of significance implies?
		There's no correlation between voxel, as there's independently activated. 
	What type of inf don't we get with VL significance
		This doesn't get information (spatial) about the signal. 
		Because we smooth that shit out,the activation of the signal will spread to surrounding signals
	2. Cluster level inference
		1. what are clusters?
			A group of contiguous voxels, with the t above a stat.level Uc
	**how do you know a cluster is stat. significant?**
		If its overall t-threshold is above k
	How do we do decide what cluster and what level of activation are relevant?
		You find the t-values of every voxels.  
		Do a plot by time and define a thresold Uc = relevant for the cluster. 
		Set the cluster threshold: Not too low nor too high
		Lack of spatial specificity: You don't know which voxels are significant inside, so not too big cluster. 
	3. Set level Inference
	You wont know which clusters are significants. They don't have a spatial definition. 



What's a type I error?
	a false positive error?
		We rejected the null hypothesis, even though there was no difference between the two sets of data taken from the same distribution=> we assumed there was a stat sign. difference, where there wasn't. => We thought there were brain activation while there wasn't.

How's a type I error noted?
	alpha
What's a type II error?
	When we failed to reject the Ho, EVEN THOUGH there was a difference! (Bc well, the difference wasn'T big enough), which doesn't mean there's no difference between the data. Just that we can't prove, the two samples, taken from the same data, are significantly different => they may come from the same dataset => There's no activation of the voxel/cluster
	how can we evaluate the prob of a test to reject the Ho?
		1-alpha = power procedure
Problem with the standart Ho significant vale is that it's easier to have false positive. 
What should we use to id voxels/cluster that are so active, that that can't be done by random?
	Using Family Wise Error and

How does Family wise Error works
	What's FWE rate?
		probability of making one or more false discoveries, or type I errors when performing multiple hypotheses tests.
	What are 3 relevant types of FWE?
		RFT, Parametric, Non-Parametric simulations


 What do we take into account in FWerror?
	 We take into account the internal and external smoothing. Because we don't have independent tests. That we take into account for correcting the voxels


Random Field Theory: How does it do p-value correction  
	Estimates the smoothness of your t-image by recreating the filter, and base on that calculates the corrected p-value. 
	The more the filter increases, the smoother the image was =>the more the corr happens on a longer distances => the smaller the p value becomes. A very smooth data means we gotta be VERY CONSERVATIVE #unclear

What is Random Field Theory
	It's a math formula to estimate corrected p-values for each clusters. It  kinda does it by estimating the Smoothness of the data (intrinsic and after smoothing), and the more it finds smoothness, the lower the p-value will be => and the higher the Uc will be.
	Which means, too much smoothness in the data makes it hard to find FP and we have to be more conservative.
What are some issues with Random Field Theory?
	The demands a lot of assumption and don't work well for low smoothed datas. 
What are parametric designs?
	Methods like the Monte Carlo, similar to RFT but they don't rely on approximate results. They are comp. intensive
What are non-parametric approches in FWER?
	They use the data itselfs to recreate empirical new distribution of the test statistic
How do Non-Parametric works? 
	It works will the assuption that the Ho is correct, for example, that t-groups of High Low performers don't differ. So that their BOLDr are the same. If it's true, shufflling 1 or 2 in the other group, won't change the BOLDr of the 2 groups. Now we reshuffle that shit till every new test statistic curve possible is created.
	Now the question is, how many of those say... 300  new 



What's cluster building threshold?
	It decides how big our clusters are, a low threshold will give us a very large cluster. And higher t. will give many cluster?
How does FWE and FDR helps in cluster levels? 


