---
alias: [ECG Eye Tracking EEG]
---
###### tags: #ecg #eeg #eyetracker 
###### links:  

# Signal Acquisition
"ECG signal was acquired using the ECG v.12 device manufactured by Bayamed"
"The SX230 surface electrode and Skintact F-55 electrode were used to acquire the EMG and ECG signals, respectively." 

"The state-trait anxiety inventory (STAI)  questionnaire was utilized to measure the self-reported stress of participants."
-> To measure stress as reported by participants we use the STAI. Stress is measured before and after the experiment. 
[[@pourmohammadiStressDetectionUsing2020]]

Stroop Task was used to induce stress. 
# Preprocessing

![[stress detection using ECG and EMG#^bb94e6]]
=>To pick up the signals from the ECG, namly the R peaks, we use a bandpass filter. For the RR interals, we use the Pan-Tompkins peak detection algo.
- We can divide the filtered ECG signales into 60s frames
# Features finding
# Stress Prediction

