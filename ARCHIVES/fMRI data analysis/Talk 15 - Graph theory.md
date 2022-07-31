**1. Why do we do slice timing?**
**2. Why are movement correction important for defining links in graph theory?**
	- bc movements affect long distance corr in Physical space - they reduce those corr. But increase the corr. between brain region that are closed increase
	- Therefore you should add parm. to check the mvmt parameters. computing framewise displacement (the mvmt parameters) and DVARDS (take the images, make a Root mean squared, and if there's a large change that means, there's more movement in the change of our Betas/Analysis... basically you're fucked.)
	- Delete the images that are really affected by noise (pretty violent)
	- Interpolate the data point affected by noise: Use ICA-AROMA (P14)

3. Why do we parcelate the brain in different Brain regions
	   - To get mean time series of those regions. 
	   - They use a low pass filter and focus on frequencies componetnts below 0.1 Hz. Which is surprising bc we are supposed to recieve a lot of noise in the low-pass filter.
	   - This is bc long range autocorrelation, low freq autocorr. isn't just noise. ex: herzt coefficient?
	   - This means, we use LPF to take the information about long range communication, to see if neural networks communicate between each other. 
- We can use a pearson correlation to find the regions by regions connectivity matrix, and by changing the threshold, we can find the connections between the brain graphs.

4. Why do we parcelate the brain again? (into mean time series)
	1. To reduce the data space
But how do we do that?
		- We use anatomical landmarks ex(we know where the gyri is) = **anatomical parcelation**. To do so, weuse the anatomical labelling of activations.
		- More recently: **functional parcelation** the parcels have differents volumes and sizes, and there's a corr btwen volume size <-> Mutual information?The higher the volume, the higher the correlation. 
		- But why bigger regions correlates with other regions?
			Many voxels averaged reduce the noise, so the t-series is less effected bynoise, so its more likely to find corr with brain areas (since noise has zero corr, the bigger area, the lesser noise, the higher the correlation with other stuff )
How do we definie the edges/notes using functionnal connectivity?
	We turn time series into F.bands, and we compare eacht T-Series in each frequency ranges with a connectivity matrix (using for ex. The pearson correlation)

	
How do functional parcellation works?
	it doesn't limits to the anomtical parts.
What's the problem that arise with fxn connectivity
	inderect correlation P.10
How do we correct that?
	Use partial correlation. By taking only the residuals between the correlation btwn regions to find the correlation, so that will eliminate the indirect correlation. 
		PS: I didn't get SHIT!
What's the problem with partial correlation?
	- Bc it can force two ID nodes to become correlated: Berkson's paradox. 
	p.11
	- This can create a very high correlation  #unclear 
**What is DERIVING DIRECTIONALITY?**
	It's an equation to predict the future of one signal X2, using information of the past of another signal X1
	Created by Granger-causaliting, originally about the stock prices. 
	If we wanna predict X1 at time t, we have to go backward in the timeseries, and predict X1, but we can also use the inormation of X2 in the past to predict it. (Check the p.12)
What's impossible to do with Granger causality
	The past can predict the future, but not the contrary. 


Now how are links defined?
**How to compute **time resolved analysis****
	Use a certain sliding window and just shift tha tshit ofter time to compute thte fcn connectivity of this time windows

How are the resting state networks related to taks network?

Structural and fxn connectivity:
What are the models of fxn connectivity

----
# Capital importance
ANOVA models. #fmriquestion 
How to investigate the main effects in multiple condtions? 
Where in the brain is there more activation of cars vs flowers? 
 CarB CarR FlowerB FlowerR
 1        0       0              0
 0        1       0              0
 etc...
 
 1 1 -1-1 is cars - flowers activations
 