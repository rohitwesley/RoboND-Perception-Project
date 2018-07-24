# RoboND-Perception-Project
## Project: Perception Pick & Place
### [Rubric](https://review.udacity.com/#!/rubrics/1067/view) Points
### Here I will consider the rubric points individually and describe how I addressed each point in my implementation.  

#### 1. Provide a Writeup / README that includes all the rubric points and how you addressed each one.  You can submit your writeup as markdown or pdf.  

You're reading it!

### Exercise 1, 2 and 3 pipeline implemented :
The exercise project readme has a detailed explanation about how I went about these steps : [senso stick](https://github.com/rohitwesley/sensor_stick)

### Pick and Place Setup


### Filtering Steps:
1. Image
2. Voxel Grid Downsampling
3. Passthrough over Z-Axis
4. Passthrough over X-Axis
5. Outlier Filter
6. RANSAC PLANE Filter

### Features Extraction and SVM training:
Here are the settings I used to create my SVM:

Pictures: 500

Bins (Color & Normals): 64

RGB vs HST: HST

Total Features: 4000

Here's the output of the training:
![SVM](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/images/svmresult1.png)

![Confusion Matrix](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/images/confusion_matrix3.png)
![Normalized Confusion Matrix](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/images/normalized_confusion_matrix3.png)

### Object Recognition :- 

#### 1. For all three tabletop setups (`test*.world`), perform object recognition, then read in respective pick list (`pick_list_*.yaml`). Next construct the messages that would comprise a valid `PickPlace` request output them to `.yaml` format.
#### Results for each World:
World 1 100%:
![Object Recognition](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/images/object_recognition_world1.png)
YAML File: [Link!](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/pr2_robot/scripts/output_1.yaml)

World 2 100%:
![Object Recognition](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/images/object_recognition_world2.png)
YAML File: [Link!](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/pr2_robot/scripts/output_2.yaml)

World 3 100%:
![Object Recognition](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/images/object_recognition_world3.png)
YAML File: [Link!](https://github.com/rohitwesley/RoboND-Perception-Project/blob/master/pr2_robot/scripts/output_3.yaml)

My Thoughts:
The exercise took me 80% of the way through the project. Importing the code from the exercise and outputting to yaml files was mostly straightforward. 

### TODO & Challenges:
Tweeking the features to get good results.
Would like to improve this projects furthur in my free time to have the robot pick and place the objects in the box more accurately.
