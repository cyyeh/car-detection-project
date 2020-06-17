# Car Detection Using YOLO

## Abstract

This project implements YOLO/YOLOv2, which came from [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640) and [YOLO9000: Better, Faster, Stronger](https://arxiv.org/abs/1612.08242).

## Introduction

- YOLO is a state-of-the-art object detection model that is fast and accurate
- It runs an input image through a CNN which outputs a 19x19x5x85 dimensional volume.
- The encoding can be seen as a grid where each of the 19x19 cells contains information about 5 boxes.
- You filter through all the boxes using non-max suppression. Specifically:
  - Score thresholding on the probability of detecting a class to keep only accurate (high probability) boxes
  - Intersection over Union (IoU) thresholding to eliminate overlapping boxes
- Because training a YOLO model from randomly initialized weights is non-trivial and requires a large dataset as well as lot of computation, we used previously trained model parameters in this exercise.

## Related Information

- [Yolo-v4 and Yolo-v3/v2 for Windows and Linux](https://github.com/AlexeyAB/darknet)
- Object Detection for Dummies
  - [Part 1: Gradient Vector, HOG, and SS](https://lilianweng.github.io/lil-log/2017/10/29/object-recognition-for-dummies-part-1.html)
  - [Part 2: CNN, DPM and Overfeat](https://lilianweng.github.io/lil-log/2017/12/15/object-recognition-for-dummies-part-2.html)
  - [Part 3: R-CNN Family](https://lilianweng.github.io/lil-log/2017/12/31/object-recognition-for-dummies-part-3.html)
  - [Part 4: Fast Detection Models](https://lilianweng.github.io/lil-log/2018/12/27/object-detection-part-4.html)