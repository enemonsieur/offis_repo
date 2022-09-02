---
alias: [ECG Eye Tracking EEG]
---
###### tags: #ecg #eeg #eyetracker 
###### links:  @giannakakisReviewPsychologicalStress2022

# Signal Acquisition
## ECG
"ECG signal was acquired using the ECG v.12 device manufactured by Bayamed"
"The SX230 surface electrode and Skintact F-55 electrode were used to acquire the EMG and ECG signals, respectively." [[@bitkinaAbilityEyetrackingMetrics2021]]

"In accordance to the guidelines for HR and HRV measurement in occupational science [57] for ECG measurement, a 1-channel Faros eMotion 180◦ Holter ECG with 1000 Hz sampling frequency was used. Eye-tracking data were recorded using SensoMotoric Instruments (SMI) Eye-Tracking Glasses 2 Wireless. Sampling frequency for binocular recording was 60 Hz using the inbuilt infrared sensors." [[@blasingInfluenceIncreasingTask2021]]

## Eye Tracker
"The wearable eye-tracker of Tobii Pro Glasses 2 was used to record the driver’s glance and pupil behavior with Corneal reflection and dark pupil techniques (Tobiipro, 2021)." [[@bitkinaAbilityEyetrackingMetrics2021]]

The metrics tracked are: maximal, minimal, mean, and standard deviation of gaze point (on x/y axis), gaze duration, gaze fixation (on x/y axis), and pupil diameter.

"The state-trait anxiety inventory (STAI)  questionnaire was utilized to measure the self-reported stress of participants."
-> To measure stress as reported by participants we use the STAI. Stress is measured before and after the experiment. [[@bitkinaAbilityEyetrackingMetrics2021]]

Standard NASA-TLX questionnaire (Appendix 1) was used as an assessment tool to measure the subjective driving workload with a score scale of 0 –100. The survey was conducted in the form of a written questionnaire after driving experiments for each participan
[[@bitkinaAbilityEyetrackingMetrics2021]]

# EEG

- Stroop Task was used to induce stress. 
[[@pourmohammadiStressDetectionUsing2020]]


# Preprocessing

![[stress detection using ECG and EMG#^bb94e6]]
=>To pick up the signals from the ECG, namly the R peaks, we use a 5-15 Hz bandpass filter. For the RR interals, we use the Pan-Tompkins peak detection algo.
- We can divide the filtered ECG signales into 60s frames [[@pourmohammadiStressDetectionUsing2020]]

"Data preparation and analysis were performed using Mathworks MATLAB 2019a and the HRV Tool [58] for ECG data and SMIs BeGaze for eye-tracking data. IBM SPSS 25 was used for statistical analysis." [[@blasingInfluenceIncreasingTask2021]]

# Features finding
![[Detection of human stress]]
=> To find the best results, the study used signal from 0 to 10Hz, and seperated them in sub-bands. This lead to rougly 80% accuracy in the models they used (SVM and k-nearest neighbor) [[@karthikeyanDETECTIONHUMANSTRESS2013]]


![[stress detection using ECG and EMG#^00cfb3]]
=> We extract 3 leads (I II III) * 25 features for the ECG. 
- We remove unnecessary features to improve algo accuracy. We use the RSFS method for that:

"Besides, in the SFFS method, the gain of a feature is computed by including or excluding it from an existing set of features, but in the random subset feature selection (RSFS) method, each feature is evaluated in terms of its average usefulness with other feature combinations. The steps of the RSFS method summarized as follows:" [[@pourmohammadiStressDetectionUsing2020]]

"the following metrics were extracted and used in the analysis: maximal, minimal, mean, and standard deviation of gaze point (on x/y axis), gaze duration, gaze fixation (on x/y axis), and pupil diameter. Extracted eye-tracking metrics with abbreviations used in the analysis are shown in Table 1." [[@blasingInfluenceIncreasingTask2021]]
	![[Pasted image 20220707085847.png]]


## EEG
"In this phase, we estimated the channel-averaged power spectral density (PSD) in Delta (1–4 Hz), Theta (4–8 Hz), Alpha (8–13 Hz), Beta (13–25 Hz), and Gamma (25–45 Hz) bands, the RG, and the Alpha asymmetry (AA). Prior to the estimation of the spectral power, we applied a Tukey window to ease edge effects. Formulae for RG and AA are presented in Eqs 1 and 2."
=>Extract the different frequencies bands, the RG and the alpha asymmetry.

EEG asymmetry index is a robust stress feature revealing emotional arousal [28] implicated in many studies to differentially dissociate psychological states [29]. The EEG asymmetry index is the subtraction of the alpha’s power natural logarithm of the right hemisphere from that of the left hemisphere, as provided by the equation:
![[Pasted image 20220808174441.png]]
=> Assymetry index: We substract the power frequency (?) of the left versus right hemisphere.

The most common positions used in the estimation of alpha asymmetry are channels F3-F4 as they are located above the dorsolateral prefrontal cortex [30], [31], a region directly affected by stressful conditions [32]. However, there are stress studies employing lateral (e.g., F7-F8 [33]), anterior (e.g., Fp1-Fp2 [34], [35]), and posterior pairs (e.g., C3-C4, O1O2 [29], T5-T6 [35]) as shown in Fig. 5.
The majority of studies support the notion that in stress state there is generally greater frontal right alpha activity in relation to the left alpha activity [26]
=> To find that assymetry index, we use the channels F3 and F4 (Frontal areas)


Although there are some conflicting results in spectral features, stress conditions are considered to decrease the alpha activity [29], [35], [44], [45], [46], [47], [48], [49] and increase the beta activity waves [47], [50]
=> Increase stress should result in decreased Alpha activity.

An index that integrates the variations of both alpha and beta rhythms is reflected in the beta to alpha power ratio (b/a ratio) being a measure of cognitive load associated with the arousal dimension [52]. Increased beta/alpha relative power ratio is commonly expected in stress groups [30].
=> Find the power ratio: Beta/Apha activity. If it increase that means stress increases. 

Power of higher frequency rhythms (such as gamma band) may provide a sensitive index of stress response magnitude (relative power in the gamma band recorded from prefrontal electrodes [35]), although caution is advised when interpreting results in this frequency range due to the potential of contamination by myogenic activity.
=> Consider measuring gamma bands frequencies ryh

# Stress Prediction
- We classify the predicting features using the SVM
- ![[@blasingInfluenceIncreasingTask2021]]
"Logistic regression analysis was performed to classify high and low workload levels through eye-tracking metrics using IBM SPSS Statistics Version 25 Software"

"NASA-TLX workload scores were divided into the low (0–50) and high (51–100) levels. In the presented research, the Nasa-TLX scale is normalized to a number between 0 and 100. Point 50 is the midpoint of the scale, which was selected as a cutofffor workload level classification (low and high) and labeled as neutral considering the verbal anchor for the midpoint. In this type of scale, the middle value (midpoint) can be used as a cutoff (Zheng et al., 2011; McDonald et al., 2014). In the lo gistic model, the dependent variable was coded as a “0′′ event in case of low workload, and the high workload was a “1′′ event; independent variables were 24 extracted eye-tracking metrics.""
=> we transform the NASA scale into metrics from 0 to 100. and define a cut off at the middle to implement a logistic regression model as 0= low workload 1= high workload


.[[@bitkinaAbilityEyetrackingMetrics2021]]
