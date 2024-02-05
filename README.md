# Underwater Fish Recognition Model
An underwater fish recognition model developed using YOLOv8. The model was trained on enhanced images of the dataset. The enhancement technique used was RGHS.

## Dataset
DeepFish : https://alzayats.github.io/DeepFish/

### Dataset enhancement technique RGHS usage
1. List of libraries you need to install to execute the code :

    python = 3.6, cv2, numpy, scipy, matplotlib, scikit-image, natsort, math, datetime

2. Put the input images to corresponding folders :
   
    Create 'InputImages' and 'OutputImages' folders
    
   Then put raw images to 'InputImages' folder
![image](https://github.com/noori03/underwater-fish-recognition/assets/156057742/a8546838-73fb-4b85-9427-a64822f4f0b6)
Figure-Enhanced image after RGHS

4. Run main.py;

The enhanced/restored images will be saved in "OutputImages" folder.

## Model Usage

### 1) Using the deployed model on Roboflow
The model is deployed on Roboflow and can be used directly through following link

https://universe.roboflow.com/underwater-fish/underwater-fish-detection-izi1l/model/6

### 2) Through Python

Download the model weights file fish_detection_model.pt

Install ultralytics
```
pip install ultralytics
```
The fllowing should be run in the python file
```
from ultralytics import YOLO

# load model
model = YOLO('fish_detection_model.pt')

# predict on image
model.predict('image_file.jpg', save=True, conf=0.5)
```
![image](https://github.com/noori03/underwater-fish-recognition/assets/156057742/fec0470f-573b-44d6-a43a-0c540dd8a2dd)
Figure- Detection of caranx fish
