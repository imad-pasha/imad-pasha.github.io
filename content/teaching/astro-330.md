+++
title = "Astro 330: Scientific Computing for Astrophysics"
image = "a330_banner.jpg"
type = "single"
+++

![](/a330_banner.jpg)

This course (now a regular offering in the Yale Astronomy department) focuses on high level Python computing in the context of astrophysics research. The course goal is to provide students with the fundamentals of building astronomical pipelines and the general use of cutting edge tools and techniques currently used in the astronomical community. We discussed (and built) software for the analysis, manipulation, reduction, and visualization of astronomical data from observations and simulations. I created this course as a natural follow up to the primary research methods introductory class at Yale, ASTR 255 (“Research Methods in Astrophysics”). Students were expected know basic Python coding, including working with numpy arrays and creating basic plots with matplotlib, before attempting the assignments in this course.

The course (as I ran it) consisted of weekly Python lectures and in-depth tutorial/workshop days during which students worked together on programming assignments. We also held seminar lectures by invited outside experts who are pushing the forefront of Python in Astronomy. There are weekly coding assignments and a final capstone project. 

We are grateful to the speakers who met with our students - below is a running list, including some of the packages they are associated with:
- Prof. X Prochaska (UCSC; pypeit)
- Prof. David Hogg (NYU/Flatiron CCA; emcee)
- Shany Danieli (IAS/Princeton; artpop)
- Yao-Yuan Mao (Rutgers;adstex)
- Adrian Price-Whelan (CCA/Flatiron; gala,astropy)

Our course handled distribution and submission of assignments via Github classroom. Students pulled assignments (Jupyter Notebooks) from Github, worked on them, and pushed the final labs back to Github.

# Topics Covered 

**Fundamentals recap and review**

We began with an assignment which was distributed prior to the semester starting, and which focused on setting up conda environments for the students to use during the course, ensured everyone had the proper libraries installed, and reviewed basic operations such as numpy array manipulation, list comprehensions, plotting, and fitting.

**Astronomical Imaging** 

Our first core lab and lecture were focused on the analysis of astronomical images (e.g., FITS imaging from HST). The programming goals of this module were to emphasize file handling with FITS, and the creation of robust functions in Python. Students wrote functions to plot astronomical imaging which handled WCS coordinate transformations, scaling, and optional arguments for colorbars and other features. They then used array manipulation and the astropy photutils package to perform aperture photometry on sources in the provided imaging.

**Object Oriented Programming** 

From functions, we moved to Object Oriented Programming (OOP) and the construction of class objects with attributes and methods. We discussed the structure and use cases for classes, and the lab carried the students through the creation of a full pipeline to perform PSF Photometry on the stars in an image. Their pipelines, created as a series of methods for a class, performed calibrations (dark subtraction, flatfielding), background estimation and subtraction, masking of galaxies in the frame, algorithmic detection of the stars, centroiding of those stars, calculation of the second moments, and ultimately the creation of PSF models that were used to estimate the flux of each star in the frame.

### Sampling and MCMC
A key task in general astronomy research is fitting models to data. In this module, we introduced various means of fitting, from linear least squares fits using simple polynomial functions, to more complex models fit using student-built Metropolis Hastings MCMC samplers, and more complex models still fit using the popular fitting code emcee (Dan Foreman-Mackey). We spent time parsing the concept of sampling, and how it relates to the estimation of integrals, the concept of the Likelihood, the Prior, and the Evidence. In the lab, students first used Chi-squared methods to fit models to data, and then used self-made MCMC samplers to do the same. We assigned problems from two papers, Hogg, Bovy, and Lang (2010) on fitting, and Hogg & Foreman-Mackey (2018) on MCMC, then extended these with comparisons to Chi-squared fitting. Students also got their first taste of emcee here.

### Stellar Spectroscopy and MCMC Fitting

Having practiced the fundamentals of fitting and sampling in module four, we approached a more complex problem: fitting stellar spectral templates to Keck/DEIMOS data. Students used skills developed through the first three labs to sucessfully read in and modify the real and synthetic data and match their continuua and smooth the synthetic spectra to the instrumental resolution. They then used both Chi-squared and emcee to find the best fit radial velocities of the stars.

### Pandas

Pandas is a popular data management library, used often in the data science industry, which extends the functionality of basic arrays. We taught the fundamentals of creating and operating on pandas DataFrames, including row and column based indexing, filtering on conditions, and joining tables using set theory / SQL style commands. Our lab used two datasets, including the 3DHST catalog, to exemplify some of the handy features of DataFrames that would be difficult to carry out with numpy arrays. Using the pandas tools, students were able to investigate the 3DHST catalog, creating UVJ diagrams of massive galaxies in the sample conditioned on different mass ranges, redshift ranges, etc.

### Packages

At this point in the semester, students began working on their final projects, a requirement of which was that installable packages were created. We carried out an interactive lecture, which followed roughly the guide in Jo Bovy’s handbook on package development, in which the students created and installed an example package from scratch during the lecture. For their lab, students investigated the code structure, import syntax, and documentation of several astronomical software packages, namely, ArtPop (Danieli & Greco). By investigating the documentation and API reference for this unfamiliar software, students were able to create stellar populations in an odd shape (a ring) and inject this system into a real sky image. The ultimate goal was to gain familiarity with package structure, and how to write documentation useful for others using your code.

### Interactivity

Our final module focused on interactivity in Python. We focused on two areas within this topic — interactivity in matplotlib, including the use of sliders and animations, and interactive websites made using the streamlit package, which allows python scripts to seamlessly interact with buttons, sliders, and other forms of user input. A majority of the class used one of these two tools (or both) in their final projects.
