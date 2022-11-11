# pdrs4all-PAHvsH2

Code for my paper using the [PDRs4all](https://pdrs4all.org/) data. This code is public, and
might serve as a "real world" example for the use of PAHFIT and PAHFITcube.

The paper text is in a private repository until publication.

## Main questions:
- Which AIBs (aromatic/aliphatic infrared bands) are excited by the same radiation as H2?
- Does this tell us anything about which particles could be co-spatial with H2? We know that
  there are FUV absorbing particles which are co-spatial with H2, particularly those causing the
  FUV rise features in diffuse Milky Way extinction curves, as shown in [Van De Putte et al.
  (2022)](https://ui.adsabs.harvard.edu/abs/2022arXiv221004972V/abstract).

## Method

### Core idea
Compare the spatial scales of the broad IR features and lines of vibrationally excited H2. The
latter trace a certain band of the UV radiation field. By comparing the spatial scales of the
emission, we can constrain the opacity of the AIB carriers at their excitation wavelength.

### Spatial maps

We will extract spatial maps of all features of interest, by applying
[PAHFIT](https://github.com/PAHFIT/pahfit) to the NIRSPEC and MIRI MRS mosaics of the Orion Bar.
The [PAHFITcube](https://github.com/drvdputt/PAHFIT-cube) code is being developed to do this in
an efficient manner.

We will then make cuts through these maps, and investigate the spatial scales of various
features, as inspired by [Witt et al.
(2006)](https://ui.adsabs.harvard.edu/abs/2022arXiv221004972V/abstract)

### Most important features

PAHFIT performs a simultaneous fit of all the AIBs and lines in the spectrum, and PAHFITcube
automatically makes maps for all of these features. We will consider all feature strength maps
for analysis, as long as they have a sufficient signal-to-noise (i.e. the feature strength
doesn't jump from pixel to pixel).

So far, the following things stick out:

NIR: The 3.3 and 3.4 micron features clearly have different behaviors.

MIR: No MRS data yet.
