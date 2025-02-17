+++
title = "Research"
type = "gallery"
+++
![](/IMG_5650.jpg)


# News
- 2025-02-04: My paper on [The Bullseye Galaxy](../publications/bullseye/), recently published in ApJL, was the subject of several press releases from STScI/HST, Keck, and Yale, which were then also referenced in numerous news publications. 
- 2023-12-15: My paper on [Quenching in Cosmic Sheets](../publications/quenching-sheets/) was awarded the Yale Astronomy Department's annual Beatrice Tinsley Prize. 



# Overview 

I am broadly interested in the processes that drive galaxy evolution, and the tools and techniques we use to characterize galaxy properties. I work with both observations and simulations, having spent over 50 nights leading observing runs at Keck Observatory (mostly LRIS, KCWI, MOSFIRE, NIRES, and NIRSPEC) as well as having worked extensively with cosmological simulations. 


In particular, from the processes perspective, my research has focused on the interplay between galaxies, their **circumgalactic media** (CGM), and their surrounding enviornments. 

# Quenching in Cosmic Sheets 
In a [recent simulation paper](../publications/quenching-sheets/), I followed the evolution of high redshift dwarf galaxies which experienced a cosmic shock --- literally. During the formation of the cosmic web and large scale structure collapse, so-called cosmic "sheets" can form, large planes of stratified gas which eventually collapse into the filaments we see in the cosmic web today. But when two of these sheets collide, an accretion shock can rapidly drive the entirety of the (combined) sheet regions to high ambient temperatures in excess of a million Kelvin. Such temperatures exceed the virial temperature of dwarf galaxies, and I showed that indeed, the cold CGM of sheet-dwelling dwarf galaxies in the simulation I was using --- one of the largest area high resolution zoom simulations of the IGM to date --- was being stripped or otherwise heated, leaving the galaxies without a supply of cold gas to accrete and ultimately form stars. 

![](/quenching.png)


# Direct Imaging of the CGM with the Dragonfly Spectral Line Mapper 

Much more locally, my observational thesis work focuses on the CGM of nearby galaxies. Because the gas in the CGM is so low in density, highly specialized instruments are required to tease out the large scale low surface brightness emission from ionized gas (e.g., Halpha, [NII], [OIII]). 

To this end, the Dragonfly Team (a collaboration between U Toronto and Yale) have been developing and comissioning a new instrument based on the design successes of the Dragonfly Telephoto array --- an exquisite low surface brightness imager comprising 48 canon telephoto lenses as the primary light gathering aperatus. 

We build on this design, expanding to 120 lenses and adding ultranarrowband, tunable filters to the front of each lens, which can target the key optical emission lines from CGM gas for galaxies out to ~4000 km/s. The picture below is just one of the 4 mounts of 30 lenses each! 

![](/dslm.jpg)


You can read much more about the instrument and my contributions to it [here.](dslm)

First results from the instrument are already available; using a pathfinder (3-lens, 3nm filter) prototype, our group discovered several new features in the well-studied M81-M82 group. In my case, I discovered and characterized a young star forming structure in the tidal streamer being stripped from M82, which bears the signs of being a possible Tidal Dwarf Galaxy progenitor. You can read more about that paper [here.](../publications/tdg/)

![](/tdg.webp)
{.custom-css-class}

# Bridging Simulations and Observations of the CGM 

The goal of DSLM is to "take a picture" of the CGM around nearby galaxies, unlocking spatially resolved studies of the brightness, extent, and morphology of the gas. Understanding these observations necessetates comparison to simulations, and in turn, this means we require the forward modeling for realistic observations from simulations. 

At the same time, simulations have been working to improve predictions in the CGM for some time; the low densities generally mean that simulations have poor spatial resolution in the CGM, and numerous studies have found that essentially no simulation (including those focused on enhanced resolution in the CGM) is fully converged. On top of this, processes which actually produce the line emission from the gas may come from very small (relatively) interface regions dominated by physics totally sub-resolution to the simulation. Self shielding, radiative transfer, and the subgrid models being used etc., all need to be understood before all aspects of predictions in the CGM can be trusted. 

Nevertheless, direct observations of the resolved CGM are beginning to provide actionable constraints on aspects of simulations. 

In short, both fields are working toward a common goal at the moment, with several groups attempting to build CGM focused zoom simulations, and numerous observational facilities coming online to match that with new data. 

![](/tng.webp)

Given my involvement in Dragonfly and interest in simulation work, a natural project emerged in order to combine current state-of-the-art CGM simulations with the data DSLM is beginning to gather. You can parse this several ways; in some sense, it is making qualitative predictions for the observing strategy we will need with DSLM to see the putative CGM and indicating where and how the gas *should* be distributed generally. In another sense, it is the creation of a mock which Dragonfly can soon quantitatively validate or invalidate in certain aspects of the emission, providing constraints on, e.g., feedback and accretion models. Either way, such comparisons will be bi-directional. 

I am currently working on a paper which forward models TNG50 galaxies into the DSLM observed frame for this kind of comparison --- I am also using FIRE2 and (hopefully soon) FOGGIE data for these comparisons, but I am starting with TNG50 (the lowest resolution) case as it has the largest statistical sample. 

I've dubbed this ongoing project **CGMBridge**, and hope to have first results out for those studies soon. 

# Examining the Fate of Collisional Ring Galaxies 


Collisional Ring Galaxies (CRGs) form when one galaxy flies at a nearly 90 degree angle through the center of another (sprial). The outcome is a reconfiguration of the impacted galaxies, in which spiral arms are swept by propogating structures into one or more rings. Classic examples of this type of system include Hoag's Object and the Cartwheel galaxy. 

![](/crg.jpg)

I recently discovered a very rare case of a CRG in Legacy imaging --- rare beause the "ring" phase of evolution is incredibly short by cosmic standards, which is in part why not many of these systems are known. But this system, which we nicknamed the Bullseye, was especially rare, because it has not one, nor two, but at least *nine* rings. 

Not only does this provide a rare look at the shortest-lived phase of ring galaxy post collision evolution, we also discovered faint emission far in the outskirts (~70 kpc) of the galaxy. We hypothesize this emission is from the first expanding ring, which has since faded. If this is indeed the case, it would provide a strong case that CRGs can evolve into giant low surface brightness disks as they evolve --- validating some simulation-based evidence that this can occur, and shedding light on the formation mechanism of another poorly understood (and poorly sampled) galaxy type. 

I was awarded several orbits of HST time during Cycle 31 to obtain high resolution imaging of the system in F425W and F814W, and in combination with Keck imaging and spectroscopy and the Dragonfly Telephoto Array, we have published a comprehensive study of the system and its rings. 

![](/esa-bullseye-crop-scalebar.jpg)

This exciting galaxy was the subject of several press releases and, in turn, numerous news articles highlighting the unique nature of the system.


# Tools and Techniques 

Another aspect of my work has focused on the techniques and tools we use to extract information about galactic systems. How do we infer the properties we care about e,g., mass, distance, star formation rate, while being careful about our uncertainties? 

# SED Fitting Validation with NIR spectroscopy 



[Prospector](https://prospect.readthedocs.io/en/latest/) is a sophisticated Bayesian framework for deriving posteriors on the properties of galaxies via sampling constrained by broadband photometry, spectroscopy, or both. In short, this code generates realistic galaxy SEDs from the `FSPS` stellar population synthesis code (Conroy et al. 2012, 2013) and compares forward modeled photometry or spectroscopy based on those SEDs to provided inputs. In doing so, the code determines the region of likely (well-fitting) models, in turn providing parameter fits and uncertainties for key galactic properties. 

![](/prospector.webp)
{.custom-css-class}

One of those properties is star formation rate (SFR). But as has been extensively investigated, every method of measuring SFR comes with some degeneracies or drawbacks, and different measures can trace different timescales of star formation as well.

A key test of any SED modeling framework that performs this kind of analysis is to predict SFR from broadband photometry alone, then compare to SFRs measured directly using the best available methods (usually spectroscopy). An [earlier paper](https://ui.adsabs.harvard.edu/abs/2017ApJ...837..170L/abstract) by my collaborator Joel Leja had found this test to be successful using comparisons with Halpha measured SFRs. 

However, Halpha nebular emission, though a strongly correlated tracer of SFR, is fairly dust-affected, and dust properties are also included in the fit. To get a better handle on this recovery test, I reduced and analyzed near infrared drift-scan spectroscopy from Palomar Observatory of a subset of the sample used in Joel's paper, a result published in a [2020 paper](../publications/brg/).

![](/brg.png)

NIR spectroscopy --- while a pain to reduce --- captures the Paschen and Brackett Hydrogen series' in the JHK bands for nearby galaxies. At ~2.16 micron, Brackett-gamma is one of the faintest, but also least dust-attenuated tracers of the same star formation traced by Halpha. Using our sample, we demonstrated that Brg alone is an extremely clean SFR measure, and that the prospector SFRs do robustly predict SFR in this gold-standard comparison. You can read more about that, and a few other takeaways, in the paper. 


# Pysersic: Bringing Bayesian statistics to galaxy light profile fitting. 

Co-developed with Tim Miller, our publicly available pysersic code is designed to allow bayesian posteriors on galaxy light modeling (e.g., the task long delegated to GALFIT). You can read more about pysersic and it's scientific uses over on my [software page](../software/pysersic/).

![](https://pysersic.readthedocs.io/en/latest/_images/example-fit_18_0.png)

# Silkscreen: Semiresolved galaxy distances from simulation based inference and convolutional neural nets

With upcoming wide field surveys from the ground and space the number of known dwarf galaxies at ≲ 20 Mpc is expected to exponentially increase. A limiting factor to scientific advancement will be measuring accurate distances to these galaxies. Traditional techniques such as tip of the red giant branch or surface brightness fluctuations are limited in their widespread applicability, especially in the semi-resolved regime. In this work we propose to use the rapidly growing field of simulation based inference to infer distances, and other physical properties, of dwarf galaxies directly from multi-band images. We use neural posterior estimation to infer the posterior distribution of parameters while simultaneously training a embedding network to extract summary statistics from the images. To train the network we employ ArtPop to simulate images of dwarf galaxies before injecting them into real images to best match the noise properties. We describe our the details of our implementation which is available as the SilkScreen python package. We apply our method to ground based survey data of globular clusters in the milky way halo, dwarf galaxies at the edge of the local group and at ∼ 10 Mpc showing the flexibility of SilkScreen to infer accurate distance to many stellar systems ranging from fully resolved to un-resolved. We discuss the limitations of the current method and discess future directions including the possibility of amortized inference to easily enable inference for thousands of dwarf galaxies. [(more)](../software/silkscreen/).
