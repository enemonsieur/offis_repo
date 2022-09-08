https://mne.tools/dev/auto_tutorials/preprocessing/70_fnirs_processing.html

1. Preprocessing files
source: https://github.com/smburns47/analyzingfNIRS/tree/master/demo_data
- Extract NIR data
- removing bad channels : 
- convert to nirs format
- Filter pipeline

2. ML (is it data analysis, is there a step between preprocessing and ML analysis?)
source: https://github.com/zm6148/fNIRS_data_analysis/blob/master/fNIRS_ML.ipynb
- calculate accuracy
- prepare training and testing data sets
- Apply 3 differents ML methods
	- SVM
	- DT
	- NN
- Fit the data with fit generator
- Visualize classification using 3D projection of the top 3 PCA components