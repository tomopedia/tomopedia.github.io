---
layout: page
title: HTTomo (High Throughput Tomography pipeline)
permalink: software/httomo/
---

HTTomo stands for High Throughput Tomography pipeline for processing and reconstruction of parallel-beam tomography data in Python. The HTTomo project was initiated in 2022 at [Diamond Light source](https://www.diamond.ac.uk/) by Tomography Team. With the [Diamond-II](https://www.diamond.ac.uk/Home/About/Vision/Diamond-II.html) upgrade approaching, there is a need to be able to process bigger data in larger quantities and with high fidelity. With the support of modern developments in the field of High Performance Computing and multi-GPU processing, it is possible to enable faster data streaming and higher throughput for big data.

The main [concept](https://diamondlightsource.github.io/httomo/introduction/about.html) of HTTomo is to split the data stored as HDF5 files into three-dimensional (3D) chunks that would fit into a GPU memory available and process them in parallel on one or multiple devices.

As a UI, HTTomo exploits [YAML](https://diamondlightsource.github.io/httomo/reference/yaml.html) for [pipelines](https://diamondlightsource.github.io/httomo/tutorials/yaml.html) or process lists construction.

HTTomo fully relies on the [backends](https://diamondlightsource.github.io/httomo/backends/list.html) for data processing and does not contain any algorithms.

## Installation

Please see the detailed instructions [here](https://diamondlightsource.github.io/httomo/howto/installation.html).

## Usage

Please see the examples how to [run](https://diamondlightsource.github.io/httomo/howto/run_httomo.html) HTTomo from the command line inside the shell. 

## Benchmarks

To be added...
