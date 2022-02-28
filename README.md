# Real-time 2D Multi-Person Pose Estimation on CPU: Lightweight OpenPose

This repository contains training code for the paper [Real-time 2D Multi-Person Pose Estimation on CPU: Lightweight OpenPose](https://arxiv.org/pdf/1811.12004.pdf). This work heavily optimizes the [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose) approach to reach real-time inference on CPU with negliable accuracy drop. It detects a skeleton (which consists of keypoints and connections between them) to identify human poses for every person inside the image. The pose may contain up to 18 keypoints: ears, eyes, nose, neck, shoulders, elbows, wrists, hips, knees, and ankles. On COCO 2017 Keypoint Detection validation set this code achives 40% AP for the single scale inference (no flip or any post-processing done). The result can be reproduced using this repository. *This repo significantly overlaps with https://github.com/opencv/openvino_training_extensions, however contains just the necessary code for human pose estimation.*

<p align="center">
  <img src="data/preview.jpg" />
</p>

:fire: Check out our [new work](https://github.com/Daniil-Osokin/gccpm-look-into-person-cvpr19.pytorch) on accurate (and still fast) single-person pose estimation, which ranked 10<sup>th</sup> on CVPR'19 [Look-Into-Person](http://47.100.21.47:9999/index.php) challenge.

:fire::fire: Check out our lightweight [3D pose estimation](https://github.com/Daniil-Osokin/lightweight-human-pose-estimation-3d-demo.pytorch), which is based on [Single-Shot Multi-Person 3D Pose Estimation From Monocular RGB](https://arxiv.org/pdf/1712.03453.pdf) paper and this work.

## Table of Contents

* [Requirements](#requirements)
* [Prerequisites](#prerequisites)
* [Training](#training)
* [Validation](#validation)
* [Pre-trained model](#pre-trained-model)
* [C++ demo](#cpp-demo)
* [Python demo](#python-demo)
* [Citation](#citation)

### Other Implementations

* TensorFlow by [murdockhou](https://github.com/murdockhou/lightweight_openpose).
* OpenVINO by [Pavel Druzhkov](https://github.com/openvinotoolkit/open_model_zoo/pull/1718/).

## Requirements

* Ubuntu 16.04
* Python 3.6
* PyTorch 0.4.1 (should also work with 1.0, but not tested)

## Prerequisites

1. Download COCO 2017 dataset: [http://cocodataset.org/#download](http://cocodataset.org/#download) (train, val, annotations) and unpack it to `<COCO_HOME>` folder.
2. Install requirements `pip install -r requirements.txt`

## Python Demo <a name="python-demo"/>

* `python demo.py --checkpoint-path .\<model path> --video .\<video path>`


## Citation:

If this helps your research, please cite the paper:

```
@inproceedings{osokin2018lightweight_openpose,
    author={Osokin, Daniil},
    title={Real-time 2D Multi-Person Pose Estimation on CPU: Lightweight OpenPose},
    booktitle = {arXiv preprint arXiv:1811.12004},
    year = {2018}
}
```
