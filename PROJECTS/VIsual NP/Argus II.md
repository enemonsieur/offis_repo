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
