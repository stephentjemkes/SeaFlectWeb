# Problem formulation

The problem at hand is to derive from the observations the reflectance (in physical units) of the combined surface interface and ocean layer, as this parameter is sensitive to the wind speed. Under low windspeed conditions this reflectance is small and dominated by the reflectance of the ocean layer. With increasing windspeed the white cap fraction increases. As white caps are bright, an increasing white cap fraction will result in an increase of the return signal. 

The Aeolus L1b datastream provides the Mie-useful signal which is the so-called ACCD counts, for 24 range bins. This data is appended with the background signal. A total 25 elements are available. The data consistered here represent the Aeolus observations averaged over an 87 km track. This to increase the SNR.

The ACCD counts are engineering units and hence are unitless.

Furthermore the data of interest are contained in the surface range bin. Nominally this is bin number 23. The surface range bin is a composite layer, and consists of an atmospheric layer, the sea surface and an ocean layer. The thickness of these layers are not fixed, as instrument parameters which determine this are changing during in-orbit. 

To extract the combined sea surface - ocean layer reflectance from the surface range bin, requires a correction of the atmospheric contribution. This contribution is estimated from the return signal from the lowest atmospheric layer, after a correction of the thickness of the atmospheric layers. 

This implies that the thickness of the atmospheric sub-layer in the surface range bin, and of the lowest atmospheric layer are accurately knowns.

Furthermore it is assumed that the field of view is free of clouds or aerosol content, as we are interested in the return signal from the ocean-surface. Any contribution to the return signal from clouds-aerosol will only complicates the analysis. 
