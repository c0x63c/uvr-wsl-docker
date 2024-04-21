### Description

* This is a docker compose (GPU support) for WSL2 of UVR.
* Folders under volumes are treated as symbolic links in docker, so you don't need to copy local files into docker.
* windows can be displayed on windows via wsl2 via Xwindows.

### Prerequisites

* Windows 11(64GB)
* NVidia video card (RTX3060 12GB)
* WSL2 (32GB and operation confirmed on Ubuntu 20.04)

*Not confirmed in other configurations than those listed above.

### Installing

* Build Docker with the following command
```
docker compose build
```

## Usage

* After installing, do the following.
```
docker compose up
```

* Directory Overview.
```
#links under volumes.
volumes/models→ultimatevocalremovergui/models
volumes/inputs→ultimatevocalremovergui/inputs
volumes/ouputs→ultimatevocalremovergui/ouputs
```

## Version

* 2024/04/21

## Acknowledgments

* [ultimatevocalremovergui](https://github.com/Anjok07/ultimatevocalremovergui)
* [nVidia 525 + Cuda 11.8 + Python 3.10 + pyTorch GPU Docker image](https://dev.to/ordigital/nvidia-525-cuda-118-python-310-pytorch-gpu-docker-image-1l4a)
* [docker で cypress の gui を動かす](https://mogura.dev/articles/2022/run-cypress-gui-in-docker/)
