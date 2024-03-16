# Shredder Machine

## Overview

* In any production line safety of the worker is the first priority so that they can work safely and confidently which eventually increase the growth in a company. So this project try to solve that issue by building a system which can be deployed through IP Camera, Microcontroller, Relay etc.

* There are two lines in our system which makes worker cautious, one is safety line in which if workers hand reaches ALARM Continously Set ON and another is Boundary Line in which if workers hand reaches Machine Automatically Swiched off from the command Microcontroller gives.

* Since Faster RCNN give unrealistic MAP value so I choose to finalized my model by training it on SSD MobileNetV2 which give me a MAP in between 60 to 70.

## Requirement Gathering

### Data -> Imgaes -> Palm ->Hand
### Camera -> Web Camera

## Data -> User oriented
### Capture video in the factory
### Video -> Frames -> Images
### Annotation -> 1.x1, xml
### Model Training -> YOLO, Detectron2, TFOD

## Important Points

### Safety Line -> Warning
### Border Line -> Shutdown the Machine

## TechStack Selection

### Programming Language -> Python 3.6
### DL FrameWork -> TensorFlow Object Detection -> 1.14
### Image Processing -> OpenCV, imutils
### Sound -> PlaySound

## Architechture

![](https://user-images.githubusercontent.com/75604769/177889835-3dd92603-1340-43ce-9683-48fe7a5dee6b.png)

##  Project Workflow

### Our pipeline consists of three steps:

1. An AI model which detect all human hands in the live video at workshop.
2. An AI model which predict if that hands is out of safety line.
3. The output is ALARM to alert worker and shutting down a machine if hamd crosses Boundary line.

## Model's performance

* Faster RCNN give unrealistic MAP value of 85 so I choose to finalized my model by training it on SSD MobileNetV2 which give me a MAP in between 70.

* First training with 3500 images gives the MAP of 60 so I increased the data to 7500. and it gives MAP of 85 in Faster RCNN and 70 on SSD MobileNetV2.