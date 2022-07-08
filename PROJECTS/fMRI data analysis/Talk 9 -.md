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
	 The problem is that it'll create a lot of FN (because it cuts too low, it demands a very high ttest to say: Yees, this isnt done )