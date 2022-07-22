1. Why do we do slice timing? 
2. Why do we parcelate the brain in different Brain regions
	   - To get mean time seriies of those regions. 
	   - They use a low pass filter and focus on frequencies componetnts below 0.1 Hz. Which is surprising bc we are supposed to recieve a lot of noise in the low-pass filter.
	   - This is bc long range autocorrelation, low freq autocorr. isn't just noise. ex: herzt coefficient?
- We can use a pearson correlation to find the regions by regions cnnectivity matrix, and by changing the threshold, we can find the connections between the brain graphs.
3. How do we model nodes and edges?
4. Why do we parcelate the brain again? (into mean time series)
	1. To reduce the data space
	2. But how do we do that?
		1. We use anatomical landmarks ex(we know where the gyri is) = **anatomical parcelation**. To do so, weuse the anatomical labelling of activations.
		2. More recently: **functional parcelation** the parcels have differents volumes and sizes, and there's a corr btwen volume size <-> Mutual information?The higher the volume, the higher the correlation. 