What is the point of doing a Statistical Analysis of the BOLD RESPONSE?![[Pasted image 20220705084056.png]]
	Create a generative model: Predicts the BOLDr, given the experimental values (light ON, sound OFF)


X values comes from the design Matrix. But what is the design Matrix?
	The design matrix is a matrix containing the different conditions that we apply to the brain, expressed as value, that we then weight with the Beta parameter, to predict how much those conditions affects the brain activity aka the BOLDr. 
	The Design matrix contains in the 1st column the values of the experimental design
	![[Pasted image 20220705084850.png]]
	during the 84 blocks of time, we alternate OFF and ON auditory signal
	In the second column its for the dummies
	In the rest of them, it's the values of the different predictors Betas


What does LTI means?
	LInear time invariant model
Why would we convolve the LTI to the X? #reformulate 
	Because the neural activation of every voxel is always expressed in HRF. So if the Y changes because of a X.Beta(say, 0,3), it will always be express in the shape of the HRF
	
	![[Pasted image 20220705085447.png]]
What is autocorrelation? #unclear 
	In our case, its when the variance of a voxel, correlates with the variance of this voxel, but over time. This means, after 1s, the prob that the intensity of the e-errort and e-error-t-1 are similar is pretty high, meaning they autocorrelates. 
In our case, autocorrelation is not important because we consideror that the error values (that are not explained by the design matrix) are not correlated. 
**How does the epsilon error term relate to autocorrelation?**
The error is normaly distributed (gaussian)
**Why is serial auto-correlation a problem for modeling the BOLD signal HDR-response:**

### Talk 7: Part 2 Statistical Analysis

Why do we add Ones columns to the  X design Matrix? 

We convolve the HRF with the BOLD signal to get one column per conditions. #unclear (looks plain out false) Because it is. Mofo.

**How do we convolve a signal time point ? (Think one point with an intensity) into a Hemodynamic Signal.**
	1. We  split the input into different intermediate signals (with diffre)
	2. You scale the intermediate inputs by the intensity of the input. 
	3. Let's say there's 3  intermediate input. THey all get assign a HDR funcion. So we have 3 HDR function, seperate by different time frame
	4. In the end, we just sum all of those intermediate response to have the shaep of the final response

**Why is there (mathematically) a large dependency between regressors? #unclear** 
	If we change the x2 values, we will change the B2 value (so that the x2 and x1 are uncorrelated aka 90deg), but to predict the y vector we'll have to change the x1 as well. 
	![[Pasted image 20220701110708.png]]
questions: Why do we use Identity matrix for the e
whats kind of values are in the design matrix? For example?
**Why is correlated regressors a problem? #reformulate** 
	Because by avoiding large correlation in our design matrix we can avoid having to change all of the Xs and Betas?
	2. Ancova
What does covariance means? #unclear  

 Why do we have to do Convolution with  HRF?
	 Because even when we apply a short signal, we always get a long response 4-6 s and we have to model every signal as such

**How is correlated regressor a problem? #reformulate** 
	Because by applying a HRF conv. We created a correlation between the different regressors. 
	This create **multicolinearity**

Why is there noise in the low frequency range of our measured signal? #unclear
	Because the sampling rate is so low we cant detect high frequencyies. This creates a low frequency. Basically its due to: Aliasing and/or the way we sample data
How do we get rid of low frequency?
	By applying a high pass filter.
**How do we make sure we don't filter our interesting frequencies (design matrix) because of the high pass filter**
	By choosing the frequency of repeting our signal (like Light ON) frequently enough not to fall in the noise frequencies. This is I think> 72 seconds

How can we confirm our hypothesis that: Are there differences in neural activity between conditions
	Find if the BETA1 is larger than the BETA 2 (substract)
		NB: you need to use linear contrasts: ![[Pasted image 20220701121034.png]] #reformulate 


Here's the Aufgabe
	![[Pasted image 20220701122749.png]]
	For the b, the contrast vector would be c = [ 1 1 -1 -1]
	ATTENTION: The c vector represent the gesamt 4 regressors, not all  condition. this means the above c means, we used a condition with those 4 regressors at the same B1 is the parameter of Light on, tone ON
	Question 3:
		The difference of the diffrence between TON LON - TONOFF LON  AND TON LOFF - TON LON has to be diff  from zero. In this case, that gives us the contrastfor the interaction effect.


What arethe  3 types of problem created by applying a convolution to predict the HDR?
	- : Convolution with HRF I think, bc its difficult to model multiple signals. #unclear 
	- Serial Autocorrelation: related to the e
	- Correlated regressors: There's some variance shared between the B's regressors so that if the X1 changes, the B1 and B2 will be affected #unclear 
		- It can create multicolinearity. It can help to enlever signales related to movement. We use to do that, an ANCOVA,  where we add Betas related to the 6 movements, and remove the movements, from influencing the X

There's another point, a problem created during statistical analysis: Reducing noise in the low frequency range. What do we do for it?
	apply a high pass filter

What kind of questions we can ask to validate our hypothesis?
	Do one of our conditions increase Neural Act incomparison to other
	-





#reformulate the contrast weights and how to measure conditions: Interaction effect
FS1 isfemale face FS2 is male face OS1 is object in condition 1 and OS2 is object in condition2
	![[photo_2022-07-06_15-03-48.jpg]]

 Really take the time to go through that again. Check the MATLAB Reader #unclear  
What's the save in the constrast Image
	LC of the contrasts weights c and the Betas. cT.B
Why do we need contrasts image  
	Group analysis?
What is  a full model?
What is a reduce model?
	
	![[photo_2022-07-06_15-17-56.jpg]] 
What model has a higher variance?
	The reduce model error is alwyas >= bc you need other parameter to reduce the variance
	e^2r >= e^2

What does the f-variance measure
	the f contrast is 2 sided
	it calculates the diff between the variance estimates
	We loose the directions
	1 0 0 0 
	0 1 0 0
	0 0 1 0 By having this as DMatrix, we tryna see if any of the regressors  are able to reduce the error matrix. 
	The Ho would be that every B are = 0 , so no change in the basal activity B1... b1 = 0
	The H1 would be:

How do you build a reduced model?
	You assume that c'B=0.

You ran ttest for each voxels and found f values as well. But now, how to you define the t values or f values as large? #unclear (What are we trying to do)
	Determine a threshold
	What are the 2 types of threshold?
		Extend threshold
		Height threshold
		What's the extend threshold? 
			It means we need a min of adjacent voxels with large t-values
		what is the height threshold? #unclear  
What are the problem with these multiple comparions?
	That by change you can have a lot of significan but random error. 
	
What can be solutions to the Multiple comparisons comming from having so much tests run in voxels?
	Adapt the p value to the M.C = p= 0.5/100 = 0.005

If one voxel shows activation, there's a higher prob that the neighbour also are activated, so we can apply techniques on that. But what techx or what for

res = Y(:,1) - Y_pred;
![[Pasted image 20220708064157.png]]  contrast
the contrast vector is a vector that express that oppposes the weights of our differents conditions. This means it express how we can contrast Condition A with condition B, saying that (for ex), Condition A differs from condition B. If this is false, then the contrasted activity (difference in the HDr) will be 0, which will validate the null Ho. 
This can be rewrite in a linear comb so: cB1 - cB2 = 0 #excellent
We can use 2 types of statistics to find if  our conditions differs from each other:
- T-test: If we wanna find if two conditions have a different impact on the HDr or if we wanna see if a condition differs from baseline ex
	- ![[Pasted image 20220708065432.png]]
	- 
- f-test: We use it by creating a reduce model excluding the parameter of interest. Then, we can add em and see if they improve our model prediction (of the BOLDr) or not. 
- what the fuck is 2 sided difference? What are we exactly calculating with the f-test? 
	- The f statistic doesn't care about the sign: It can't tell you if the difference is positive or negative
	- f-test compare the full model with the reduced model (without the B we want)
	- We have thev ariance of the BOLDr that's explained by the reduced model. Now, adding the different parameter, how much more variance is explained? (Variance because it will deviate from the standard HDR of as well)