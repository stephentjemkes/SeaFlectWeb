# Problem formulation

The problem at hand is to derive from the observations the reflectance (in physical units) of the combined surface interface and ocean layer. This parameter is sensitive to the wind speed as explained before. 

The surface range bin is a composite range bin, it consists of an atmosphere, ocean layer, separated by the surface interface.

Thus the return signal from this surface range bin, contains information of these three sub-components.

To extract the combined sea surface - ocean layer reflectance from the surface range bin,  a correction of the atmospheric contribution is required.
This correction is estimated from the return signal from the lowest atmospheric layer. The calculation of this correction takes into account the differences in geometrical thickness of this atmospheric range bin, and the atmospheric sub-component of the surface range bin.

It is important that the values of the geometrical thickness of the lowest atmospheric range bin, and of the atmospheric sub-layer in the surface range bin, are accurately known.


The available Aeolus L1b data are the Mie-useful signal.
This is an array of 24 values corresponding to 24 range bins. This data is appended with the background signal, as such a total 25 data points are available.
The number of array elements is fixed. However the geometrical thickness of the corresponding range bins are not fixed and is depending on specific instrument parameters which have been changed in-orbit.
The data of interest are contained in the surface range bin. Nominally this is bin number 23.


The Mie-useful signal are counts from the ACCD detector, and are engineering units and hence are unitless.
No conversion exists to related the ACCD-counts to physical units (radiometric calibration). 

The data consistered here represent the Aeolus observations averaged over an 87 km track. This to increase the SNR.

Finally it is required that the field of view is free of clouds or aerosol content, as we are interested in the return signal from the ocean-surface.
Any contribution to the return signal from clouds-aerosol will only complicates the analysis. 

In summary a number of processing steps are required before a windspeed product can be derived from the Aeolus return signal.

The analysis of the Aeolus return signal will indicate the quality of the available data to understand if the spaceborne observations will support the theoretical relation between surface return and windspeed.

