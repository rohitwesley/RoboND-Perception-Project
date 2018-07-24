# RoboND-Perception-Project
## Project: Perception Pick & Place
### [Rubric](https://review.udacity.com/#!/rubrics/1067/view) Points
### Here I will consider the rubric points individually and describe how I addressed each point in my implementation.  

#### 1. Provide a Writeup / README that includes all the rubric points and how you addressed each one.  You can submit your writeup as markdown or pdf.  

You're reading it!

### Exercise 1, 2 and 3 pipeline implemented :
#### 1. Complete Exercise 1 steps. Pipeline for filtering and RANSAC plane fitting implemented.
PointCloud Filtering with RANSAC - [RANSAC.py](https://github.com/rohitwesley/sensor_stick/blob/master/scripts/RANSAC.py)
![Object PointCloud](https://github.com/rohitwesley/sensor_stick/blob/master/images/object_pointcloud.png)

#### 2. Complete Exercise 2 steps: Pipeline including clustering for segmentation implemented.  
PointCloud Segmentation - [segmentation.py](https://github.com/rohitwesley/sensor_stick/blob/master/scripts/segmentation.py)
![Segmented](https://github.com/rohitwesley/sensor_stick/blob/master/images/color_cluster.png)

#### 3. Complete Exercise 3 Steps.  Features extracted and SVM(Support Vector Machine) trained.  Object recognition implemented.
Compute histograms :- [features.py](https://github.com/rohitwesley/sensor_stick/blob/master/src/sensor_stick/features.py)
Feature Generation :- [capture_features.py](https://github.com/rohitwesley/sensor_stick/blob/master/scripts/capture_features.py)
SVM Training :- [train_svm.py](https://github.com/rohitwesley/sensor_stick/blob/master/scripts/train_svm.py)
![Confusion Matrix](https://github.com/rohitwesley/sensor_stick/blob/master/images/confusion_matrix.png)
![Normalized Confusion Matrix](https://github.com/rohitwesley/sensor_stick/blob/master/images/normailzed_confusion_matrix.png)
Object Recognition :- [object_recognition.py](https://github.com/rohitwesley/sensor_stick/blob/master/scripts/object_recognition.py)
![Object Recognition](https://github.com/rohitwesley/sensor_stick/blob/master/images/object_recognition.png)

### Pick and Place Setup

#### 1. For all three tabletop setups (`test*.world`), perform object recognition, then read in respective pick list (`pick_list_*.yaml`). Next construct the messages that would comprise a valid `PickPlace` request output them to `.yaml` format.

And here's another image! 
![demo-2](https://user-images.githubusercontent.com/20687560/28748286-9f65680e-7468-11e7-83dc-f1a32380b89c.png)

Spend some time at the end to discuss your code, what techniques you used, what worked and why, where the implementation might fail and how you might improve it if you were going to pursue this project further.  


