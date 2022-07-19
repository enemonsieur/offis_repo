---
ANOVA MODELS: 
alias:  (ID questions/Blocks) (Summarize/Answer) (Revise 1-2-3) (Mindmap) 
---
 
 What are continuous covariates?
How does different contrast affect the interpretation of an ANOVA model?
page 6 : what happen is that for each subject, we wanna see how much variance is explained by each parameter
One way ANOVA explain how similar each group are between is other g1 -g2 g2-g3 g3-g1


We can run ANOVA within the second level design
or each values there are offste, different effects differences like Alpha (low vs high lights) Neta (tones, silent, light, midlle etc..) and gammaij, that represents the interactions. 

In the design matrixi in page 4 we ca have a design matrix that contrasts all of those conditions. They model the interactions. 
- What is small k here=n
- The 2nd and 3 column model the alpha 1or 2 for example. 
On the 2nd level, diferent design matrix can model the same effect. 

When is a matrix rank definicient?
What happen is fhhe matrix is rank deficient?
	Has in infinite number of solutions
How can we turn a rank def. matrix into full rank?
	We can sum them up p.10
p11. Why is it not rank definiient?
	Bc we can use the colim 1 2 to redict the re rest?
find a 2 number a +b =4- A lot of solutions right?

page 14.

Some parameters are uniquely definie. Can we combine X design matrix by a matrix T, so that we definde a function that estimate the model parameters.

The contrast vector ca be estimal,e, have 1 solution or define solutions, if it can be repreent as a linear combi of the rows of X. p15
In this big matrix there are many Beta estiamteives that measure different interactions. But if qwe wanna find th ediffernece betqeen A1 and A2 in general,, we have to combine the different rowns of the design matrix to correct the main efect of A (look again)

If it's not estimable, there'd be a grey box. at the level of the column 

The Dmatrix are often overparameterize bc they don't have full ranks, bc we can predict a colum with the param of others. In this case we can't inverse the matrix, and can't apply the formula tu find the exact B-estimates. 
We can use the pseudoinverse, but the model wont be uniquely estimated. 

On the other side certains contrasts are estimable, when we can combine the diff. rows of the DM to get the constrasts rate to find wtf you wnat. 
In this case, the SPM will be gray where the Betas aren't estimable. 

## To know: 
Thinkabout the sANOVA design matrixes anre understad them, like the OW ANOVA, the first five. Understand what the betas are estimating? Which contrast are you selcting?
-What happen if the matrix have full rank?
Havent full rank.