---
alias: [Visual neuroprosthetics]
---
###### tags: #retinalfunction #retinaltype #r
###### links: http://dx.doi.org/10.1016/j.preteyeres.2015.09.003

---
	

The Argus® II Retinal Prosthesis System (Second Sight Medical Products) is the first prosthetic vision device to obtain regulatory approval in both Europe and the USA.
To date, over 100 devices have been implanted worldwide, representing the largest group of patients currently treated with visual prostheses. (now 800)

How does the Argus works?
	Visual information from a glasses-mounted video camera is converted to a pixelated image by an external processor, before being transmitted to the microelectrode array at the macula. Elicited retinal responses are then relayed via the normal optic nerve to the cortex for interpretation. #retinalfunction 


How succesful is the Argus
	The Argus® II has become the most widely used and most successful retinal prosthesis currently available in terms of regulatory approval. Since obtaining the CE mark in 2011 and FDA approval as a humanitarian device in 2013,
BUt why is it so much better than the other RP?
	a) greater accessibility at **lower surgical risk** than the intracranial visual pathways
	b) straightforward monitoring of the device by direct visualisation; ???
	c) **potentially predictable and reproducible retinotopy by applying stimulation at a pre-processing site.** #unclear 
=> it stimulates the RGCs that stimulates what?
Not all the information capture by the eyes are transmitted to the nerve cells. Therefore 
 it'D be possible to see with even a low resolution stimulation of the gagnliion cells
	furthermore, as there are around 120 million photoreceptors while only 1.5 million ganglion cells, **many photoreceptors converge onto a single bipolar cell especially at the periphery,** with further convergence taking place from the bipolar cells to RGCs (Kolb, 2003).
=> There's a massive complexity reduction of the amount of neuron. Especially at the periphery of the eyes, so that you don't really need to stim 120 millions photoreceptors to generate "phosphenes"

>Conversely within the macular region of the retina, the photoreceptor:bipolar cell:RGC ratio approaches 1:1:1, with minimal convergence. It is thus envisaged that focal electrical stimulating patterns with a multi-electrode array in the macular region would more likely manifest retinotopic correlations along the visual pathway. There is, however, a particular limitation to this rationale, due to the arcuate displacement of axons and the piling up of ganglion cell bodies when approaching the fovea. #retinalimitations

some limitations of the implant of electrodes

What percentage of people work well with the Argus?
	Ideal candidates for treatment would therefore have conditions where the outer retina (i.e. photoreceptors and/or retinal pigment epithelium) has been destroyed by any mechanism, while the inner retina (e.g. bipolar cells, RGCs, horizontal cells and amacrine cells) remains relatively intact

The perfect candidates are Retina Pigmentosa
	RP denotes a group of hereditary outer retinal dystrophies, affecting around 1 in 4000 live births and more than a million people worldwide (Hartong et al., 2006). Affected individuals suffer from progressive visual loss which can be profound (0.5% with no light perception and 25% with 20/200 vision in both eyes) (Grover et al., 1999).
=> The Argus works on eyes that have a destroyed outer layer but preserved inner. Therefore, we isolate the diseases that destroy photoreceptors but not RGCs.
This narrows the disease to: RP and AMD
	![[Pasted image 20220711194213.png]]
## Argus components
There are 3 funciton a RP should be able to do: 
1. Capture the visual information
2. Transduc it into electrical stimuli
3. Activating  correctly the Retinal ganglion cells and BPcells (residual inner retina)
#retinalcochlea 
Its made of 3 external and 3 internal components: 

The 3 external componets of Argus are:
	1. . A glasses mounted video-camera e for real-time image capture.
	2.   A portable computer (the Visual Processing Unit, VPU) e for processing of the captured scenes and translation into electrical stimulating parameters conveying spatialetemporal information. 
	3. 3. An external coil (built into the side arm of the glasses) e for wireless transmission of the processed data from the VPU and electrical power to the internal components using radiofrequency (RF) telemetry.
The 3 external components are: 
	![[Pasted image 20220629085057.png]]
	1. An internal coil e as a wireless receiver of RF telemetry, converting radio waves back to electrical signals to recover both data and electrical power. 
	2. **2. An inbuilt Application-Specific-Integrated-Circuit (ASIC) e for generating appropriate electrical pulses in accordance with the stimulating parameter data recovered from the internal coil, which are then relayed to the multi-electrode array.** 
	 => what are the generated pulses?
	3. A 60-channel microelectrode (6 * 10) epiretinal array e consisting of 60 platinum electrodes (diameter ¼ 200 mm) spaced 575 mm (centre-to-centre) apart, embedded in a thin film of polyimide. Each microelectrode is connected to the ASIC in a parallel circuit via a metallised polymer connecting cable, **such that each electrode can be activated independently according to the stimulating parameters.** The array comes into direct contact with the retinal surface, allowing injection of electrical charge
>The internal coil recieve the radio waves of the RF transmiter 
>The ASIC will generate the pulse to the microelectrode
>The electrod will stim the retinal surface

### HOW MUCH VISION IS REGAINED  
### 2.1. Proof of concept

The development of the Argus® II Retinal Prosthesis, as with all retinal prostheses, was based on the following assumptions:

1.The inner retina (RGCs with/without bipolar cells) of end-stage [RP](https://www.sciencedirect.com/topics/medicine-and-dentistry/retinitis-pigmentosa "Learn more about RP from ScienceDirect's AI-generated Topic Pages") patients remains functionally intact for transmission of information along the [visual pathway](https://www.sciencedirect.com/topics/medicine-and-dentistry/visual-pathway "Learn more about visual pathway from ScienceDirect's AI-generated Topic Pages") to the [visual cortex](https://www.sciencedirect.com/topics/medicine-and-dentistry/visual-cortex "Learn more about visual cortex from ScienceDirect's AI-generated Topic Pages").

2.The residual inner retina can be activated focally with localised [electrical stimulation](https://www.sciencedirect.com/topics/medicine-and-dentistry/electro-stimulation "Learn more about electrical stimulation from ScienceDirect's AI-generated Topic Pages") to elicit discrete phosphenes without causing damage or toxicity to the retina.

**3.[Retinotopy](https://www.sciencedirect.com/topics/neuroscience/retinotopy "Learn more about Retinotopy from ScienceDirect's AI-generated Topic Pages") is relatively preserved in the residual inner retina and along the visual pathway, such that simultaneous multi-focal stimulations would form geometric patterns of phosphenes in accordance with retinotopic locations.**
=> Unfortunately it's not


4.The elicited geometric patterns of phosphenes can be relayed in a spatio-temporally correct manner along the visual pathway and interpreted by the primary visual cortex as recognisable visual patterns.

5.Limited pixels can still provide useful visual function.

## HOW IT PULSES

We used a previously established hybrid threshold algorithm to determine the patient's perceptual threshold for individual electrodes [7]. To mimic stimulation generated by daily Argus II use, all electric stimuli were biphasic, charge-balanced, cathode-first current pulses. The pulse width was 0.45 ms/phase, applied for 250 ms at a pulse frequency of 20 Hz. We generated randomly distributed blocks of six electrodes to test in a series of one-hour sessions. Each session involved 300–400 trials. Each trial administered single-electrode stimulation at a pre-determined pulse amplitude, and the subject responded (verbal “yes”/“no”) based on whether a phosphene appeared. The hybrid algorithm continually generated new pulse amplitudes based on a Weibull distribution of previous responses. We randomized the order of active electrodes and included 32 catch (stimulus-absent) trials per block. Trials continued until the maximum likelihood function converged to 0.5 for each electrode, representing a current amplitude where a phosphene appears 50% of the time (Figure 2(a)). Using 50% percept probability to define visual perception threshold is standard in the field of artificial vision [7], [20], [21]. We tested five blocks, establishing perceptual thresholds for 30 electrodes. However, we disregarded one block due to a high false positive rate (>25% “yes” response for catch trials). Thresholds are shown in Figure 2(b) for the 24 eligible electrodes. Electrode impedance was also measured using the native Argus II hardware.

For silicon chronically implanted in the brain, the electrical conductivity of surrounding encapsulation tissue has been measured between 0.15 S/m and 0.37 S/m [24]. We performed a parameter sweep over this range to determine the fibrotic tissue conductivity that produced a model impedance at the center (C5) electrode that best matched with the patient's average electrode impedance.

https://www.intechopen.com/chapters/66090
## 2. Principles of natural vision #toread
## 3. Principles of prosthetic vision
### 3.2 Image processing
	![[Pasted image 20220711200958.png]]

### 3.4 Microelectrode array stimulation
There are three primary sites for placement of a retinal stimulating microelectrode array ([Figure 1](https://www.intechopen.com/chapters/66090#F1)): epiretinally (i.e. on the surface of the neurosensory retina), subretinally (i.e. between the retinal pigment epithelium and the degenerated outer retina) or suprachoroidally (i.e. between the sclera and the choroid). The advantage of the epiretinal placement is that the surgical approach is more familiar to vitreoretinal surgeons, allowing safer and easier implantation, adjustment and removal of devices. Furthermore, the interface with the vitreous cavity seems to permit safer heat dispersion. This set-up may be disadvantageous due to the fact that, in order to stimulate the RGCs, the stimulating current must pass through the retinal nerve fibre layer, which may produce ectopic visual percepts elsewhere in the retinotopic map.

Finally, suprachoroidal devices require a less invasive surgical procedure, which lends itself to easier repair or removal, but trials to date have been complicated by subchoroidal haemorrhage and fibrosis [[52](https://www.intechopen.com/chapters/66090#B52)]. Due to the distance from the RGCs, these systems tend to require higher stimulation thresholds, leading to greater current dispersion and lowering the achievable SR. Overall, it seems that epiretinal and subretinal approaches have a superior performance in safety and efficacy to suprachoroidal implants. However, with pros and cons to both approaches, there is currently no clear evidence to suggest that, of these latter two, one system offers an overall advantage.

The challenge of electrode size and density is primarily a biological one, in as far as the native PR cells change in type, size, density and downstream signalling depending on their role and location in the retina. For example, cone PRs are, on average 6 μm in diameter, but in the centre of the fovea, they are around 1.5 μm in diameter and densely packed to permit the high resolution of vision that humans usually enjoy [[53](https://www.intechopen.com/chapters/66090#B53)]. If we consider that normal vision is 20/20, meaning that the minimal angle of resolution at the retina is 1 arcminute, or the spatial frequency (SF) is 60 cycles per degree (cpd), then the SF required to achieve 20/200 (the approximate level of visual impairment) is 6 cpd. Since each degree angle subtended at the human retina is represented by ~280 μm, a SF of 6 cpd would necessitate a maximum pixel size of about 50 μm and, in turn an electrode size and pitch of 25 μm [[54](https://www.intechopen.com/chapters/66090#B54), [55](https://www.intechopen.com/chapters/66090#B55)]. Therefore, before factors such as electrode contact, dissipation of electrical current or heat are even considered, there is a significant theoretical constraint on the scale of manufacturing required to achieve a resolution corresponding to a visual acuity of 20/200.
=> NOT THAT USEFULL

The Argus II device has 200 μm electrodes separated by 525 μm, which suggests a theoretical maximum VA of 20/1600. The best result, with grating acuity, has been reported as 20/1262 (just over 1 cpd) with this system [[57](https://www.intechopen.com/chapters/66090#B57)].
=> Electrode seperation

Size, shape and contact of the electrode at the tissue interface are all important considerations to improve SR, but also have implications to the charge density per unit area. As the electrode size becomes smaller, there is an exponential increase in concentration of the current, which can result in target tissue damage [[59](https://www.intechopen.com/chapters/66090#B59)]
=> There'S a problem to decreasing the charge. The solution is under.
Therefore there is an onus on finding materials that can permit the charge-injection requirements of neural stimulation, while minimizing conduction of heat or inducing tissue degradation. In addition to this, they must be biocompatible, waterproof and remain operational over an extended lifespan. While the precise electrochemical properties of the electrode-electrolyte interface, the capacitance and charge injection limits of different electrode materials is beyond the scope of this chapter, it is worth noting that new technologies, such as nanocoating, nanotubes and conductive polymers are providing promising developments in electrode fabrication
### 4.3 Safety outcomes

### 4.4 Functional outcomes 
=>What can those MF do with that?

https://www.intechopen.com/chapters/66090
--------------------------------------------------
Simulated prosthetic vision (SPV) studies have been undertaken to try and estimate the optimum spatiotemporal image processing techniques for specific task completion, as well as the basic hardware requirements to best deliver RGC stimulation patterns [[13](https://www.intechopen.com/chapters/66090#B13), [14](https://www.intechopen.com/chapters/66090#B14), [15](https://www.intechopen.com/chapters/66090#B15), [16](https://www.intechopen.com/chapters/66090#B16), [17](https://www.intechopen.com/chapters/66090#B17)]. SPV studies have extensively investigated the spatial resolution, visual field and contrast required for assorted activities of daily living, concluding that a minimum resolution of ~600–1000 pixels over a visual field 15° × 15° can permit reasonable accuracy in manipulation, recognition, orientation and mobility tasks. The resolution of around 3 pixels/degree2 is similar to that in some currently available photovoltaic retinal prosthetic systems while fields of at least 15° × 15° have been created. However, and disappointingly, there remains a mismatch in the functional aptitude demonstrated by subjects in SPV studies and that in recipients of visual prostheses. This suggests that other factors, such as the effects of behavioural adaptation, perceptual learning and cortical plasticity, as well as the loss of the intrinsic retinal processing capacity, could be critical requisites in the development of a visual restorative system that could deliver appreciable functional value [[18](https://www.intechopen.com/chapters/66090#B18), [19](https://www.intechopen.com/chapters/66090#B19)].

 It has been demonstrated that outer retinal degenerative disease results in a cascade of reorganization and remodelling within the retina and central nervous system, even taking place before there is clinical evidence of PR loss [[20](https://www.intechopen.com/chapters/66090#B20), [21](https://www.intechopen.com/chapters/66090#B21), [22](https://www.intechopen.com/chapters/66090#B22), [23](https://www.intechopen.com/chapters/66090#B23), [24](https://www.intechopen.com/chapters/66090#B24)]. A stepwise deterioration culminates in extensive neuronal cell migration, rewiring and death, accompanied by glial hypertrophy and retinal remodelling, rendering the retina incapable of processing or encoding visual data. This neuronal plasticity carries implications for all forms of visually restorative therapy, but particularly for prostheses, which are currently introduced at a late stage of visual impairment, where there has already been widespread reorganization with limited scope for rescuing vision. However, it may be that future iterations of bionic devices could even be introduced earlier in tthe disease process in an attempt to halt or reverse the remodelling process.
 
Another matter that remains unclear is the extent to which the human brain undergoes reorganization following loss of visual sensory input. Both animal and human studies have shown that there is the capacity for neuroplasticity as a functional adaptation to loss of a sensory modality [[25](https://www.intechopen.com/chapters/66090#B25), [26](https://www.intechopen.com/chapters/66090#B26), [27](https://www.intechopen.com/chapters/66090#B27)]. For example, visual cortical activity has been demonstrated in blind subjects while reading Braille [[28](https://www.intechopen.com/chapters/66090#B28), [29](https://www.intechopen.com/chapters/66090#B29)]. Other studies of patients undergoing cochlear implant surgery, have shown correlation between the pre-operative auditory organization and activation and subsequent success of the neuroprosthesis [[30](https://www.intechopen.com/chapters/66090#B30), [31](https://www.intechopen.com/chapters/66090#B31)]. If a method could be developed by which a patient could be assessed for the feasibility of generating interpretable phosphenes, this would enhance patient selection and thus outcomes in this area of visual restoration. Further understanding of the nature of cortical plasticity in sensory loss and how subjects can adapt to a new form of vision with perceptual learning and rehabilitation, is sure to enhance the beneficial effect of visual restorative treatments in the future.


https://jamanetwork.com/journals/jamaophthalmology/fullarticle/1375731
----------------------------------------------------------------------
Each of the 60 electrodes (in a 6 × 10 grid) were 200 μm in diameter and were made of platinum gray, a high surface-area platinum developed by Second Sight Medical Products (US Patent no. 6 974 533). The array (along the diagonal) covered an area of retina corresponding to about 20° in visual angle, assuming 293 μm on the retina equates to 1° of visual angle.[6](https://jamanetwork.com/journals/jamaophthalmology/fullarticle/1375731#ref-ecs120052-6)

Stimulation parameters were chosen such that they maximized the subject's performance on previous assessments during the clinical trial, while remaining within the safety and technical limits of the system. Stimulation parameters used for all subjects were charge-balanced cathodic-first pulses with a pulse width of 0.46 milliseconds, except for a single subject (61-001), who used settings with a pulse width of 0.97 milliseconds. The pulse frequency was fixed for each subject, ranging from 3 Hz to 60 Hz.

https://iovs.arvojournals.org/article.aspx?articleid=2188619
---------------------------------------------------------------
he DS array of 4 × 4 hardwired microelectrodes (titanium nitride, TiN) in a rectangular grid with a spacing of 280 μm (Fig. 1a) is used for light-independent, direct stimulation of the retina. This array was modified during the course of the study to increase the safe charge injection capacity of the electrodes: In first-generation implants 50 × 50-μm electrodes (S1–S8; Fig. 1b) were used and in second-generation implants, 100 × 100-μm electrodes (one electrode consisting of four 50-μm electrodes close together owing to the production process; S9–12, compare Fig. 1c). The electrodes are driven monopolarly, with one large return electrode subcutaneously placed near the orbital rim. The implant is connected to a battery-driven stimulus generator via a percutaneous cable (Fig. 1d). It employs a single constant voltage source that can route one stimulation voltage to an arbitrary combination of electrodes. Therefore, in concurrent stimulation of multiple electrodes, differences in thresholds between electrodes could not be accounted for. Amplitude (0–2.3 V), pulse duration (0.5–6 ms), and pulse shape (square-wave anodic or cathodic first, biphasic, or monophasic) can be adjusted. Each electrode is grounded after stimulation, to allow for charge balance.
![[Pasted image 20220714141247.png]]

. Single pulses of 0.5- to 6-ms duration and the four pulse forms were tested in separate sessions. Generally, single biphasic pulses with a duration of 2 to 3 ms yielded the best reproducible thresholds. Transferred charge at threshold was typically in the range of 20 to 60-nC per phase. 26  

The stimulation parameters were tested only for influence on thresholds (Wilke R, et al. _IOVS_ 2010;51:ARVO E-Abstract 2026), not for the perception of patterns. All psychophysical tests were performed by using the stimulation setting with the lowest thresholds, and single-pulse stimulation was applied, so that the participants saw a certain pattern only once for a brief time. 

Psychophysical Tests and Statistics

After an initial phase for finding the optimal stimulation parameter and a brief learning phase, all psychophysical tests were performed employing an alternative forced choice scheme. 44 Reported results include the chance rate and the _P_ value calculated from the binomial function. Although the chance rate depends only on the number of choices given, the _P_ value also depends on the number of trials and indicates the probability of obtaining the respective hit rate or a higher one by guessing. Results with _P_ < 0.05 were considered to be significant. The sequence within individual tests was randomized. Results are summed from tests of multiple sessions.

![[Pasted image 20220714141651.png]]
https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg
------------------------------------------------------------------------------
##### 2.4.3.2. Selective stimulation and waveform

Various stimulation strategies aimed to improve the temporal and spatial profiles of the retinal response have been studied. Selective activation of bipolar cells and ganglion cells is possible by altering the stimulus waveforms ([Freeman et al., 2010](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib53), [Fried et al., 2006](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib55), [Margalit and Thoreson, 2006](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib118)). Retinal ganglion cells are more susceptible to short duration pulses (<150 μs) whereas inner retinal neurons favor longer pulse width. Bipolar cells are preferentially activated by sinusoidal stimulus at 25 Hz and ganglion cells at 100 Hz, thus rectangular waveforms employed by the retinal prostheses are likely to activate both cell types ([Freeman et al., 2010](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib53)). Within the ganglion cell population, specific activation of single ON and OFF parasol cells was initially accounted by [Sekirnjak et al. (2008)](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib166), using small electrodes (9–15 μm diameter) and short duration (0.05–0.1 ms) biphasic stimulation. With similar approach, localized activation of ON and OFF midget cells and bistratified retinal ganglion cells was achieved, but at only ∼50% of the time, due to the unwanted axonal activation ([Jepson et al., 2013](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib85)). It remains a challenge to preferentially activate specific ganglion cell populations by variations in the waveforms alone, if not taking into account the spatial factors such as electrode size. [Jensen and Rizzo (2006)](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib83) found that, in subretinal stimulation, ON and OFF cells exhibited [differential thresholds](https://www.sciencedirect.com/topics/medicine-and-dentistry/differential-threshold "Learn more about differential thresholds from ScienceDirect's AI-generated Topic Pages") for anodic-leading current pulses but not for cathodic-leading pulses, possibly unveiling a mechanism for the targeted stimulation of ON and OFF signaling pathways.

##### 2.4.3.3. Stimulation efficiency and waveform

Changes in the stimulus waveforms influence the stimulation efficiency. Addition of an [interphase](https://www.sciencedirect.com/topics/medicine-and-dentistry/interphase "Learn more about interphase from ScienceDirect's AI-generated Topic Pages") gap between the leading cathodic phase and the following anodic phase has been demonstrated to be effective in reducing electrical stimulation thresholds for the epiretinal Argus II prosthesis ([Weitz et al., 2014](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib201)). Enhanced brightness of the phosphenes can be achieved by increasing either the amplitude or the frequency of the stimulation, but the latter allows for the maintenance of the phosphene size ([Nanduri et al., 2012](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib132)). The working frequency of the subretinal Alpha IMS implant is typically set at 5–20 Hz, though some patients preferred a lower frequency to prevent phosphene fading ([Stingl et al., 2015](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib178)). [Freeman and Fried (2011)](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib54) proposed a fade-resistant strategy that consists of longer duration desensitizing pulses (1 ms) interspersed in the short duration stimulating pulse trains. The desensitizing pulses, expected to diminish the synaptically mediated response, are continuously delivered independent of luminance. The effectiveness of this strategy is not experimentally validated yet.

#### 2.4.5. Stimulation encoding
These 20 separate mosaics are interwoven over the entire retina, oftentimes with overlapping receptive fields, and each extracts a distinct feature of the image flow, such as luminance, contrast, shape, color and motion. Outputs of these mosaics are carried to the higher visual centers in the brain each via a specific ganglion cell channel, encoded by the spatiotemporal patterns of spiking ([da Silveira and Roska, 2011](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib34), [Trenholm and Roska, 2014](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#bib186)). In the presence of the same visual stimuli, these anatomically distinct ganglion cell types are known to exhibit differential responses that are integrated and decoded by the cortex to generate sense of vision. Therefore a stimulation algorithm that incorporates the firing patterns specific to each mosaic has the potential to produce retinal outputs more readily interpretable to the cortex

Due to various constraints on the electrode size as discussed in Section [2.4.1.1](https://www.sciencedirect.com/science/article/pii/S1350946216300271?casa_token=Vi1M1Ddhi_YAAAAA:xLwovbsaX_tVLT-dxvRSbA4hiZ-tmzFPIpmuQtBmWJoa1PujnFccMy0sLfFjNrYXTVCCUO7sWg#sec2.4.1.1), current devices only allow simultaneous activation of multiple cell populations. 
EXEMPLE:
Earlier electrophysiological studies have predicted primate ganglion cell responses by a linear-nonlinear (LN) cascade model with a difference-of-Gaussians or wavelet-shaped characteristic spatial profile

### retinal degeneration
Functional magnetic resonance imaging (fMRI) of the patients with [macular degeneration](https://www.sciencedirect.com/topics/medicine-and-dentistry/macular-degeneration "Learn more about macular degeneration from ScienceDirect's AI-generated Topic Pages") indicates that part of the cortex that normally responds to foveal visual inputs are strongly activated by the peripheral stimuli, confirming some level of neuroplasiticity in visually deprived cortex
But other studies with PET scans suggest otherwise