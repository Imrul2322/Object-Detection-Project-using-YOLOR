# Custom Object Detection Project using YOLOR

## Key Findings

The trained model is capable of finding objects with excellent accuracy from the list of 10 collected and annotated objects. Mean Average Precision (mAP @ 0.5) of 72.8% after training the model for 500 epochs. Using YOLO-v4 on the same dataset 71.09% of maP @ 0.5 achieved after 500 epochs. Detection time improved 63% using YOLOR compared to YOLO-v4. 

## Table of Contents

* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Problem-Statement">Problem Statement</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Methodologies">Methodologies</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Resources">Resources</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Dataset">Dataset</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Summary-of-Results">Summary of Results</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Contribution">Contribution</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Repository-Structure">Repository Structure</a>
* <a href="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR#Acknowledgements">Acknowledgements</a>

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

## Dataset

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

![alt text](https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR/blob/main/assets/labels.png)

Figure 1: Analysis of the labels used. 

![alt text](https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR/blob/main/assets/precision-recall_curve.png)

Figure 2: Precision Recall curve.

![alt text](https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR/blob/main/assets/test_batch2_labels.jpg)

Figure 3: Object detection in random images.

<a href="https://drive.google.com/file/d/1pYlTC-hrTUykopNUfVh64yCQsX2LDOAa/view?usp=sharing"><img src="https://github.com/Imrul2322/Object-Detection-Project-using-YOLOR/blob/main/assets/detection_detection_video.png" ></a>

Video 1: Object detection in a 5 min long Manhattan St video. 


## Contribution

1. Dataset Collection (100%)
2. Model Building (100%)
3. Produce results (100%)

## Repository Structure

```bash

Custom_Dataset_YOLOv4_version1.ipynb
│   README.md
│
├───assets
│       detection_detection_video.png
│       labels.png
│       labels_correlogram.png
│       precision-recall_curve.png
│       results.png
│       test_batch2_labels.jpg
│
├───Dataset generation ToolKit
│   │   classes.txt
│   │   convert_annotations.py
│   │   LICENSE
│   │   main.py
│   │   README.md
│   │   requirements.txt
│   │
│   ├───images
│   │       classes.png
│   │       rectangle.png
│   │       visualizer_example.gif
│   │
│   └───modules
│       │   bounding_boxes.py
│       │   csv_downloader.py
│       │   downloader.py
│       │   image_level.py
│       │   parser.py
│       │   show.py
│       │   utils.py
│       │
│       └───__pycache__
│               bounding_boxes.cpython-39.pyc
│               csv_downloader.cpython-39.pyc
│               downloader.cpython-39.pyc
│               image_level.cpython-39.pyc
│               parser.cpython-39.pyc
│               show.cpython-39.pyc
│               utils.cpython-39.pyc
│
└───YOLOR
        custom.names
        custom.yaml
        generate_test.py
        generate_train.py
        process.py
        README.md
        yolor_p6_custom.cfg

```

## Acknowledgements

1. https://github.com/AlexeyAB/darknet/
2. https://github.com/WongKinYiu/yolor
3. https://github.com/EscVM/OIDv4_ToolKit











