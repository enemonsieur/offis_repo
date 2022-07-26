---
ANOVA MODELS: 
alias:   (Summarize/Answer) (Revise 1-2-3) (Mindmap) 
---
-  **On what factor do the beta values depend on in the 2nd level analysis ?**
	When the  matrix is overparameterize this leads to depencies, so its not full rank.  So there's not unique solutions to the Betas
 What are continuous covariates?
	 covariate that can be 1 0.5 3.4 etc...
 

When is a matrix rank deficient?
	When it has an infinite number of solutions, which happens when its column aren't colinear.
What happen is the matrix is rank deficient?
	Has in infinite number of solutions
How can we turn a rank def. matrix into full rank?
	We can sum them up p.10
 number a +b =4- A lot of solutions right?

page 14.

Some parameters are uniquely definie. Can we combine X design matrix by a matrix T, so that we definde a function that estimate the model parameters.

What is the condition to be able to find a contrast vector?
	If it can be express as a LC of the rows of X
	Can we obtain it, by combining the --> of X?
In this big matrix there are many Beta estiamteives that measure different interactions. But if  we wanna find th ediffernece betqeen A1 and A2 in general,, we have to combine the different rowns of the design matrix to correct the main efect of A (look again)

In SPM, what happen if the contrast vector isn't estimable?
	If it's not estimable, there'd be a grey box. at the level of the column 

The Dmatrix are often overparameterize bc they don't have full ranks, bc we can predict a colum with the param of others. In this case we can't inverse the matrix, and can't apply the formula tu find the exact B-estimates. 
We can use the pseudoinverse, but the model wont be uniquely estimated. 

On the other side certains contrasts are estimable, when we can combine the diff. rows of the DM to get the constrasts rate to find wtf you wnat. 
In this case, the SPM will be gray where the Betas aren't estimable. 

## To know: 
Thinkabout the sANOVA design matrixes are understnad them, like the OW ANOVA, the first five. Understand what the betas are estimating? Which contrast are you selecting?
	-What happen if the matrix have full rank?+
		Theres an unique solution
Havent full rank.
	Xb 1 = Xb 2 with b 1≠ b 2 (different parameters).
	 • The parameters are not therefore ‘unique’, ‘identifiable’ or ‘estimable’. 
	 • For such models, XTX is not invertible so we must resort to generalised inverses (SPM uses the pseudo-inverse).
How do we call the column of ones in ANOVA? (Not dummies)
	Offsets

![[Pasted image 20220719194133.png]]
	Why does La-b uses zeros on the offset, but the rest consider the offset
		bc we are only interested in diff in activation?
What does having a full rank means in term of matrix colums?
	That some colums can be recreated by a LC of others
What's an overparametized function?
How can we find the solutions if the matrix X isnt full rank?
	We use pseudo inverse, bc it's not invertible
How does invertible/rank matrix affects our **Contrast Matrix?**
	Because we can only interpret it if it's the LC or made of the LC of the ---> of the Design matrix X
What does the unicity of the X solution means in term of C and T matrix?
	That there's only one T matrix that * by X gives the C marix
How do SPM analysis signal a non invertible matrix?
	Appears gray

#fmriquestion 
- The Betas have to be uniquely definie. I f they means mutluple things, then you can't gueess what they mean. 
- What about the contrasts matrix? How do they have to be? 
- Which contrasts are uniquely defined?
	- The SPM does that shit alone. And estimate it or not. 
	- Why are only certain contrasts estimatable? Some of them but no all of them
- f-test: Full and reduced model. 