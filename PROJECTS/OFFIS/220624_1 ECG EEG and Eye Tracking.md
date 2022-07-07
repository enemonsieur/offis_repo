---
alias: [ECG Eye Tracking EEG]
---
###### tags: #ecg #eeg #eyetracker 
###### links:  

# Signal Acquisition
"ECG signal was acquired using the ECG v.12 device manufactured by Bayamed"
"The SX230 surface electrode and Skintact F-55 electrode were used to acquire the EMG and ECG signals, respectively." [[@bitkinaAbilityEyetrackingMetrics2021]]

"In accordance to the guidelines for HR and HRV measurement in occupational science [57] for ECG measurement, a 1-channel Faros eMotion 180◦ Holter ECG with 1000 Hz sampling frequency was used. Eye-tracking data were recorded using SensoMotoric Instruments (SMI) Eye-Tracking Glasses 2 Wireless. Sampling frequency for binocular recording was 60 Hz using the inbuilt infrared sensors." [[@blasingInfluenceIncreasingTask2021]]

The wearable eye-tracker of Tobii Pro Glasses 2 was used to record the driver’s glance and pupil behavior with Corneal reflection and dark pupil techniques (Tobiipro, 2021). [[@bitkinaAbilityEyetrackingMetrics2021]]


"The state-trait anxiety inventory (STAI)  questionnaire was utilized to measure the self-reported stress of participants."
-> To measure stress as reported by participants we use the STAI. Stress is measured before and after the experiment. [[@bitkinaAbilityEyetrackingMetrics2021]]

Standard NASA-TLX questionnaire (Appendix 1) was used as an assessment tool to measure the subjective driving workload with a score scale of 0 –100. The survey was conducted in the form of a written questionnaire after driving experiments for each participan
[[@bitkinaAbilityEyetrackingMetrics2021]]
- Stroop Task was used to induce stress. 
[[@pourmohammadiStressDetectionUsing2020]]


# Preprocessing

![[stress detection using ECG and EMG#^bb94e6]]
=>To pick up the signals from the ECG, namly the R peaks, we use a bandpass filter. For the RR interals, we use the Pan-Tompkins peak detection algo.
- We can divide the filtered ECG signales into 60s frames [[@pourmohammadiStressDetectionUsing2020]]

"Data preparation and analysis were performed using Mathworks MATLAB 2019a and the HRV Tool [58] for ECG data and SMIs BeGaze for eye-tracking data. IBM SPSS 25 was used for statistical analysis." [[@blasingInfluenceIncreasingTask2021]]

# Features finding
![[stress detection using ECG and EMG#^00cfb3]]
=> We extract 3 leads (I II III)*25 features for the ECG. 
- We remove unnecessary features to improve algo accuracy. We use the RSFS method for that:

"Besides, in the SFFS method, the gain of a feature is computed by including or excluding it from an existing set of features, but in the random subset feature selection (RSFS) method, each feature is evaluated in terms of its average usefulness with other feature combinations. The steps of the RSFS method summarized as follows:" [[@pourmohammadiStressDetectionUsing2020]]

"the following metrics were extracted and used in the analysis: maximal, minimal, mean, and standard deviation of gaze point (on x/y axis), gaze duration, gaze fixation (on x/y axis), and pupil diameter. Extracted eye-tracking metrics with abbreviations used in the analysis are shown in Table 1." [[@blasingInfluenceIncreasingTask2021]]
	![[Pasted image 20220707085847.png]]
# Stress Prediction
- We classify the predicting features using the SVM
- ![[@blasingInfluenceIncreasingTask2021]]
Logistic regression analysis was performed to classify high and low workload levels through eye-tracking metrics using IBM SPSS Statistics Version 25 Software.[[@bitkinaAbilityEyetrackingMetrics2021]]