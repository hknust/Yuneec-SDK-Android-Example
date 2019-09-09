# Running SITL in Docker

## Description

This is an example of running SITL headless in a Docker container.

## Building the docker image

From this directory, run:

`$ docker build -t yuneec-sitl .`

An image called `yuneec-sitl` should be created. Note that the latest version of the SITL simulator is downloaded at that point.

## Running a SITL container

Run the following command:

`$ docker run -it yuneec-sitl`

More details on how to use the SITL simulation can be found [here](https://github.com/YUNEEC/Yuneec-SDK-Android-Example-prerelease#run-the-simulation).

## Running SITL with GUI in Docker (NVIDIA only)

Requires [CUDA 9 or 10](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html), [Docker CE 19.03 or newer](https://docs.docker.com/install/) together with the [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-docker) installed on the host machine.

Test the successful installation with

`$ docker run --gpus all nvidia/cuda:10.0-base nvidia-smi`

If you see the `nvidia-smi` output, launch the SITL appklication with

`$./launch-sitl`
