---
layout: page
title: TIGRE toolbox
permalink: software/tigre/
---

The Tomographic Iterative GPU-based Reconstruction (TIGRE) toolbox is a MATLAB-CUDA toolbox for fast iterative recosntruction of 3D tomographic images. It supports cone and parallel X-ray sources and it has a flexible geomtry (arbitrary axis of rotation, offsets, pixel sizes, etc). TIGRE is easy to use and features over 10 iterative algorithms in addition to the classic filtered backprojection algorithms. 

A python of TIGRE versions is in building stage.

Learn more in the [open access paper](http://iopscience.iop.org/article/10.1088/2057-1976/2/5/055010) or in the [main Github repo](https://github.com/CERN/TIGRE).

## Installation

Dowload the toolbox in [main Github repo](https://github.com/CERN/TIGRE). 

[Install CUDA](https://developer.nvidia.com/cuda-downloads) (the latests the better).

Install a [supported MATLAB compiler](https://uk.mathworks.com/support/sysreq/previous_releases.html) for your OS and MATLAB version.
Remember to check [if its compatible with CUDA too](http://docs.nvidia.com/cuda/cuda-compiler-driver-nvcc/index.html#supported-host-compilers).

Run `Compile` in MATLABs command line and you are good to go.

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
recosntruction= ALGORITHM_NAME(projections,geo,projection_angles, numebr_iterations);
```

Learn more in [the demos](https://github.com/CERN/TIGRE/tree/master/MATLAB/Demos). 

## Benchmarks

Comparing to [ASTRA](https://tomopedia.github.io/software/astra/), TIGRE has similar backprojection speeds and sligthly slower (but same order of magnitude) projection speeds. 

The tierative algorithms themselves are slower, due to the optimized architecture of ASTRA, and the modular architecture of TIGRE. 

Runtime numbers to be added...
