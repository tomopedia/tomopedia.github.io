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
