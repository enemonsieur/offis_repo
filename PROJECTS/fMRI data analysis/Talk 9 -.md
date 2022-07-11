What are the different levels of significance?
	Voxel level
	Cluster ofvoexesl?
	---? 

1. Voxel level of significance
	There's no correlation between voxel,as there's idnependently activated. 
	This doesn't get information (spatial) about the signal. 
	Because we smooth that shit out,the activation of the signal will spread to surrounding signals
2. Cluster level inference
	Ho do we do decide what cluster and what level of activation are relevant?
		You find the t-values of every voxels.  Do a plot by time and define a thresold relevant for the cluster. 
		Set the cluster threshold: Not too low nor too high
		Lack of spatial specificity: You don't know which voxels are significant inside, so not too big cluster. 
3. Set level Inference
	You wont kno which clusters are significants. They don't have a spatial definition. 

Problem with the standart Ho significant vale is that it's easier to have false positive. 
What should we use to id voxels/cluster that are so active, that that can't be done by random?
	Using Family Wise Error and

How does Family wise Error works?
	 Bonferroni Correction: Divide the p>0.5 by the number of tests. So its like 0.5/1000 voxels 
	 The problem is that it'll create a lot of FN (because it cuts too low, it demands a very high ttest to say: Yees, this isnt done by random noise)
	 The data by itselfs have intrinsic smoothness + smoothings for gaussian and Bonferroni don't account for this correlation between voxels 


 Means: we llok at the family of test and we wanna keep the alpha* level p-value to 0.05 for the entire family. 
 What do we take into account in FWerror?
	 We take into account the internal and external smoothing. Because we don't have independent tests. That we take into account for correcting the voxels. The theory that helps explaining that is RFtheory

Random Field Theory p-value correction (is FWError)
	Estimates the smoothness of your  t-image. Its used to figue out, what "filter" was used to smooth your imaged.
	The more the filter increases? the more the corr happens on a longer distances and the smaller the p value increase. A very smooth data means a very small correction or so. 
	R is the Reso volume? the volume of the brain, than we calculate / smoothing function. To determine how smooth or correlated or dependent our data are. If its already pretty smooth, you won't have to correct the p value. 
	The smaller the smoothness the bigger the p-value will be transform
	whats RFT takes into account?
		It takes into account the smoothness of thedata
  
False discovery rate
	Has to do with this false positive and negative
	R is the total of FP and TP
	We say, 5% of the voxels we measue are wrongly declared as FP
What's FDR?
	is the proportion of Type I errors among the rejected hypotheses FDR=P*(V/R)
What does FDR depends on?
	Cutt off P-values
What do we wanna control in FDR?
	the number of FP within the total positive values. Because we know in that there's are some FP, so we wanna make sure its not too big.
Why is FWError more conservative?

What's FWE correciton
	Prob of finding one or more false discoveries (Type I error), as we perform multiple voxels stat analysis.

What are we looking for at a cluster level?
	We look at the size of the activation and find its its randomn noise or not. 
What's cluster building threshold?
	It decides how big our clusters are, a low threshold will give us a very large cluster. And higher t. will give many cluster?
How does FWE and FDR helps in cluster levels? 

What are the contrasts rate and contrast images?
What's the first level analysis?
What's the second level analysis?
	Group analysis
		![[Pasted image 20220711125716.png]]


How do they differ?
What's Y in the 2nd level?
	The become the Beighteds, that we found by analysing every subjects in the first level
		it represent the  contrast image of different subjects.
		They are the weighted sum of the Betas from the 1st level, which gives the difference btwen light ON OFF for ONE subject: s1= c1* B1,1+ cn* Bn,1. Is this difference larger than zero? That is the question
			B1,1 is the index for Betas
			Then for each subjec we have their Sm, which represent the  Y of the 2nd level analysis.. so that we have Subject m = c1 * B1,m + cnBn,m



Then we wanna minimise the betas that we found from each subjects so that we have a mean of
What are the dimensions of Y
	they depends on the subjects. And the d2 is 1 because we find the weighted sum of all the Beta so we have 1,n(subjects). This isjust for one voexels right??

What's the lenght of the C vector ?
	Just one because we estimatejust one betas in the 2nd level

What are one and two sample t-test for 2nd Level?

How do we get the mean of the betas?
	We get the mean by minimizing the error (the residuals). Because it will give the smallest difference from the mean x-xhat, which is as close at the mean as it can get-

What are the X of the second level?
	A column of one. This is to get the mean of the Betas (on the 2nd level)>0. But if you wanna compare 2 samples, then you need to compare 2 different means,  and you X them by a X = 10 subjects  * colum 2 means and  the Betas= 2betas * 10 subjects
Why do we have zeros and 1 here? 
	![[Pasted image 20220711132138.png]]
?? It depends, it could be any constrast rate like [1 -1] this will give us a ttest of c'B/ std(c'B) = B1 - B2 /std(B1-B2). Because  well, this is the contrast right?



## Random vs Fixed effects analysis
Its helpful if you have bad models on the first level. ex: The onsets of the lights are wrong (measure time points when there's no light)