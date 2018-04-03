---
layout: page
title: Operator Discretization Library (ODL)
permalink: software/odl/
---

ODL
===
*Operator Discretization Library* (ODL) is a Python library that enables research in inverse problems on realistic or real data. The framework allows to encapsulate a physical model into an `Operator` that can be used like a mathematical object in, e.g., optimization methods. Furthermore, ODL makes it easy to experiment with reconstruction methods and optimization algorithms for variational regularization, all without sacrificing performance.

For more details and an introduction into the inner workings of ODL, please refer to the [documentation](https://odlgroup.github.io/odl/).

Highlights
==========
- Well-tested data containers based on NumPy or CUDA allow high performance computing with minimal effort.
- A versatile and efficient library of optimization routines for smooth and non-smooth problems, such as CGLS, BFGS, PDHG and Douglas-Rachford splitting.
- Support for tomographic imaging with a unified geometry representation and bindings to external libraries for efficient computation of projections and back-projections.
- And much more, including support for deep learning libraries, figures of merits, phantom generation, data handling, etc.

Installation
============
Installing ODL should be as easy as

    conda install -c odlgroup odl

or

    pip install odl

For more detailed instructions, check out the [Installation guide](https://odlgroup.github.io/odl/getting_started/installing.html).

ODL is compatible with Python 2/3 and all major platforms (GNU/Linux / Mac / Windows).

Resources
=========
- [ODL Documentation](https://odlgroup.github.io/odl/)
- [Installation guide](https://odlgroup.github.io/odl/getting_started/installing.html)
- [Getting Started](https://odlgroup.github.io/odl/getting_started/getting_started.html)
- [Code Examples](examples)
- [API reference](https://odlgroup.github.io/odl/odl.html)
- [ODL Course Material](https://github.com/odlgroup/odlworkshop)
