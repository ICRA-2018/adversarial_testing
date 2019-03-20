# adversarial_testing
<a href="#roslab-run"><img src="https://img.shields.io/badge/ROSLab-run-brightgreen.svg"></a>

This is a python package for testing controllers for black box system in simulators

# Installation
To install, 
```
python3 setup.py install --user
```
This should allow you to use the package anywhere in your current environment

# Tests
The tests folder has 3 files:
- test_sincos.py : This file shows the difference between modeling smooth and non-smooth functions using GPy
- test_car.py: This file implements a simple linear controller on a car for obstacle avoidance. This file shows how we use KernelPCA for reducing the input space.
- test_cartpole.py: This file tests a nearest neighbor controllder code submitted by user for the Open AI Gym environment Cartpole-v0

# ROSLab Run

## Prerequisites:
* [Docker](https://www.docker.com/)
* [nvidia-docker](https://github.com/nvidia/nvidia-docker/wiki/Installation-(version-2.0))
* Tested on Ubuntu Linux 16.04, Docker version 18.06.1-ce, NVIDIA Driver version 410.48.

## 1. Clone the repository and build ROSLab image:
```
git clone https://github.com/ICRA-2018/adversarial_testing.git
cd adversarial_testing
./roslab_build
```
## 2. Launch ROSLab image:
```
./roslab_run
```
## 3. Open JupyterLab in your browser:
[http://localhost:8888/lab/tree/README.ipynb](http://localhost:8888/lab/tree/README.ipynb)

## 4. Run in JupyterLab:

Open a test notebook and run all the cells.

- [test_sincos](test_sincos.ipynb) : This notebook shows the difference between modeling smooth and non-smooth functions using GPy
- [test_car](test_car.ipynb): This notebook implements a simple linear controller on a car for obstacle avoidance. This file shows how we use KernelPCA for reducing the input space.
