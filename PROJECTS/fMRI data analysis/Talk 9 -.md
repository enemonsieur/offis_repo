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
	 We take into account the internal and external smooething

Random Field Theory p-value correction
	Estimates the smoothness of your  t-image. Its used to figue out, what "filter" was used to smooth your imaged.
	The more the filter increases? the more the corr happens on a longer distances and the smaller the p value increase. A very smooth data means a very small correction or so. 
	R is the Reso volume? the volume of the brain, than we calculate / smoothing function. To determine how smooth or correlated or dependent our data are. If its already pretty smooth, you won't have to correct the p value. 
	The smaller the smoothness the bigger the p-value will be transform
  
False discovery rate
	Has to do with this false positive and negative
	R is the total of FP and TP
	We say, 5% of the voxels we measue are wrongly declared as FP
