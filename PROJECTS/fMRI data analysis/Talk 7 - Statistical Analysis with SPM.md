what the fuck is 2 sided difference? What are we exactly calculating with the f-test?
	- The f-test uses ANOVA to find if there's a diff between two populations
	- The f statistic doesn't care about the sign: It can't tell you if the difference is positive or negative
	- f-test compare the full model with the reduced model (without the B we want)
	- We have the variance of the BOLDr that's explained by the reduced model. Now, adding the different parameter, how much more variance is explained? (Variance because it will deviate from the standard HDR of as well)
 Relearn Full vs reduced matrix
 **What model has a higher variance?**
	The reduce model error is alwyas >= bc you need other parameter to reduce the variance
	e^2r >= e^2


**Here's the Aufgabe**
	![[Pasted image 20220701122749.png]]
	For the b, the contrast vector would be c = [ 1 1 -1 -1]
	ATTENTION: The c vector represent the gesamt 4 regressors, not all  condition. this means the above c means, we used a condition with those 4 regressors at the same B1 is the parameter of Light on, tone ON
	Question 3:
		The difference of the diffrence between TON LON - TONOFF LON  AND TON LOFF - TON LON has to be diff  from zero. In this case, that gives us the contrastfor the interaction effect.
**How do we make sure we don't filter our interesting frequencies (design matrix) because of the high pass filter**
	By choosing the frequency of repeting our signal (like Light ON) frequently enough not to fall in the noise frequencies. This is I think> 20sseconds
**What does the f-variance measure**
	The difference between variance estimates, to explain, how much did our conditions (Ligh, sound) can explain the variance of the BOLD signal
**How do you build a reduced model?**
How do we convolve a signal time point ? (Think one point with an intensity) into a Hemodynamic Signal.
	1. We  split the input into different intermediate signals (with diffre)
	2. You scale the intermediate inputs by the intensity of the input. 
	3. Let's say there's 3  intermediate input. THey all get assign a HDR funcion. So we have 3 HDR function, seperate by different time frame
	4. In the end, we just sum all of those intermediate response to have the shape of the final response
What problem do we run into while convolving HRF?
	1. We have to take long signal delay so that the HRF won't mix
	2. Serial Auto-correlation: Signal at any time point  can be prolonged to the subsequent time points, which increases the likelihood of obtaining false positives in task studies
	3. Correlated regressors because of movement
	4. Noise in the low frequency range bc of aliasing effect, below 0.02 Hz
What does covariance means? #unclear  

cWhat is the point of doing a Statistical Analysis of the BOLD RESPONSE?
	![[Pasted image 20220705084056.png]]
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
Why would we convolve the LTI to the X?  
	Because the neural activation of every voxel is always expressed in HRF. So if the Y changes because of a X.Beta(say, 0,3), it will always be express in the shape of the HRF
	
	![[Pasted image 20220705085447.png]]
What is autocorrelation?   
	In our case, its when the variance of a voxel, correlates with the variance of this voxel, but over time. This means, after 1s, the prob that the intensity of the e-errort and e-error-t-1 are similar is pretty high, meaning they autocorrelates. 
In our case, autocorrelation is not important because we consideror that the error values (that are not explained by the design matrix) are not correlated. The error is normaly distributed (gaussian)

Why do we add Ones columns to the  X design Matrix? #fmriquestion
	It's the intercept that models the offset
Why is there (mathematically) a large dependency between regressors? #unclear
	talking about regressors modelling the phsyical parameters like 6 heads
	If we change the x2 values, we will change the B2 value (so that the x2 and x1 are uncorrelated aka 90deg), but to predict the y vector we'll have to change the x1 as well. 
	![[Pasted image 20220701110708.png]]
questions: Why do we use Identity matrix for the e
whats kind of values are in the design matrix? For example?
Why is there noise in the low frequency range of our measured signal? #fmriquestion 
	Because the sampling rate is so low we cant detect high frequencyies. This creates a low frequency. Basically its due to: Aliasing and/or the way we sample data
How can we confirm our hypothesis that: Are there differences in neural activity between conditions
	Find if the BETA1 is larger than the BETA 2 (substract)
		NB: you need to use linear contrasts: ![[Pasted image 20220701121034.png]] #reformulate 
There's another point, a problem created during statistical analysis: Reducing noise in the low frequency range. What do we do for it?
	apply a high pass filter

#reformulate the contrast weights and how to measure conditions: Interaction effect
	![[photo_2022-07-06_15-03-48.jpg]]

What is a reduce model?
	
	![[photo_2022-07-06_15-17-56.jpg]] 
What are the 2 types of threshold?
		Extend threshold
		Height threshold
		What's the extend threshold? 
			It means we need a min of adjacent voxels with large t-values
		what is the height threshold? #unclear  
- f-test: We use it by creating a reduce model excluding the parameter of interest. Then, we can add em and see if they improve our model prediction (of the BOLDr) or not.  This mean, we see if the important parameters explain much of the variance in our model, or if the boring parameters (reduced) are also meaningfull

