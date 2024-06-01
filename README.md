# Football Ball Possession Measurement using YOLOv5
- This project implements real-time object tracking using the YOLOv9 object detection model and the DeepSORT tracking algorithm.

## Introduction

- This project implements a computer vision system based on YOLOv5 (You Only Look Once v5) for estimating ball possession time in football matches. By detecting the ball and players in video footage, the system calculates the percentage of time each team controls the ball.

## Dependencies
- Python 3.x (Recommended: 3.7 or later)
- PyTorch (compatible with your Python version)
- OpenCV (optional, for video processing utilities: pip install opencv-python)
- YOLOv5 (install using pip install git+https://github.com/ultralytics/yolov5.git)

## Installation

### 1.Clone this repository:

#### Bash
```
git clone https://github.com/ShouyiLeee/Football-Measuring-Possession
```

### 2.Create a virtual environment (recommended for managing dependencies):

#### Bash
```
python -m venv env source env/bin/activate  # Windows: env\Scripts\activate
```



### 3.Install the required packages within the virtual environment:

#### Bash
```
 pip install poetry
```
```
- > poetry install
```

### 4. download the ball.pt file:
- https://github.com/tryolabs/soccer-video-analytics/releases/tag/v0



## Run:
#### Bash
```
 python run.py --<application> --model <path-to-the-model> --video <path-to-the-video>
```

## Training
#### Prepare your data:
- Create a directory for your football video files (e.g., data/videos). If needed, prepare a custom dataset with ball and player annotations in YOLOv5 format (refer to YOLOv5 documentation for format details).
  
#### Train a YOLOv5 model (if using a custom dataset):
- Modify the data.yaml file to specify your dataset paths and class labels (ball, player).
- Run the training script:
#### Bash
```
 python train.py --data data.yaml --img-size 640  # Adjust img-size as needed

```

### Demo
[![Watch the video](https://img.youtube.com/vi/_qlpIrutztFQ.jpg)](https://youtu.be/qlpIrutztFQ)


