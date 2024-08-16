---
layout: page
title: Scico
permalink: software/scico/
---

[Scientific Computational Imaging Code (SCICO)](https://github.com/lanl/scico) is a Python package for solving the inverse problems that arise in scientific imaging applications. Its primary focus is providing methods for solving ill-posed inverse problems by using an appropriate prior model of the reconstruction space. SCICO includes a growing suite of operators, cost functionals, regularizers, and optimization algorithms that may be combined to solve a wide range of problems, and is designed so that it is easy to add new building blocks. When solving a problem, these components are combined in a way that makes code for optimization routines look like the pseudocode in scientific papers. SCICO is built on top of [JAX](https://jax.readthedocs.io/en/latest/) rather than [NumPy](https://numpy.org/), enabling GPU/TPU acceleration, just-in-time compilation, and automatic gradient functionality, which is used to automatically compute the adjoints of linear operators.

## Installation

see [on-line documentation](https://scico.readthedocs.io/en/latest/install.html).

## Usage

see [github](https://github.com/lanl/scico?tab=readme-ov-file#usage-examples).

## Benchmarks

To be added...
