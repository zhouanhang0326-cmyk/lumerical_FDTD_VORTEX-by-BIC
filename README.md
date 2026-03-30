# lumerical_FDTD_VORTEX-by-BICOverview

This repository contains an Ansys Lumerical FDTD script for reproducing the Supplementary Fig. S1-type simulation from the 2020 Nature Photonics work
“Generating optical vortex beams by momentum-space polarization vortices centered at bound states in the continuum” by Bo Wang, Wenzhe Liu, Maoxiong Zhao, Jiajun Wang, Yiwen Zhang, Ang Chen, Fang Guan, Xiaohan Liu, Lei Shi, and Jian Zi. The paper was published in Nature Photonics 14, 623–628 (2020).

This script is intended for learning, academic discussion, and method reproduction only. It reproduces the Supplementary Fig. S1-style far-field behavior of BIC-enabled vortex-beam generation in a finite photonic-crystal slab using circularly polarized Gaussian-beam excitation.

## What this script does

The script builds a finite photonic-crystal slab, excites it with a circularly polarized Gaussian beam, and projects the transmitted field to selected far-field planes. It is designed to help users reproduce the generated vortex beam after extracting the cross-polarized branch, which is the physically relevant branch for the Supplementary Fig. S1-style comparison.

## Main functions

This script performs the following tasks:

Builds a finite photonic-crystal slab with a circular-hole array.
Launches a circularly polarized Gaussian beam using two orthogonal linearly polarized sources with a 90° phase delay, consistent with the standard Lumerical circular-polarization construction.
Records the near field above the slab.
Projects the field to multiple far-field planes.
Separates the transmitted field into polarization branches and extracts the generated cross-polarized beam.
Outputs far-field intensity and phase maps relevant to vortex-beam analysis.
Figures this script can output

In its full version, the script can output:

Generated beam intensity (cross-polarized branch) at selected propagation distances
Generated beam phase at selected propagation distances
Raw total Ex intensity for diagnosis
Raw total Ex phase for diagnosis
Co-polarized intensity for diagnosis
Co-polarized phase for diagnosis
Side-view intensity map assembled from multiple propagation planes
Saved .mat data files for post-processing
Which figures are the key figures

If your goal is to keep only the figures most closely related to the Supplementary Fig. S1-style result, keep only:

Generated beam intensity (cross-polarized branch)
Generated beam Ex phase / generated beam phase
Side-view of generated beam intensity

These are the most important outputs for showing whether the script reproduces the BIC-enabled vortex-beam generation effect.

How to remove nonessential plots

If you want a cleaner script that only keeps the key figures, delete or comment out the following parts:

Raw total Ex diagnostic plots
remove the image(...) commands for
Raw total Ex intensity
Raw total Ex phase
Co-polarized diagnostic plots
remove the image(...) commands for
Co-pol intensity
Co-pol phase
Raw Ex side-view
if present, remove the side-view block for the raw field
keep only the side-view block for the generated cross-polarized beam
Optional .mat saving lines
remove matlabsave(...) lines if you do not need exported data files

If you want the script to show only the most important Supplementary-Fig.-S1-style outputs, the plotting section should keep only:

the generated cross-polarized intensity maps
the generated beam phase maps
the generated-beam side-view map
Recommended short description for the repository

This repository provides an Ansys Lumerical FDTD reproduction script for the Supplementary Fig. S1-style result in the 2020 Nature Photonics paper on BIC-enabled optical vortex beam generation by the groups of Lei Shi and Jian Zi. It is intended as a learning and reproduction example for finite-array photonic-crystal-slab simulations of vortex-beam generation from momentum-space polarization vortices.

## Important usage notice

This code is provided for learning and academic reproduction only.

To run this script, users must have access to a valid Ansys Lumerical FDTD installation and license. Ansys states that its Lumerical products use licensed components and that academic licenses are restricted to academic use; Ansys academic product licenses may not be used for commercial activity. Commercial use therefore requires an appropriate Ansys license/authorization from Ansys.

##　Suggested disclaimer

Disclaimer:
This repository contains only user-level scripting for Ansys Lumerical FDTD and does not distribute Ansys software itself. This code is shared solely for educational and academic reproduction purposes. Any commercial use of this workflow requires a valid and appropriate Ansys license and authorization from Ansys. Ansys academic licenses may not be used for commercial activity.

##　Suggested citation note

If you use this script in academic work, please cite the original paper:

Wang, B., Liu, W., Zhao, M., Wang, J., Zhang, Y., Chen, A., Guan, F., Liu, X., Shi, L., & Zi, J.
Generating optical vortex beams by momentum-space polarization vortices centered at bound states in the continuum.
Nature Photonics 14, 623–628 (2020)
