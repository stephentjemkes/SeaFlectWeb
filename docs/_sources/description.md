# Description of the Analysis


## Dataset

The Aeolus dataset considered here is the so-called Mie useful signal (L1B data product). This signal is the Accumulated Charged Coupled Device (ACCD), which is an engineering unitless parameter. the ACCD-counts is provided for 24 layers. The interfaces of these layers are determined by the delay time of the return signal, i.e. the time it takes between sending and receiving the laser pulse. The nominal stratification of these layers is as follows, starting from the bottom: one pure ocean range bin (range bin 24), a composite range bin which contains an ocean layer, the sea surface and an atmospheric layer (range bin 23) and then 22 pure atmospheric layers. Here we consider the three lowest range bins. The 24 ACCD counts are complemented with a 25 parameter which contains the measured background signal. This data is also used for the diagnostic analysis. In summary the nominal numbers of the range bins considered here are in the next table

Number | Description
-------| ----------------
22 | Lowest pure atmospheric layer
23 | Surface layer
24 | Top most pure ocean layer
25 | Background signal


The thickness of the range bins are configurable parameters and they have been changed in-orbit. The number of layers is a fixed number. 

The ACCD data comes in two two spatial resolution. There is one low spatial resolution dataset which represents the ACCD counts over an area of 87 km, and there is one high spatial resolution dataset, which represents the ACCD counts over an area of 3 km. For the presented analysis the course spatial resolution dataset has been considered.



## Definitions

To follow the discussion presented here a number of variables are used. 

Variable  | Meaning                                                                               |
:-------- | :-------------------------------------------------------------------------------------|
$R_{aso}$ | Reflectance of the surface range bin                                                  |
$R_{so}$  | Combined reflectance of the sea-surface and ocean sub-layer                           |
$R_{a}$   | Reflectance of an atmospheric layer                                                   |
$\Upsilon_{aso}$ | The Accumulated Charged Coupled Device (ACCD) counts of the surface range bin  |
$\zeta$ | The altitude of the upper boundary of the range gate [m]                                       |
$\Gamma$ | The range of a range gate [m] |

A a number superscript indicates the specific range bin, the nominal numbers are presented in the previous table.


## Objective

The objective of the processing chain is to derive $R_{so}$ from $R_{aso}$. This requires a transformation from $\Upsilon_{aso}$ to the reflectance values $R_{aso}$, and further remove the atmospheric contribution $R_{a}^{23}$. This is done using $R_{a}^{22}$ after correcting this reflectance for layer difference. 

The correction methodology itself is described below, but in general terms is based on a simple conceptual model which involves a standard approach to describe atmospheric multiple scattering. This conceptual model (CM), makes use of the the transmission of an atmospheric layer ${\cal T}$ which is a function of the number of molecules in a layer, so in general

$${\cal T} = F\left( N_{molecules}\right) = F\left( P, T\right)$$

For the moment a fixed values for ${\cal T}$ is assumed. The conceptual model is described in more detail later.


## Region of Interest

The analysis is performed for a number of regions over the global oceans. These regions are characterised by a chlorophyl content which is relatively stable over time. In particular we consider the South Pacific gyre which contains the "cleanest" water on earth and the Southern Storm track regions.  The latter is included to have a large dynamical range of observed wind speeds. 

## Period of interest

The analysis considers the Aeolus observations for a 12 month period starting from september 2019.

## Outline

What follows next is a walk through of the various variables required for the processing from ACCD-counts to surface reflectance extracted from the level 1b product stream for the region "E" (the south pacific gyre) for the entire period.

In summary the layer thickness, the ACCD-counts and quality control parameters are analysed in the next pages.
The conversion from ACCD-counts to physical parameters is not part of the analysis.

### Use of the notebook

The figures presented in the notebook are interactive, tools to analyse details of the figures are presented at the top right of each figure. 

To facilitate an easier flow of the results, the python code used to generate the figures, is hidden.
But they can be viewed by clicking on the icon if more details of the spacific scripts are needed.

