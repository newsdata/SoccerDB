# SoccerDB: A Large-Scale Database for Comprehensive Video Understanding
This implementation codes of paper "SoccerDB: A Large-Scale Database for Comprehensive Video Understanding".
## Introduction
This implementation includes three main parts, [object detection](https://github.com/newsdata/SoccerDB/tree/master/code/object_detection), [video classification](https://github.com/newsdata/SoccerDB/tree/master/code/video_classification) and [video detection](https://github.com/newsdata/SoccerDB/tree/master/code/video_detection). And the video classification part includes three parts, video classification, Highlight detection, MRTS(Mask and RGB Two-Stream).

## Detection
See the [README.md](https://github.com/newsdata/SoccerDB/blob/master/code/object_detection/README.md) for details in the [object Detection](https://github.com/newsdata/SoccerDB/tree/master/code/object_detection) section.
## This implementation largely borrows from [mmdetection](https://github.com/open-mmlab/mmdetection), [SlowFast](https://github.com/facebookresearch/SlowFast), [BMN](https://github.com/JJBOY/BMN-Boundary-Matching-Network).
## Detection
### All of the detection experiments are powered by [mmdetection](https://github.com/open-mmlab/mmdetection). The process is as follows:
### 1: Build the environment for [mmdetection](https://github.com/open-mmlab/mmdetection).
### 2: Process the detection data in coco format.
### 3: Config files and models are in [detection](https://github.com/newsdata/SoccerDB/tree/master/code/detection).

## Video classification, Highlight detection, MRTS(Mask and RGB Two-Stream)
### 
