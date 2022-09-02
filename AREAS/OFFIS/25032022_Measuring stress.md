#measurestress #stress To measure stress with EEG we use the frontal EEG assymetry, and measure the F3 and F4 channels. The waves of interest are the alpha waves [Toth, 2015 (Bs.C Thesis)](-   [10.13140/RG.2.1.3441.6162](http://dx.doi.org/10.13140/RG.2.1.3441.6162))
	285.2 Frontal EEG asymmetry15. Figure: Channel locations of the Emotiv EPOC. The electrodes, from which the asymmetryfeatures were obtained are indicated in red.In the current study, the EEG asymmetry feature was obtained as = (3) − (4)where the power spectral density (PSD) via Welch periodogram was used todetermine the alpha band powers for the EEG signals. The alpha waves activity was takenbetween 8 and 13 Hz. Logarithm was calculated for both left and right hemisphere alphaactivity before subtracting the right from the left. The Matlab code that extracts the alphaasymmetry feature is the following:
	Here the input was the array of examined alpha frequencies (IAF) in ascendingorder and the matrix of EEG data that consisted of 15 rows: time series in the first, and EEG voltage data of 14 channels in the consecutive rows. Every row, except for the first,was labelled with the index of the sensor as the first column. The alpha asymmetry featurewas calculated for widows with length of 1 second without overlapping. The result wasviewed beside the skin conductance measurements to validate frontal EEG asymmetry asthe indicator of fear intensity.
``` MATLAB
function fea = fea_feature(EEG, freqs)
F3ind = 3 + 1;
F4ind = 12 + 1;
[F3psd, F3freqs] = pwelch(EEG(F3ind, :),[],[],[], 128);
[F4psd, F4freqs] = pwelch(EEG(F4ind, :),[],[],[], 128);
F3psdind = F3freqs >= freqs(1) & F3freqs <= freqs(end);F4psdind = F4freqs >= freqs(1) & F4freqs <= freqs(end);
fea = mean(log(F3psd(F3psdind)) - log(F4psd(F4psdind)));

end
```

This study uses EEG at the  frontal lobes position (photo included ), and measured Relative Gamma and Alpha Assymetry
	In relation to the EEG acquisition, we used the Versatile EEG system, a semi-dry acquisition device designed by Bitbrain (Spain), that works at a sampling rate of 256 Hz. For the electric setup, we considered four electrodes located at positions Fp1, Fp2, F5, and F6 of the 10–20 International System based on previous successful studies about emotions assessment ([Brown et al., 2011](https://www.frontiersin.org/articles/10.3389/fncom.2021.684423/full#B7); [Jenke et al., 2014](https://www.frontiersin.org/articles/10.3389/fncom.2021.684423/full#B18); [Vaquero-Blasco et al., 2020](https://www.frontiersin.org/articles/10.3389/fncom.2021.684423/full#B36)). The electrodes were referenced at the left ear lobe and grounded to an extra electrode equidistant from Fpz and Fz. For all the participants, we acquired an independent EEG recording for each phase of the experimental session
 Subsequently, we carried out a feature extraction phase. In this phase, we estimated the channel-averaged power spectral density (PSD) in Delta (1–4 Hz), Theta (4–8 Hz), Alpha (8–13 Hz), Beta (13–25 Hz), and Gamma (25–45 Hz) bands, the RG, and the Alpha asymmetry (AA). Prior to the estimation of the spectral power, we applied a Tukey window to ease edge effects. Formulae for RG and AA are presented in Eqs 1 and 2.

	![[Pasted image 20220627080600.png]] 
[Perez-Valero 2021 Quantitative Assessment of Stress Through EEG During a Virtual Reality Stress-Relax Session](![[Pasted image 20220627080902.png]]) 


  To measure accurately HRV we use the IBI that we can compute finding its loss function (mean square error) accross all of the IBI. Another alternative is to compute the %of IBI that differs more than 50ms from the other, which is called **pNN50**

- SSSQ has been used in conjunction with NASA-TLX to gauge changes in stress due to the experimental setup along with NASA-TLX (Matthews & Campbell, 2010)
- 
#measurestress #hrv #ecg HRV is the beat-to-beat variation of the interbeat interval (IBI) of the ECG (ECG). This variability is modulated primarily by the sympathetic and parasympathetic autonomic nervous system (2– 4). Methods for calculating time and frequency-domain parameters of HRV were recommended by the Task Force of the European Society of Cardiology (5) and these methods have been widely adopted (6). The SD of the IBI (SDNN) is the most widely used measure of HRV, followed by the root mean square of the difference of successive IBIs (RMSSD). [kemper (2007)](http://www.nature.com/doifinder/10.1203/PDR.0b013e318123fbcc)
- Other commonly used parameters include pNN50 (the percentage of IBIs that differ by more than 50 ms from the previous IBI), and parameters from power spectral analyses based on fast Fourier transformations, particularly low frequency (LF) and high frequency (HF) power. HF oscillations (0.15- 0.4 Hz) are thought to be markers of parasympathetic and particularly vagal autonomic tone. LF oscillations (0.04 – 0.15 Hz) reflect sympathetic and to a lesser extent, parasympathetic tone (7).


## ECG stress measurement

- Subject preparation #ecg [(Fletcher 1998)](https://reader.elsevier.com/reader/sd/pii/S0146280698800078?token=A880CC28528B7E9873FB6DBEB7B3A6EB3DB92A305DCD2FF0FBFDC16EF9C91D8F270AAA53E23D457960B788371E6EADCF&originRegion=eu-west-1&originCreation=20220628123534)
	- The subject should be instructed not to eat or smoke for 3 hours
before the test and to dress appropriately for exercise, especially with
	3 6 2 Curr Probl Cardiol, July 1 9 9 8
	regard to footwear. No unusual or intense physical activity should be
	performed for >12 hours before testing
**Preparing the skin:** Skin preparation. The most critical issue of the electrode-amplifier-
recording system is the interface between electrode and skin. Removal of
the superficial layer of skin significantly lowers resistance, thus decreas-
ing the signal-to-noise ratio. The areas for electrode application are first
shaved (if needed) and then rubbed with alcohol-saturated gauze. After
the skin dries, it is marked with a felt-tipped pen and rubbed with a fine
sandpaper or rough material. With these procedures, skin resistance
should be reduced to <5000 f~

 (Pourmohammadi and Maleki, 2020, p. 3)
![[Pasted image 20220628144257.png]]
- Self reporting: 
	- To measuure stress they used a state-trait anxiety inventory (STAI) [25] questionnaire, which measure the conscious moments of anxiety. This is usually associated with arousal of the ANS. 
	- Details on the experiment: In arithmetic tasks, the mathematical expressions were presented with their corresponding answers (greater than and smaller than) and the participant decided whether or not the answer was correct. Each mathematical expression was displayed for up to five seconds. No response was received during the first two seconds to avoid nothinking responses. After two seconds, if the participant answered correctly, the “correct” feedback text was shown immediately. If the answer was incorrect, the “incorrect” feedback text was shown immediately. Otherwise, when five seconds elapsed, the “Time out”
	- What features are measured by the EEG and EMG:
		- or the ECG signal of each lead (I, II and III), 25 HRV features were extracted. Therefore, the ECG feature vector consisted of 75 features. HRV is the physiological phenomenon of tiny fluctuations in the time intervals between heartbeats. It reflects the tenseness and balance of the sympathetic and the vagus nerve activities and their effects on the cardiovascular motion [37]. Therefore, HRV is of significant importance and adverse in the stress detection field. HRV is traditionally determined by the digital processing of the ECG signal. The R-wave peaks of QRS complexes in ECG were detected and RR intervals were calculated. Then, several time-domain, frequency-domain and nonlinear features were extracted [38]. A list of the features along with their descriptions are presented in Table 2. For more details, see [9,39,40].
		- ![[Pasted image 20220628144902.png]]

- Where to monitor the ECG #ecgmeasurement #stress
	- https://www.researchgate.net/post/Where-is-the-best-location-to-measure-the-ECG-and-HR-simultaneously-instead-on-the-chest
	- if it is for monitoring purposes limb leads would be sufficient or you can even try the alternative electrode position over the mid arms and lower abdomen as described [in this paper:](https://openheart.bmj.com/content/openhrt/2/1/e000226.full.pdf)![[Pasted image 20220628145302.png]]
	- In the cathlab we used to put the elctrodes on the shoulders and base of the thorax. It gives a clear ECG signal wothout interfering with the angio acquisition
		> It's also about avoiding intereference with the other measurement parameters