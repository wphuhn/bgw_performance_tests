# BerkeleyGW Test

## Contents

These input files were last tested on 22 January, 2021 with BerkeleyGW commit
0fadcaa0.

### Mean-Field Input Files

Due to the large size of the mean-field input files, you will need to obtain
them from another source.  The files you will need, as well as the MD5 sums,
for the SiC calculations are:
```
652278964f8cdfe032e3a43cbb739bac  ./mean_field/SiC/RHO
96219d58766e6e9b6ad532e857d246d8  ./mean_field/SiC/vxc.dat
94f37dd7bc047f9f64c7551cb949c200  ./mean_field/SiC/WFN.h5
3f1f0de1773bf99d1cdbe96011ea23d7  ./mean_field/SiC/WFN_inner
5a49db5b0b97602a523fdc051da5836c  ./mean_field/SiC/WFNq.h5
```
and the files you will need for the Si214 calculations are
```
83526815d8a53cebb7ed08e54bd20637  ./mean_field/Si214/RHO
b834da576a1b8fd9ddf195495fbc3db4  ./mean_field/Si214/VXC
f895468482834628e50db7f64f6f7827  ./mean_field/Si214/WFN.h5
de22f4d48dfcc4a2fd8949173e9a8ef7  ./mean_field/Si214/WFN_inner
dcf016ca900cf1ec6c1a6c3b4ee9a78f  ./mean_field/Si214/WFNq.h5
```

### SiC\_GPP

SiC 2-atom unit cell, computing the static inverse dielecric matrix in Epsilon
and using the Generalized Plasmon Pole (GPP) model for the inverse dielectric
matrix in Sigma.

This calculation is intended to run in ~30 seconds on a single CPU core.

### SiC\_FF

SiC 2-atom unit cell, computing the full frequency dependent inverse dielectric
matrix in Epsilon and using the Full Frequency (FF) model for the inverse
dielectric matrix in Sigma.

This calculation is intended to run in ~30 seconds on a single CPU core.

### Si214\_GPP

Si 214-atom supercell, computing the static inverse dielecric matrix in Epsilon
and using the Generalized Plasmon Pole (GPP) model for the inverse dielectric
matrix in Sigma.

This calculation is intended to run in ~minutes for full utilization of a
Summit-sized nodes.

### Si214\_FF

Si 214-atom supercell, computing the full frequency dependent inverse dielectric
matrix in Epsilon and using the Full Frequency (FF) model for the inverse
dielectric matrix in Sigma.

This calculation is intended to run in ~minutes for full utilization of a
Summit-sized nodes.

## Running

* Obtain the mean-field input files and make sure that their location and MD5
  checksums are correct (see above).
* `cp make.sys.template make.sys`, then modify `make.sys` to correspond to your
  local environment
* `cd` into the folder for the calculation of your choice
* `make` to run a full BerkeleyGW calculation, or `make X` to run a particular
  stage (i.e. `make sigma` to run the Sigma stage)
    * Note: to run any stage other than EPSILON, you must first run EPSILON
      (`make epsilon`) to generate `epsmat.h5` and `eps0mat.h5`.
