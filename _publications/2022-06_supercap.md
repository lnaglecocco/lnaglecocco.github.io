---
title: "Deciphering the In Situ Surface Reconstruction of Supercapacitive Bimetallic Ni-Co Oxyphosphide during Electrochemical Activation Using Multivariate Statistical Analyses"
collection: publications
permalink: /publication/2022-06_supercap
excerpt: 'Amina A. Saleh, Doha M. Sayed, **Liam A. V. Nagle-Cocco**, Giorgio Divitini, Loujain G. Ghanem, Caterina Ducati, and Nageh K. Allam.'
date: 2022-06-06
venue: 'ACS Applied Energy Materials'
paperurl: 'https://pubs.acs.org/doi/full/10.1021/acsaem.2c01122'
---
Amina A. Saleh, Doha M. Sayed, **Liam A. V. Nagle-Cocco**, Giorgio Divitini, Loujain G. Ghanem, Caterina Ducati, and Nageh K. Allam.

# Story

A side project I pursued in the second year of my PhD was performing nanometre-resolution Electron Energy Loss Spectroscopy (EELS) on NaNiO<sub>2</sub>, looking for differences between the surface and bulk. I was in part inspired by various interesting papers I'd read on LiNiO<sub>2</sub> where EELS, and other spectroscopies such as X-ray Absorption Spectroscopy, were used to argue for or against charge-transfer insulating behaviour (of the Zaanen-Sawatzky-Allen type) or alternatively for the formation of surface phases where the Ni<sup>3+</sup> cations were reduced to Ni<sup>2+</sup>. I worked with Dr Giorgio Divitini, then an electron microscopist in the University of Cambridge Department of Materials Science, to obtain some preliminary data. After that I spent a few weeks working out how to analyse the data and writing my own Python code, using [Hyperspy](https://hyperspy.org/), to automate the process of fitting peaks to the white lines at transition metal L edges. The most difficult parts were automating the process of deciding whether a spectrum was actually taken on a sample or whether the beam is on empty space; i.e. the grid of pixels where spectra were measured was generally larger than the particulate and so some pixels do not contain any sample. Such pixels should be excluded from analysis, but this is not so easy. From the ratio of the counts in the zero-loss peak to the counts of electrons exhibiting loss, it is possible to calculate sample thickness (in elunits of electron mean free path), and so this would be an obvious way of deciding whether a pizel contains sample, but in practice this approach is sensitive to noise and an algorithm based on this does not work so well, at least for a powder. This issue took a lot of thinking about.

After collecting the preliminary data and working out how to perform the analysis, there was a period of time where it was not possible to 


