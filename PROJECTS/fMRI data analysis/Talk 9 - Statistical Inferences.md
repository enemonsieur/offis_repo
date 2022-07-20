---
Stat Inference: 
alias: (Summarize/Answer) (Revise 1-2-3) (Mindmap) 
---
What are the different levels of significance?
	Voxel level
	Cluster ofvoexesl?
	Set level? 
	1. What does voxel level of significance implies?
		There's no correlation between voxel, as there's idnependently activated. 
	What type of inf don't we get with VL significance
		This doesn't get information (spatial) about the signal. 
		Because we smooth that shit out,the activation of the signal will spread to surrounding signals
	2. Cluster level inference
		1. what are clusters?
			A group of contiguous voxels, with the t above a stat.level Uc
	how do you know a cluster is stat. significant?
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
		The chances of having 1+ FP anywhere in the image
	What are 3 relevant types of FWE?
		RFT, Parametric, Non-Parametric simulations


Why is Bonferroni correction unuseful for.. for what again?
	 Bonferroni Correction: Divide the p>0.5 by the number of tests. So its like 0.5/1000 voxels 
	 The problem is that it'll create a lot of FN (because it cuts too low, it demands a very high ttest to say: Yees, this isnt done by random noise)
	 The data by itselfs have intrinsic smoothness + smoothings for gaussian and Bonferroni don't account for this correlation between voxels 

What does FWE means?
	 Means: we look at the family of test and we wanna keep the alpha* level p-value to 0.05 for the entire family. 
 What do we take into account in FWerror?
	 We take into account the internal and external smoothing. Because we don't have independent tests. That we take into account for correcting the voxels. The theory that helps explaining that is RFtheory
What's the corrected p-value? #unclear 

Random Field Theory: How does it do p-value correction  
	Estimates the smoothness of your t-image by recreating the filter, and base on that calculates the corrected p-value. 
	The more the filter increases, the smoother the image was =>the more the corr happens on a longer distances => the smaller the p value becomes. A very smooth data means we gotta be VERY CONSERVATIVE #unclear
What is R in the RFT
	R is the Reso volume? the volume of the brain, than we calculate / smoothing function. To determine how smooth or correlated or dependent our data are. If its already pretty smooth, you won't have to correct the p value. 
	The smaller the smoothness the bigger the p-value will be transform
What is Random Field Theory
	It's a math formula to estimate corrected p-values for each clusters. It  kinda does it by estimating the Smoothness of the data (intrinsic and after smoothing), and the more it finds smoothness, the lower the p-value will be => and the higher the Uc will be.
	Which means, too much smoothness in the data makes it hard to find FP and we have to be more conservative.
What are some issues with Random Field Theory?
	The demands a lot of assumption and don't work well for low smoothed datas. 
What are parametric designs?
	Methods like the Monte Carlo, similar to RFT but they don't rely on approximate results. They are comp. intensive
What are non-parametric approches in FWER?
	They use the data itselfs to recreate empirical new distribution of the test statistic
How do Non-Parametric works? #unclear
	It works will the assuption that the Ho is correct, for example, that t-groups of High Low performers don't differ. So that their BOLDr are the same. If it's true, shufflling 1 or 2 in the other group, won't change the BOLDr of the 2 groups. Now we reshuffle that shit till every new test statistic curve possible is created.
	Now the question is, how many of those say... 300  new 

False discovery rate
Why do we take FDR rather than FWE?
	Bc the FWE will often leave no data with significant results. It can be too conservative. 
What's FDR? #unclear NOT UNDERSTOOD EVEN WITH THE  BOOK
	is the proportion of Type I errors among the rejected hypotheses FDR=P*(V/R)
What does FDR depends on?
	Cutt off P-values
What do we wanna control in FDR?
	the number of FP within the total positive values. Because we know in that there's are some FP, so we wanna make sure its not too big.
Why is FWError more conservative?
There are FP and Tp in the Positive we find. Within those Positves, can we 'control' the number of FP, so we always have roughliy the same value of FP? We can do thatby ordering the p-values
You can correct the p values by having multiple differe threshold, for each cluster.



What's FWE correction
	Prob of finding one or more false discoveries (Type I error), as we perform multiple voxels stat analysis.

What are we looking for at a cluster level?
	We look at the size of the activation and find its its randomn noise or not. 
What's cluster building threshold?
	It decides how big our clusters are, a low threshold will give us a very large cluster. And higher t. will give many cluster?
How does FWE and FDR helps in cluster levels? 


