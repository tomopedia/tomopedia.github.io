---
layout: page
title: ToMoBAR (Tomographic Model BAsed Reconstruction)
permalink: software/tomobar/
---

ToMoBAR is a Python library of direct and model-based regularised iterative reconstruction algorithms with a plug-and-play capability for parallel-beam geometry. ToMoBAR offers you a selection of various data models and regularisers resulting in complex objectives for tomographic reconstruction. ToMoBAR can operate on a GPU device in a device-to-device fashion (in-memory) using CuPy API, therefore ensuring a better computational efficiency. This is especially relevant for iterative algorithms where multiple projection/backprojection and image filtering (e.g. [regularisation](https://github.com/vais-ral/CCPi-Regularisation-Toolkit)) operations are in place.

With the GPU device controlling API exposed, it can also support multi-GPU parallel computing. This functionality is exploited by the [HTTomo](/software/httomo/) UI software through MPI protocols and parallel HDF5.


## Installation

Please see the detailed instructions [here](https://dkazanc.github.io/ToMoBAR/howto/installation.html).

## Usage

Please see various [tutorials](https://dkazanc.github.io/ToMoBAR/tutorials/direct_recon.html) on direct and iterative reconstruction.  

## Benchmarks

As ToMoBAR relies on [ASTRA](/astra/) toolbox modules, one can expect a similar to ASTRA performance. The speed-up (up to 5 times) can be achieved by using CuPy implementations of the advanced iterative methods with regularisation (see [FISTA](https://dkazanc.github.io/ToMoBAR/api/tomobar.methodsIR_CuPy.html#tomobar.methodsIR_CuPy.RecToolsIRCuPy.FISTA)), instead of the host-device-host versions.
