## Requirements

* Ubuntu 16.04 or windows
* Python 3.6
* PyTorch 0.4.1 (should also work with 1.0, but not tested)

## Prerequisites

1. Download COCO 2017 dataset: [http://cocodataset.org/#download](http://cocodataset.org/#download) (train, val, annotations) and unpack it to `<COCO_HOME>` folder.
2. Install requirements `pip install -r requirements.txt`

## Python Demo <a name="python-demo"/>

* `python demo.py --checkpoint-path .\<model path> --video .\<video path>`


## 說明:
在pose.py修改路徑到你要的即可將照片儲存至你要的path

##官方model
https://download.01.org/opencv/openvino_training_extensions/models/human_pose_estimation/checkpoint_iter_370000.pth 
```
