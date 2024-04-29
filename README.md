# acados-python-windows
This is a slightly revisioned version of the original acados repository with the Python interface made compatible with Windows OS.

## Installation and Setup:
Make sure you have Visual Studio Community 2019 and CMake installed. Call on the following commands in the Developer Command Prompt for VS 2019:
```
https://github.com/Herpderk/acados-python-windows.git
cd acados-python-windows
git submodule update --recursive --init
mkdir build
cd build
cmake -G "Visual Studio 16 2019" -DBLASFEO_TARGET=GENERIC -DACADOS_INSTALL_DIR=.. -DACADOS_WITH_QPOASES=ON.. -DBUILD_SHARED_LIBS=ON ..
cmake --build . -j10 --target INSTALL --config Release
cd ..
pip install -e interfaces/acados_template
```
Then add ```<path_to_acados-python-windows>/lib``` to your ```Path``` environment variable as well as the following standalone environment variable:
```
ACADOS_SOURCE_DIR = <path_to_acados-python-windows>
```
All scripts running the acados Python interface must be called in the Developer Command Prompt for VS 2019 as well.

# Original Documentation:
# acados
<!-- [![Travis Status](https://secure.travis-ci.org/acados/acados.png?branch=master)](http://travis-ci.org/acados/acados) -->
[![Appveyor status](https://ci.appveyor.com/api/projects/status/q0b2nohk476u5clg?svg=true)](https://ci.appveyor.com/project/roversch/acados)
![Github actions full build workflow](https://github.com/acados/acados/actions/workflows/full_build.yml/badge.svg)
<!-- [![codecov](https://codecov.io/gh/acados/acados/branch/master/graph/badge.svg)](https://codecov.io/gh/acados/acados) -->

Fast and embedded solvers for nonlinear optimal control.

## General
- `acados` offers fast
  - fast SQP-type solvers for Nonlinear Programming (NLP) formulations with an Optimal Control Problem (OCP) structure
  - efficient integration methods to solve initial value problems
    - with ODE or index-1 DAE
    - efficient first and second-order sensitivity propagation of the results
<!-- Sequential Quadratic Programming (SQP) -->
- `acados` offers interfaces to the programming languages `C`, `Python`, `MATLAB` and `Octave`

## Documentation
- Documentation can be found on [docs.acados.org](https://docs.acados.org/)

## Forum
- Forum: If you have any `acados`-related question, feel free to post on our forum [discourse.acados.org](https://discourse.acados.org/).

## Citing
- Citing acados: references can be found [docs.acados.org/citing](https://docs.acados.org/citing).

## Installation
Instructions can be found on
[docs.acados.org/installation](https://docs.acados.org/installation)

## `acados` interfaces
`acados` written in `C` and offers interfaces to the programming languages `C`, `Python`, `MATLAB` and `Octave`.

An overview can be found at:
[docs.acados.org/interfaces](https://docs.acados.org/interfaces)
