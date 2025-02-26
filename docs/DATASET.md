### Dataset structure
For simplicity, our datasets are structured in the following way:
```
/Uni-Sign/dataset/
├── CSL_News
│   ├── rgb_format # mp4 format
│   │   ├── Common-Concerns_20201113_0-287_14330.mp4 
│   │   ├── Common-Concerns_20201113_1562-2012_239580.mp4
│   │   └── ...
│   │ 
│   └── pose_format # pkl format
│       ├── Common-Concerns_20201113_0-287_14330.pkl 
│       ├── Common-Concerns_20201113_1562-2012_239580.pkl
│       └── ...
│      
├── CSL_Daily
│   ├── Archive/ 
│   ├── label/ 
│   ├── sentence-crop # mp4 format
│   │   ├── S005870_P0006_T00.mp4
│   │   ├── S005870_P0009_T00.mp4
│   │   └── ...
│   │ 
│   └── pose_format # pkl format
│       ├── S005870_P0006_T00.pkl
│       ├── S005870_P0009_T00.pkl
│       └── ...
│      
├── WLASL
│   ├── rgb_format # mp4 format
│   │   ├── train/
│   │   ├── val/
│   │   └── test
│   │       ├── 64550.mp4
│   │       ├── 64551.mp4
│   │       └── ...
│   │   
│   └── pose_format # pkl format
│       ├── train/
│       ├── val/
│       └── test
│           ├── 64550.pkl
│           ├── 64551.pkl
│           └── ...
```

#### Note: 
* You first need to download the [mt5-base](https://huggingface.co/google/mt5-base) weights, and place them in the `./pretrained_weight/mt5-base`.
* Download the [CSL-News](https://huggingface.co/datasets/ZechengLi19/CSL-News/tree/main), [CSL-Daily](https://ustc-slr.github.io/datasets/2021_csl_daily/), and [WLASL](https://github.com/dxli94/WLASL) datasets based on your requirements.
* The pose_format folders for the CSL-Daily and WLASL datasets can be downloaded from [here](https://huggingface.co/ZechengLi19/Uni-Sign), which are extracted using the RTMPose from MMPose.
* The Uni-Sign checkpoints can be found [here](https://huggingface.co/ZechengLi19/Uni-Sign).
* If the datasets or mt5 checkpoint are stored in different paths, you can modify the `config.py` file to specify the new paths.
