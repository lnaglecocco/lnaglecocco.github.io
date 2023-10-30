---
title: "Deciphering the In Situ Surface Reconstruction of Supercapacitive Bimetallic Ni-Co Oxyphosphide during Electrochemical Activation Using Multivariate Statistical Analyses"
collection: publications
permalink: /publication/2022-06_supercap
excerpt: 'Amina A. Saleh, Doha M. Sayed, **Liam A. V. Nagle-Cocco**, Giorgio Divitini, Loujain G. Ghanem, Caterina Ducati, and Nageh K. Allam'
date: 2022-06-06
venue: 'ACS Applied Energy Materials'
paperurl: 'https://pubs.acs.org/doi/full/10.1021/acsaem.2c01122'
---
Amina A. Saleh, Doha M. Sayed, **Liam A. V. Nagle-Cocco**, Giorgio Divitini, Loujain G. Ghanem, Caterina Ducati, and Nageh K. Allam.

Published on 6th June 2022, and available [https://pubs.acs.org/doi/full/10.1021/acsaem.2c01122](here).

# Story

A side project I pursued in the second year of my PhD was performing nanometre-resolution Electron Energy Loss Spectroscopy (EELS) on NaNiO<sub>2</sub>, looking for differences between the surface and bulk. I was in part inspired by various interesting papers I'd read on LiNiO<sub>2</sub> where EELS, and other spectroscopies such as X-ray Absorption Spectroscopy, were used to argue for or against charge-transfer insulating behaviour (of the Zaanen-Sawatzky-Allen type) or alternatively for the formation of surface phases where the Ni<sup>3+</sup> cations were reduced to Ni<sup>2+</sup>. I worked with Dr Giorgio Divitini, then an electron microscopist in the University of Cambridge Department of Materials Science, to obtain some preliminary data. After that I spent a few weeks working out how to analyse the data and writing my own Python code, using [Hyperspy](https://hyperspy.org/), to automate the process of fitting peaks to the white lines at transition metal L edges. The most difficult parts were automating the process of deciding whether a spectrum was actually taken on a sample or whether the beam is on empty space; i.e. the grid of pixels where spectra were measured was generally larger than the particulate and so some pixels do not contain any sample. Such pixels should be excluded from analysis, but this is not so easy. From the ratio of the counts in the zero-loss peak to the counts of electrons exhibiting loss, it is possible to calculate sample thickness (in units of electron mean free path), and so this would be an obvious way of deciding whether a pixel contains sample, but in practice this approach is sensitive to noise and an algorithm based on this does not work so well, at least for a powder. This issue took a lot of thinking about.

At the time, Giorgio was working with an Egyptian PhD student, Amina Saleh, who had visited Cambridge and collected a lot of EELS data on her supercapacitor materials, and who had similar analysis needs to my NaNiO<sub>2</sub> project – he put us in touch. We had a Zoom call and concluded that my code would indeed be useful for her project. I had to reconfigure my code to work with the Co edge, and the proximity of the Co edge to the Ni edge in her supercapacitor material meant that the precise algorithms I had used for the Ni L edge needed to be modified, but ultimately the code was effective at dealing with the data. Emails were exchanged, over several months, to fine tune my process and make sure I was getting the information Amina wanted. Ultimately I produced a set of colour-coded map plots and histograms, and these made it into the paper Amina was writing.

![Peak fitting at L edges](/images/SalehPaper_fig.png)
