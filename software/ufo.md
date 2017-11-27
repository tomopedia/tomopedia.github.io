---
layout: page
title: UFO reconstruction
permalink: software/ufo/
---

UFO is a small run-time [core](https://github.com/ufo-kit/ufo-core) written in C
with bindings to Python as well as a comprehensive plugin
[suite](https://github.com/ufo-kit/ufo-filters) for general image processing as
well as for tomographic reconstruction. It utilizes one or more GPUs to improve
the reconstruction throughput.


## Installation

Installation procedures for Linux and MacOS are documented in the online
[manual](https://ufo-core.readthedocs.io).


## Usage

Without writing any code, pipelines can be constructed and executed from the
command line using the `ufo-launch(1)` tool. For example, to store all TIFF
files from a directory in an HDF5 file, you can run

```bash
ufo-launch read path="directory/*.tif" ! write filename=output.hdf5:/path/in/file
```

A basic reconstruction pipeline using the filtered backprojection algorithm
using pre-generated sinograms could look like this

```bash
ufo-launch read path=sinograms/ ! fft ! filter ! ifft ! backproject ! write filename=slices/slice-%05i.tif
```

## Benchmarks

All results were obtained by reconstructing 2048 slices from 2048 sinograms each
with a width of 2048 pixels and 2048 projection angles. No actual data was read
or written, just the sinograms filtered and then backprojected.

{: .table .table-striped}
| Configuration             | Mean time (s) | Rate (slices/s) |
|---------------------------|--------------:|----------------:|
| 4× NVIDIA GTX 1080 TI     |         28.72 |            71.3 |
| 7× NVIDIA GTX TITAN       |         54.66 |            37.5 |
| 2× NVIDIA Quadro M6000    |         61.59 |            33.3 |
| 1× NVIDIA P100            |         84.32 |            24.3 |
| 4× NVIDIA GTX TITAN       |        101.02 |            20.3 |
| 2× NVIDIA Tesla K20Xm     |        132.52 |            15.5 |
| 1× AMD FirePro W9100      |        159.51 |            12.8 |
| 1× NVIDIA GTX TITAN Black |        197.54 |            10.4 |
