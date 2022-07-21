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
	The 
	The become the B-weighteds, that we found by analysing every subjects in the first level
		it represent the  contrast image of different subjects.
		for each subjec we have their Sm, which represent the  Y of the 2nd level analysis.. so that we have Subject m = c1 * B1,m + cnBn,m
	In Y 2nd level, we redo a ttest=  cB/std(cB). caö dB d- And we wanna know where's the mean difference larger than zero
	The 



Then we wanna minimise the betas that we found from each subjects so that we have a mean of
What are the dimensions of Y
	they have numbers, representing different participants. And the d2 is 1 because we find the weighted sum of all the Beta so we have 1,n(subjects). This isjust for one voexels right??

What's the lenght of the C vector ?
	Just one because we estimatejust one betas in the 2nd level

What are one and two sample t-test for 2nd Level?

How do we get the mean of the betas?
	We get the mean by minimizing the error (the residuals). Because it will give the smallest difference from the mean x-xhat, which is as close at the mean as it can get-

What are the X of the second level?
	X is just A column of one, bc we get the mean of the Betas (on the 2nd level)>0.
	This means the Betas are the means over c'B of the first level ex: The =/= unknown and known level?
	But if you wanna compare 2 samples, then you need to compare 2 different means,  and you X them by a X = 10 subjects  * colum 2 means and  the Betas= 2betas * 10 subjects
Why do we have zeros and 1 here? 
	![[Pasted image 20220711132138.png]]
?? It depends, it could be any constrast rate like [1 -1] this will give us a ttest of c'B/ std(c'B) = B1 - B2 /std(B1-B2). Because  well, this is the contrast right?




Region of interest Masks
When are they usefull?
	When we are only interested in a region of the brain. 
What kind  of p-value correction don't work well with that?
	RFT bc they need a large surface to be applied
Statistical Power computation


What if the c' contrast we took for the second level is actually -1?
	Because the mean would be just the mean of the diffferents B1-B2 (to contrast the ttest) for evety suject, reversing it will just reverse the Betas to B2-B1. 
	It'D stille give the same number, -2,3 or 2.3 just now we are contrasting the LIGHT ON versus OFF instead of Light OFF vs ON.
When we find the means B1 B2 at seocnd level, representting the two groups, we can take the constrast level to test the diferent between the groups by using the contrast level: c = [1 -1] or the reverse.