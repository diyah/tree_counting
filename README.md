# Tree Counting Assignment
This folder project is organized as follows
```
│   counting.ipynb
│   README.md
│   Theoritical assignment.pdf
│   tree_counting_modeling.ipynb
│
├───config
│       tree_cfg.yml
├───data
│   ├───raw
│   ├───train
│   │   ├───images
│   │   └───labels
│   ├───val
│   │   ├───images
│   │   └───labels
│   └───video
├───model
│   └───weights
└───predict
```

Notebook `counting.ipynb` containts code for counting and classifying tree (assignment 1). 
For theoritical assigment both `Neural Network Theory` and `Gradient Descent Theory` the answers are in file `Theoritical assignment.pdf`
 
## Installation
To be able to run the notebooks kindly do the following
* Setup a Python 3.11
* Install PyTorch for torchvision corresponding to your CUDA version and OS.
    * CUDA 12 on windows on python 3.11 command 
    `pip install https://download.pytorch.org/whl/cu121/torchvision-0.16.1%2Bcu121-cp311-cp311-win_amd64.whl`
    * Or you can download *.whl file to your local drive and install with command `pip instal <whl_file_path>`
* If you are working on google colab, no need to install pytorch individually but make sure use GPU for its computing resource
* Install ultralytics with command  `pip install ultralytics`


## Data
Before training the model, video is converted into frame using opencv locally. Video has around 1799 frames. 104 frames are selected arbitrarity to be annotated. The images and its annotation are in folder data/images and data/labels respectively. 

For annotation, we use makesense.ai platform. The images and annotaed labels are on folder `data/train/iamges` and `data/train/labels`

The original video for the assignment is in `data/video`

## Training
Due to limitation in local computing power, model training is conducted on google colab (free tier) with GPU resource. Pre-trained model `Yolov5mu.pt` is used to train the dataset with 30 epoch and image size 640. 
