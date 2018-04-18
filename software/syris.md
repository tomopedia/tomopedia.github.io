---
layout: page
title: Syris
permalink: software/syris/
---

[Syris](https://github.com/ufo-kit/syris) is a framework for simulations of
X-ray absorption and phase contrast dynamic imaging experiments, like
time-resolved radiography, tomography or laminography. It includes X-ray
sources, various sample shape creation possibilities, complex refractive index
lookup options, motion model and indirect detection model (scintillator combined
with a conventional camera). Phase contrast is simulated by the Angular spectrum
method, which enables one to include various optical elements in the simulation,
e.g. gratings and X-ray lenses.

Compute-intensive algorithms like Fourier transforms, sample shape creation and
free-space propagation are implemented by using OpenCL, which enables one to
execute the code on graphic cards.

## Installation

Download or clone the [repository](https://github.com/ufo-kit/syris) and run
`pyhon setup.py install`.

## Usage

Simulating simple white beam propagation example looks like this:

```python
import matplotlib.pyplot as plt
import numpy as np
import quantities as q
import syris
from syris.physics import propagate
from syris.bodies.simple import make_sphere
from syris.materials import make_henke

syris.init()
energies = np.arange(10, 30) * q.keV
n = 1024
pixel_size = 0.4 * q.um
distance = 2 * q.m
material = make_henke('PMMA', energies)

sample = make_sphere(n, n / 4 * pixel_size, pixel_size, material=material)
image = propagate([sample], (n, n), energies, distance, pixel_size).get()
plt.imshow(image)
plt.show()
```

## Resources

* [Documentation and API reference](http://syris.readthedocs.io/en/latest)
* [Examples](https://github.com/ufo-kit/syris/tree/master/examples)
