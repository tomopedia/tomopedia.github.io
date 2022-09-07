---
layout: page
title: TIGRE toolbox
permalink: software/tigre/
---

The Tomographic Iterative GPU-based Reconstruction (TIGRE) toolbox is a MATLAB/Python-CUDA toolbox for fast iterative recosntruction of 3D tomographic images. It supports cone and parallel X-ray sources and it has a flexible geometry (arbitrary axis of rotation, offsets, pixel sizes, etc). TIGRE is easy to use and features over 10 iterative algorithms in addition to the classic filtered backprojection algorithms. 

Algorithms in TIGRE include:

 - Filtered backprojection (FBP,FDK) and variations (different filters, Parker weights, ...)

 - Gradient-based algorithms (SART, OS-SART, SIRT) with multiple tuning parameters (Nesterov acceleration, initialization, parameter reduction, ...)

 - Krylov subspace algorithms (CGLS)

 - Statistical reconstruction (MLEM)

 - Total variation regularization based algorithms: proximal-based (FISTA, SART-TV) and POCS-based (ASD-POCS, OS-ASD-POCS, B-ASD-POCS-β, PCSD, AwPCSD, Aw-ASD-POCS)

TIGRE supports Multi-GPU computing, and larger-than GPU computing (if your problem doesnt fit in the GPU, it will split it in pieces and compute partial chuncks at a time).

Learn more in the [open access paper](http://iopscience.iop.org/article/10.1088/2057-1976/2/5/055010) or in the [main Github repo](https://github.com/CERN/TIGRE).

## Installation

Follow the instructions at TIGRE, for [MATLAB](https://github.com/CERN/TIGRE/blob/master/Frontispiece/MATLAB_installation.md) or [python](https://github.com/CERN/TIGRE/blob/master/Frontispiece/python_installation.md).


You will need [CUDA](https://developer.nvidia.com/cuda-downloads) and a C++ compiler supported. Check the links avobe to find out which compiler you need for each OS/language.


## Usage

Define your geometry as: 

```
%% Geometry structure definition.	 
% Distances	 
geo.DSD = 1536;	                              % Distance Source Detector
geo.DSO = 1000;	                              % Distance Source Origin
% Detector parameters	 
geo.nDetector = [512; 512];	                  % number of pixels
geo.dDetector = [0.8; 0.8];	                  % size in mm of each pixel
geo.sDetector = geo.nDetector.*geo.dDetector;	% total size of the detector in mm
% Image parameters	 
geo.nVoxel = [512;512;512];                 	% number of voxels in the image
geo.sVoxel = [256;256;256];	                  % total size of the image in mm
geo.dVoxel = geo.sVoxel./geo.nVoxel;	        % size in mm of each voxel
% Offsets	 
geo.offOrigin = [0; 0; 0];	                  % Offset of the image from origin (per projection)         
geo.offDetector = [0; 0];                     % Offset of detector (per projection)
```

And call your algorithms as:

```
reconstruction= ALGORITHM_NAME(projections,geo,projection_angles, numebr_iterations);
```

Learn more in [the demos](https://github.com/CERN/TIGRE/tree/master/MATLAB/Demos). 

## Benchmarks

The latest TIGRE article (has a comparison vs ASTRA)[https://www.sciencedirect.com/science/article/pii/S0743731520303336]. The short version is that they are approximately the same speed, but TIGRE is much faster at very large scale tomography. 
