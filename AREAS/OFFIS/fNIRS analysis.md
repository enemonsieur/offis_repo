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
- Fit the data with **fit generator**
- Visualize classification using 3D projection of the top 3 PCA components

2. MATLAB Preprocessing
	1. Found infos on github 
	2. Download Homer2 and  Inpaint as adviced
	3. Problem with Homer2. Can't launch the program
	4. Download MATLAB runtime as required (7GB)
	5. Still don't work
	6. Try dowload Homer3 (Looks like its well supported by admins)
	7. Apparently Runtime didn't work because the latest version wasn't supported by Homer3. Trying with version 2017
# DATA PREPROCESSING ACCORDING TO: 
https://www.researchgate.net/publication/356726823_What_Does_Sleeping_Brain_Tell_About_Stress_A_Pilot_Functional_Near-Infrared_Spectroscopy_Study_Into_Stress-Related_Cortical_Hemodynamic_Features_During_Sleep
3.1 Data Preprocessing
We exported data from all the devices and instruments forpreprocessing. Stress data and Fitbit data were aggregated at a1-day resolution (i.e., one data point for each day during theexperiment period). The perceived stress data were exported fromthe HealthLog app into a CSV file with a premium accountsubscription. Fitbit data of sleep, heart rate, and breath rate wereexported using a web app that we developed in our previous study(Liang et al., 2016). All these data were then merged by matchingdate stamps.The fNIRS data were collected at a high sampling rate of 50 Hzand required more complex preprocessing. The total raw signalsmeasured by the Brite 24 consist of several components, and theΔO2Hb and ΔHHb related to neural activity is only a smallportion. Noisy components are those related to breath, heartbeat,and movement, which need to be removed (Tak and Ye, 2014).The fNIRS data preprocessing pipeline is illustrated in Figure 3.
1) **Export raw OD signals.** Using the OxySoft, we exported rawOD signals in EDF format so that they were semi-compatiblewith the data formats supported by the MNE-NIRS Pythonlibrary (Luke et al., 2021). Although the OxySoft also allowsthe export of ΔO2Hb and ΔHHb signals that have beenconverted from raw OD signals, unfortunately the Artinisformat of these signals is not supported by the MNE-NIRSlibrary at the time of this study. It is worth noting that the MNE-NIRS library read in the EDF data as EEG signals bydefault; hence, additional processing was needed to conver tthe signal type to fNIRS after loading EDF files using the MNE-NIRS library.
2) **Trim the signals.** Since we were only interested in the first sleepcycle, we discarded the signal segments before the sleep starttime and after the first sleep cycle. The sleep start time asrecorded by the Fitbit Sense was used as the start time (Ts) ofthe effective data. The end time (Te) of the effective data wereset to Te  Ts + 90 min as the average sleep cycle of healthyadults is 90 min (Feinberg and Floyd, 1979).
3) **Remove channels with poor signal quality.** The quality of theOD signals could be compromised by many factors during themeasurement. While the OxySoft allows real-time inspection of signal quality, it does not provide computational tools toremove channels with poor signals. In our data preprocessingpipeline, we removed channels with poor signal quality usingthe Scalp Coupling Index (SCI) method (Pollonini et al.,2014). We first performed channel-wise filtering on the ODsignals at both wavelengths using a band-pass filter(0.7–1.5 Hz) to preserve only the heartbeat components.The resulting signals were normalized to balance anydifference between their amplitudes. The zero-lag cross-correlation between the resulting signals of the samechannel—defined as the SCI—was computed and used as aquantitative measure of the signal-to-noise ratio of thechannel. Channels with an SCI-value below 0.75 wereregarded as poor channels and were removed from thesubsequent analysis.
4) **Transform OD to ΔO2Hb and ΔHHb.** The modifiedBeer–Lambert law (MBLL) was applied to convert the ODsignals to ΔO2Hb and ΔHHb signals (Delpy et al., 1988). Asshown in Eq. 1, εO2HB(λi) and εHHB(λi) are the extinctioncoefficients of O2Hb and HHb at wavelength of λi,respectively. L denotes the interoptode distance. PPF(λi)denotes the partial pathlength factor, which represents thesensitivity of the measured optical density to the hemoglobinconcentration change in a focal region (Steinbrink et al.,2001). In this study, L and PPF(λi) were set to 0.03 and 0.1(Strangman et al., 2014).ΔOD λi( )  εO2HB λi( )ΔO2HB + εHHB λi( )ΔHHB[ ] × L × PPF λi( ).(1)
5) **Filter out physiological systemic responses.** The hemodynamicresponse due to neural activity has frequency contentpredominantly below 0.5 Hz (in many cases around0.1 Hz). The ΔO2Hb and ΔHHb signals were band-passfiltered to remove cardiac and respiratory noise. Accordingto the Fitbit data, the subject typically had a breath and heartrate between 11–13 bmp and 55–80 bmp, respectively, duringsleep. Hence, the cutoff frequency of the band-pass filter wasset to 0.02–0.18 Hz.
6) **Remove motion artifacts.** Although fNIRS is considered moreresilient to motion artifacts than EEG, abrupt head motionsuch as tossing and turning in sleep may still induce spikesthat contaminate the true cortical hemodynamic signals. Weused the correlation based signal improvement (CBSI)method (Cui et al., 2010) for motion artifacts removal.This method is based on the observation that the ΔO2Hband ΔHHb signals, which are typically strongly negativelycorrelated, will become more positively correlated whencontaminated with motion artifacts. Correspondingly, theCBSI method removes motion artifact through recoveringthe negative correlation between the ΔO2Hb and ΔHHbsignals.
7) Compute epoch-wise average. The effective data of eachmeasurement trial spanned over 90 min (generating270,000 data points each night). The duration wassignificantly longer than that of traditional fNIRS studieswhere a measurement is usually at the scale of severalminutes. To efficiently analyze such huge amount of data,we averaged the cleaned ΔO2Hb and ΔHHb signals epoch-by-epoch at a 30-s interval. Each epoch contains 1,500 datapoints. This step was compliant with the standardprocedure for sleep analysis (Iber et al., 2017). The outputtime series signals are denoted as {Xn: n  1, . . . , N} whereN  180

  
_(19) (PDF) What Does Sleeping Brain Tell About Stress? A Pilot Functional Near-Infrared Spectroscopy Study Into Stress-Related Cortical Hemodynamic Features During Sleep_. Available from: [https://www.researchgate.net/publication/356726823_What_Does_Sleeping_Brain_Tell_About_Stress_A_Pilot_Functional_Near-Infrared_Spectroscopy_Study_Into_Stress-Related_Cortical_Hemodynamic_Features_During_Sleep](https://www.researchgate.net/publication/356726823_What_Does_Sleeping_Brain_Tell_About_Stress_A_Pilot_Functional_Near-Infrared_Spectroscopy_Study_Into_Stress-Related_Cortical_Hemodynamic_Features_During_Sleep) [accessed Sep 19 2022].
Data files:
1. wl1: ← contains data for wavelength 1 (760 nm)
2. wl2: ← contains data for wavelength 2 (850 nm)
Table 1: Structure of the optical data files:
* .wl1, * wl2. 
* Si: i th source;
* Dj: j th detector;
* tk: k th scan, or time frame of measurement. 
* Si-Dj(tk): reading at the j th detector, of light emitted by the i th source, during the k th scan.
The number of columns in the file equals (number of sources  number of detectors): Smax * Dmax. 

To extract a desired data channel Si-Dj from the file, use the following formula to identify the appropriate column n:

n = (Si-1)Dmax + Dj

3. Header file: .hdr
Nothing in the NIRStar manual