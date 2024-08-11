### Description

* UVRのWSL2向けdocker compose(GPU対応)です.
* 特徴としては,volumes配下のフォルダはdocker内でシンボリックリンクとして扱われる為,ローカルのファイルをdocker内にいちいちコピーする必要はありません.
* Xwindowsを経由して,ウィンドウをwsl2経由でwindowsに表示できます.

### Prerequisites

* Windows 11(64GB)
* NVidia video card (RTX3060 12GB)
* WSL2 (32GB and operation confirmed on Ubuntu 20.04)

*上記以外の構成では未確認.

### Installing

* 以下のコマンドでDockerをビルド.
```
docker compose build
```

## Usage

* Installing実行後に以下を実行.
```
docker compose up
```

* ディレクトリ概要.
```
#volumes配下のリンク先.
volumes/models→ultimatevocalremovergui/models
volumes/inputs→ultimatevocalremovergui/inputs
volumes/ouputs→ultimatevocalremovergui/ouputs
```

## Version

* 2024/08/12

## Acknowledgments

* [ultimatevocalremovergui](https://github.com/Anjok07/ultimatevocalremovergui)
* [docker で cypress の gui を動かす](https://mogura.dev/articles/2022/run-cypress-gui-in-docker/)
* [nVidia 525 + Cuda 11.8 + Python 3.10 + pyTorch GPU Docker image](https://dev.to/ordigital/nvidia-525-cuda-118-python-310-pytorch-gpu-docker-image-1l4a)
* [stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) 
