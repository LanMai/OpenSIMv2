# OpenSIMv2
revised version of OpenSIM code

This set of code serves the same purpose as the original OpenSIM code:- the code provides a simple bare minimum generic template for SIM reconstruction from raw experimental data. No attempt is made to make the code sophisticated. The aim is "transparency", so that the user may look-into code and develop a better understanding of the basic SIM algorithm. 


Following are some remarks for using the code: 

1. SIMo.m is the main-file; rest are all function-files called by SIMo.m to carry out various tasks.

2. By default, the reconstruction results are saved in the same folder (where the code is). Three sets of reconstructions are saved:
	a) the default SIM (unapodized) reconstruction.
	b) the apodized SIM reconstruction (the apodiziation function used is same as in the original OpenSIM code).
	c) The cosine-apodized SIM reconstruction (here I have used a different apodization function, which I felt should provide better results. However, "visually" the results appear similar to the apodized SIM reconstruction.)

3. The code is essentially same as the prior OpenSIM code with the following three changes:
	a) The illumination phase estimation procedure is modified. The new method is based on Kai Wicker (2013, optic express) paper. As a consequence this code is suitable for TIRF-SIM reconstruction as well.
	b) The estimation procedure of object power spectrum is modified.
	c) The modulation factor is now estimated more accurately (by using a different procedure). The method is described in: Amit Lal, XiaoShuai Huang, and Peng Xi "A frequency domain reconstruction of SIM image using four raw images", Proc. SPIE 10024, Optics in Health Care and Biomedical Optics VII, 1002411 (31 October 2016); https://doi.org/10.1117/12.2246242.

4. Several comments are laid out at appropriate stages of the code for users assistance. An user familiar with the prior OpenSIM code may have little difficulty following this set of code. However, the user is free to contact me (amitlal25999@yahoo.com) if any additional clarification is desired.


Thanks!
