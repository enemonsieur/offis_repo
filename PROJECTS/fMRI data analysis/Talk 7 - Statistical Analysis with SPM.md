What is the point of doing a Statistical Analysis of the BOLD RESPONSE?![[Pasted image 20220705084056.png]]
	Create a generative model: Predicts the BOLDr, given the experimental values (light ON, sound OFF)
How do we design a 
What are Betas in the  MAtrix format? (with lenght  p)
X values comes from the design Matrix. BUt what is the design Matrix?
	The Design matrix contains in the 1st column the values of the experimental design
	![[Pasted image 20220705084850.png]]
	during the 84 blocks of time, we alternate OFF and ON auditory signal
	In the second column its for the dummies
	In the rest of them, it's the values of the different predictors
We perform analysis for each voxels, not of all. So that for every voxel, we have the entire BOLD response measure in Y, of lenght (N). This length correspond to the number of sllices that we had.  which obviously can't be too small. (May be a slide every 0.5s)

What does X, Y and B represents?
	![[Pasted image 20220629150856.png]]


What does those regression coeff mean? Betas
	hat we know is that we need the X(n,p), the part of the BOLD signal that vary because of one particular factor (may be when presented blue or light. Those Xnp when changing because of the weight Beta 

How is HDR to linear time-invariant (LTI)

Why would we convolve the LTI to ?? to predict the output of the voxel-brain aka HDR? #unclear 
What is autocorrelation? #unclear 
	It's about the fact the previous measure can predict the next one?
	can we predict time-(t) by time (t-1)
How does the epsilon error term relate to autocorrelation?
	the error is normaly distributed (gaussian)
Why is serial auto-correlation a problem for modeling the BOLD signal HDR-response: #unclear 

	The error we get fron the model, epsilon, isn't random. It's autocorrelated with the time delay, eith the previous time steps signla.


### Talk 7: Part 2 Statistical Analysis

Why do we add Ones columns to the  X design Matrix?
	In case of a single subject analysis

What are the two dimensions of the X design Matrix?
	The row dimension (n) is the time vector function 
	The column dimension (p) contains the parameter that influence the intensity of the BOL signal
We convolve the HRF with the BOLD signal to get one column per conditions. 

During the convolution, what is LTI? #unclear
	![[Pasted image 20220701103125.png]]

How do we convolve a signal time point ? (Think one point with an intensity) into a Hemodynamic Signal.
	1. We  split the input into different intermediate signals (with diffre)
	2. You scale the intermediate inputs by the intensity of the input. 
	3. Let's say there's 3  intermediate input. THey all get assign a HDR funcion. So we have 3 HDR function, seperate by different time frame
	4. In the end, we just sum all of those intermediate response to have the shaep of the final response

Why do the X design matrix stay consistent through out different voxels, why is that, that different Voxel still have the same X design matrix? Does the B values of the X matrix don't change at all with different voxels? What kind of values are contained in the X-design matrix and especially in the Beta dimension
WHat's a block design
	Stimuli are rpesnetend after each other ex: 20 times at a particular condition (A) #unnecessary 

Why is there (mathematically) a large dependency between regressors?
	If we change the x2 values, we will change the B2 value (so that the x2 and x1 are uncorrelated aka 90deg), but to predict the y vector we'll have to change the x1 as well. 
	![[Pasted image 20220701110708.png]]
questions: Why do we use Identity matrix for the e
whats kind of values are in the design matrix? For example?
Why is correlated regressors a problem?
	Because by avoiding large correlation in our design matrix we can avoid having to change all of the Xs and Betas?
	2. Ancova
What does covariance means?

 Why do we have to do Convolution with  HRF?
	 Because even when we apply a short signal, we always get a long response 4-6 s and we have to model every signal as such
Why is autocorrelation a problem to model our datas?
How is correlated regressor a problem?
	Because by applying a HRF conv. We created a correlation between the different regressors. 
	This create **multicolinearity**
But why do ANCOVA, and modeling datas helps getting read of **correlated regressor**?
Why is there noise in the low frequency range of our measured signal? #unclear
	Because the sampling rate is so low we cant detect high frequencyies. This creates a low frequency. Basically its due to: Aliasing and/or the way we sample data
How do we get rid of low frequency?
	By applying a high pass filter.
How do we make sure we don't filter our inteersting frequencies (design matrix) because of the high pass filter

How can we confirm our hypothesis that: Are there differences in neural activity between conditions
	Find if the BETA1 is larger than the BETA 2 (substract)
		NB: you need to use linear contrasts: ![[Pasted image 20220701121034.png]]
Are there signiticant differentce between the 2 conditions?
	Use a t-test

Brain activation during LON is largent than during LOFF
	You have to see all of the regressors in a design matrix:
		x1 = 1 (ligth on) x2= -1 x3 = 1 (tone off) x4 = -1
	then you just add all of them 
Here's the Aufgabe
	![[Pasted image 20220701122749.png]]
	For the b, the contrast vector would be c = [ 1 1 -1 -1]
	ATTENTION: The c vector represent the gesamt 4 regressors, not all  condition. this means the above c means, we used a condition with those 4 regressors at the same B1 is the parameter of Light on, tone ON
	Question 3:
		The difference of the diffrence between TON LON - TONOFF LON  AND TON LOFF - TON LON has to be diff  from zero. In this case, that gives us the contrastfor the interaction effect.