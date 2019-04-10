# adversarial_testing
[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/icra2018/adversarial-testing.svg)](https://hub.docker.com/r/icra2018/adversarial-testing)
<a href="#how-to-run-with-docker"><img src="https://img.shields.io/badge/Docker-instructions-brightgreen.svg"></a>
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ICRA-2018/adversarial_testing/master?urlpath=lab%2Ftree%2FREADME.ipynb)

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

# How to Run with Docker
Tested on:
* Ubuntu 16.04.6 with [Docker 18.06.1-ce](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
* macOS Mojave 10.14.3 with [Docker Desktop for Mac 2.0.0.3 (engine: 18.09.2)](https://hub.docker.com/editions/community/docker-ce-desktop-mac)
* Windows 10 Education with [Docker Desktop 2.0.0.3 (engine: 18.09.2)](https://hub.docker.com/editions/community/docker-ce-desktop-windows)

1. Open a terminal in Linux/macOS or a PowerShell in Windows and run the command:
```
docker run --rm -p 8888:8888 icra2018/adversarial-testing:latest
```
2. Run a web browser and open the link: [http://localhost:8888/lab/tree/README.ipynb](http://localhost:8888/lab/tree/README.ipynb)
