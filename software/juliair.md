---
layout: page
title: JuliaImageRecon
permalink: software/juliair/
---

[Julia](https://en.wikipedia.org/wiki/Julia_(programming_language))
is an open-source language
that solves the "2 language" problem
by being both interactive yet fast.

Rather than collecting numerous functions
under a single umbrella,
like the
[Michigan Image Reconstruction Toolbox (MIRT)](https://github.com/JeffFessler/MIRT),
software packages in Julia tend to be modular and inter-operable
and used in an "a la cart" way.
The
[JuliaImageRecon](https://github.com/JuliaImageRecon)
organization on github
is a growing collection of packages
written in the Julia language
for image reconstruction problems.

See the
[About](https://github.com/JuliaImageRecon/About)
and
[Examples](https://github.com/JuliaImageRecon/Examples)
repos there
for more information.

The most relevant package here is
[Sinograms.jl](https://github.com/JuliaImageRecon/Sinograms.jl)
that has FBP and FDK algorithms currently
and will eventually have forward and back-projectors
for iterative reconstruction.


## Installation

See the instructions here:
<https://juliaimagerecon.github.io/Examples>


## Usage

The packages all include documentation and visual examples
that are generated automatically
as part of the continuous integration process.
For a FDK example,
see
<https://juliaimagerecon.github.io/Sinograms.jl/dev/generated/examples/07-fdk>


## Benchmarks

Julia has convenient tools
for using GPU acceleration
and these will be added...
