---
alias: Factorial design
---
## Random vs Fixed effects analysis
Its helpful if you have bad models on the first level. ex: The onsets of the lights are wrong (measure time points when there's no light).

Does the error from the 1st level has an effect on the 2nd level? 
	(surely it does) -- the var on the 2nd level is a mixture of withing + between subject var. 
	![[Pasted image 20220711133913.png]]

What is random effect models?
	The influence of the var in the 1st and 2nd levels on the distribution of the population

What are the contrasts rate and contrast images?
What is the contrast vector?
	A linear combination of the regressors
What's the first level analysis?
	It's using the regression model to model the response of the OLD signal, using our Conditions in the design matrix and measuring their influences with the Regressor vector 
What's the second level analysis?
	It's modeling the difference in brain activations levels (ttest) when having different groups. In this case, the regressors model the mean activation of the groups
		![[Pasted image 20220711125716.png]]



What's Y in the 2nd level?
	The contrast images/values of every subject, obtained by contrasting certain parameters.

What does Beta at the second level represents?
	Since the Y is the ttest of every subject, we need a way to model their average response. With X DMatrix =ones, we can find a unique Beta, that models the average response of the subjects, which is the mean of the Y's
How do we find the ttest in the first level?

Then we wanna minimize the betas that we found from each subjects so that we have a mean of


Why do we have zeros and 1 here? 
	![[Pasted image 20220711132138.png]]
	In this matrix we have two groups of participants,with different conditions. That means we need 2 Betas, one to model the first group, the second the others
What kind of contrast do we apply in to find the different in activation between 2 groups?
	 c = [1 -1] a ttest of c'B/ std(c'B) = B1 - B2 /std(B1-B2), to find the difference between the 2 groups.


Region of interest Masks
When are they usefull?
	When we are only interested in a region of the brain. 
What kind  of p-value correction don't work well with that?
	RFT bc they need a large surface to be applied
Statistical Power computation


What if the c' contrast we took for the second level is actually -1?
	Because the mean would be just the mean of the diffferents B1-B2 (to contrast the ttest) for evety suject, reversing it will just reverse the Betas to B2-B1. 
	It'D stille give the same number, -2,3 or 2.3 just now we are contrasting the LIGHT ON versus OFF instead of Light OFF vs ON.
