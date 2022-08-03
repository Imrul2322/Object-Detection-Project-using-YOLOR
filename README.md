# Custom Object Detection Project using YOLOR

## Key Findings

The trained model is capable of finding objects with excellent accuracy from the list of 10 collected and annotated objects. Mean Average Precision (mAP @ 0.5) of 72.8% after training the model for 500 epochs. Using YOLO-v4 on the same dataset 71.09% of maP @ 0.5 achieved after 500 epochs. Detection time improved 63% using YOLOR compared to YOLO-v4. 

## Table of Contents

## Problem Statement

YOLOR (You only learn one representation) is one of the most efficient state-of-the-art object detection algorithm. Unlike YOLO (you only look once) algorithms which uses 1 * 1 convolutions for prediction map and feature map, YOLOR is a unified network which can combine explicit learning (learning based on data and input) with implicit knowledge (subconscious learning). It detects 80 classes of objects from COCO dataset. Though it covers many objects, our goal is to build a custom model based on YOLOR which can be trained to detect any object we want. To serve this purpose, 10 classes of object has been selected and trained the model accordingly.

## Methodologies

1. Collected and annotated 52,884 training images and 6,644 testing images. 
2. Modified existing YOLOR model to fit our needs. 
3. Created Muli-GPU environment for parallel processing. 
4. Run 500 epochs on Lambda server. 

## Resources

1. Python (PyTorch, OpenCV, scipy, tensorboard, pandas, seaborn, scikit-learn).
2. Google Open Image Dataset
3. Lambda GPU server (3 GPUs)

## dataset used

Training dataset link: https://drive.google.com/file/d/1L1mRbnLl6sPvu-q_3mhFVlsvu0fXDzJj/view?usp=sharing
Testing dataset link: https://drive.google.com/file/d/12ApqaRp8gmlGO6NkdAfs6xl4DAqx7IBn/view?usp=sharing

Object labels:
1. Bird
2. Cat
3. Chicken
4. Dog
5. Horse
6. Person
7. Tree
8. Coffee
9. Tea
10. Monkey

## Summary of Results 

![alt text](https://github.com/Imrul2322/Feature-Selection-using-Discriminative-Analysis/blob/main/assets/cifar%2010%202%20class%2025.png)

<iframe src="https://drive.google.com/file/d/1pYlTC-hrTUykopNUfVh64yCQsX2LDOAa/preview" width="640" height="480" allow="autoplay"></iframe>

## Contribution

1. Dataset Collection (100%)
2. Model Building (100%)
3. Produce results (100%)











