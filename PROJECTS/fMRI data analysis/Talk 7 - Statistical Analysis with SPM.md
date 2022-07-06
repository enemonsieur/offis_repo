What is the point of doing a Statistical Analysis of the BOLD RESPONSE?![[Pasted image 20220705084056.png]]
	Create a generative model: Predicts the BOLDr, given the experimental values (light ON, sound OFF)


X values comes from the design Matrix. BUt what is the design Matrix?
	The Design matrix contains in the 1st column the values of the experimental design
	![[Pasted image 20220705084850.png]]
	during the 84 blocks of time, we alternate OFF and ON auditory signal
	In the second column its for the dummies
	In the rest of them, it's the values of the different predictors Betas
We perform analysis for each voxels, not of all. So that for every voxel, we have the entire BOLD response measure in Y, of lenght (N). This length correspond to the number of slices that we had.  which obviously can't be too small. (May be a slide every 0.5s)

What does X, Y and B represents?
	![[Pasted image 20220629150856.png]] #unclear 


What does those regression coeff mean? Betas #reformulate
	what we know is that we need the X(n,p), the part of the BOLD signal that vary because of one particular factor (may be when presented blue or light. Those Xnp when changing because of the weight Beta 


Why would we convolve the LTI to the X? #reformulate 
	We can thus improve our prediction by modifying the box car stimulus function of Fig. 6.10a to take into account the shape of the HRF. This is done through convolution, by assuming a **linear time-invariant model.** This convolution operation is conceptually the same as the one that was used in the smoothing preprocessing step; that was a convolution in space with a Gaussian kernel, whilst here it is a convolution in time with the canonical HRF. The output of this mathematical operation is displayed in Fig
	![[Pasted image 20220705085447.png]]
What is autocorrelation? #unclear 
	In our case, autocorrelation is not important because we consideror the error values (that are not explained by the design matrix) are not correlated. But in general, they represent 
How does the epsilon error term relate to autocorrelation?
	the error is normaly distributed (gaussian)
	Why is serial auto-correlation a problem for modeling the BOLD signal HDR-response: #unclear The error we get fron the model, epsilon, isn't random. It's autocorrelated with the time delay, eith the previous time steps signla.


### Talk 7: Part 2 Statistical Analysis

Why do we add Ones columns to the  X design Matrix? #unclear 
	In case of a single subject analysis

What are the two dimensions of the X design Matrix?
	The row dimension (n) is the time vector function 
	The column dimension (p) contains the differents experimental design data like sound activated, or light on that influence the intensity of the BOL signal
We convolve the HRF with the BOLD signal to get one column per conditions. #reformulate 

During the convolution, what is LTI? 
	![[Pasted image 20220701103125.png]]
	It's the algorithm that we use, to transform a one time signal like (light ON for 10ms) into the BOLDr/HDR that he will create
How do we convolve a signal time point ? (Think one point with an intensity) into a Hemodynamic Signal.
	1. We  split the input into different intermediate signals (with diffre)
	2. You scale the intermediate inputs by the intensity of the input. 
	3. Let's say there's 3  intermediate input. THey all get assign a HDR funcion. So we have 3 HDR function, seperate by different time frame
	4. In the end, we just sum all of those intermediate response to have the shaep of the final response

WHat's a block design #unclear
	Stimuli are rpesnetend after each other ex: 20 times at a particular condition (A) #unnecessary 

Why is there (mathematically) a large dependency between regressors? #unclear 
	If we change the x2 values, we will change the B2 value (so that the x2 and x1 are uncorrelated aka 90deg), but to predict the y vector we'll have to change the x1 as well. 
	![[Pasted image 20220701110708.png]]
questions: Why do we use Identity matrix for the e
whats kind of values are in the design matrix? For example?
Why is correlated regressors a problem? #reformulate 
	Because by avoiding large correlation in our design matrix we can avoid having to change all of the Xs and Betas?
	2. Ancova
What does covariance means? #unclear  

 Why do we have to do Convolution with  HRF?
	 Because even when we apply a short signal, we always get a long response 4-6 s and we have to model every signal as such

How is correlated regressor a problem? #reformulate 
	Because by applying a HRF conv. We created a correlation between the different regressors. 
	This create **multicolinearity**

Why is there noise in the low frequency range of our measured signal? #unclear
	Because the sampling rate is so low we cant detect high frequencyies. This creates a low frequency. Basically its due to: Aliasing and/or the way we sample data
How do we get rid of low frequency?
	By applying a high pass filter.
How do we make sure we don't filter our intersting frequencies (design matrix) because of the high pass filter
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
	Do one of our conditions increase Neural act incomparison to other
	-

What's the point of using contrast to meausre hypothesis?
	We express the hypothesis via an equation, and every condition than we changed, (for example the lights on or off or the song on or OFF), can be assigned a  contrast c:
	 c1 . β1 + c2 . β2 + . . . + cn . βn
	There's as much betas as there's distance p on the column

Is B1>0 what does this Ho  represents in englis?
	Is NA increased during on te the experiment?
If all the Betas except B1 have a c of zero :  If contrast: (+1) . β1 + 0 . β2 = β1, 
Ho is B1<= 0: If the weight of the first condition, that we're changing (say light) is inferior or equal to zero, that means NA is not increased. 
But if It's >0, then there's a signal increased in comparison to the baseline (the baseline is in this case, zero)

*If you wanna compare 2 conditions, you put the 1st and 2nd Betas of the conditions with opposite contrasts: -1 and 1. So that you get a Ho of: H0 : β1 - β2 ≤ 0 
H1 : β1 - β2 > 0*

#reformulate the contrast weights and how to measure conditions: Interaction effect
FS1 isfemale face FS2 is male face OS1 is object in condition 1 and OS2 is object in condition2
	![[photo_2022-07-06_15-03-48.jpg]]

# Really take the time to go through that again. Check the MATLAB Reader #unclear  
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

What does the f variance measure
	the f contrast is 2 sides
	it calculate the diff between the variance estimates
	We loose the directions
	1 0 0 0 
	0 1 0 0
	0 0 1 0 By having this as DMatrix, we tryna see if any of the regressors  are able to reduce the error matrix. 
	The Ho would be that every B are = 0 , so no change in the basal activity B1... b1 = 0
	The H1 would be:

How do you build a reduced model?
	You assume that c'B=0.

You ran ttest for each voxels and found f values as well. But now, how to you define the t values or f values as large?
	Determine a threshold
	What arethe 2 types of threshold?
		Extend
		Height threshold
		What's the extend? 
			It means we need a min of adj voxels with large t values
		what is the height threshold? 
What are the problem with these multiple comparions?
	That by change you can have a lot of significan but random error. 
	
What can be solutions to te Multiple comparisons comming from having so much tests run in voxels?
	Adapt the p value to the M.C = p= 0.5/100 = 0.005

If one voxel shows activation, there's a higher prob that the neighbour also are activated, so we can apply techniques on that. But what techx or what for