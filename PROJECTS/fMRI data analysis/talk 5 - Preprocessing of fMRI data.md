#fMRI
What are the 5 steps of data #preprocessing
	1 - Realignment 2 - Coregistration 3 - Segmentation 4 - Normalization 5 - Smoothing

### DICOM import
What  is a NIftI image? #unclear 
	an image ...
What are the 2 datas contained in the NiFItI image?
	header
	image data

Why should we discard the first seconds of acquire datas?
	Before preprocessing an fMRI data set, the fi rst images acquired in a session should be discarded. This is because much of the very large signal change that they contain is due to the time it takes for magnetisation to reach equilibrium. This can be easily seen by looking at the fi rst fe
### #realignment
In which cases do we use #realignment
	because heads movements can change the aligments of T2 images from each others
	After that we get the realignment parameters in a text file, with 6 colums 3 for translation , 3 for rotation
whats the "thing" we need to align T-images?
	reference image
how many parameters do we use and what are they
what procedure do we use to #realignment the images
	mean-squared difference
	motion correction algorithm


### coregistration  #coregistration
what's the point of coregistration?
		to match  the anatomical, more detailed T1 with the T2-iamges
		and then to wrap the fxn images into an unique, wokrs-on-every-images- template
how do coregistration actually works steps by steps
	step 1: Move the images around and test how to make anat and fxn #overlay 
**How do we achive maching the T1 and T2 images?**
	Because both are almost the same image with inverse brightness and dark area? ( may be because one meausre the pulse inversion and the other the desynchro and they both oppose each other #t2 #t1 #boldresponse) difference between the voxel so the thing is to find how the brights and dark voxels works #unclear
step 2: How do we map the T2 into the MNI template 
	We overlay the T1 to MNI-template first, then to the mean of the T2
What happen if we directly map the T2 images with the template? #unclear
	May be there's not enough resolution to accurately match it out?
**Why do we keep the mean of T2 constant but align the T1 to it.  #coregistration** 
	we only have 1 T1 image, if we change the mean, we have to change all the functional images from the time series (mre, but if we change the T1, its just "one change" #overlay 
	


[[Talk5 - preprocessing#coregistation]]



### segmentation
#segmentation
	**why would anyone segment datas?**
		*to better align brains from differents people*'s data
		helps normalizing? the anatomical image #t1 
	how does segmentation works?
		they classify voexls in differents tissues types like grey and white matters.
		

### normalization
 #lineartransformation
what kind of maths operation do we do with normalization?
	linear and non linear(warping) trasformation
what for?
	to put the HD t1 image to the MNI template

### Smoothing
**why would we smooth?** 
It increases overlapping of brain areas btwn subjects.
		Thus diminishing the chances we misrepresent a gyrus to the Erinal cortex which increases stat. significance
To revmove noise, increase SNR: It makes noises/errors more normally distributed because within data many signals vary
We use a gaussian fxn to blur out and smooth outh the BOLD signal so tha tthe strongest bolds appear and the noise (that doesnt occurs often ) fade out.
We use 8mm in the gaussian smoothing fxn
What's the effect of smoothing on resolution?
	Decreases it?

[[fMRI data analysis]]

