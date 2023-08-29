## Voila Jones Face Detection
The human face can be recognised in a picture using the viola-jones 
algorithm. The system accepts either face- or non-face-based images as 
input. 
The training phase, during which the system detects faces, will begin 
after taking the input photographs. Positive image sets and negative 
picture sets are both used in the training phase. 
 Positive image sets => faces
 Negative image sets => non-faces
All the features that are connected to the face photographs are 
gathered during the training phase and saved in a file. 
In the testing step, an input image is processed with all the stored 
features and categorised as a face or not. The image is categorised as a 
face if it meets all the criteria; else, it is classified as nonface.

### STAGE-1: Haar Feature selection
All human faces have some characteristics in common. Haar features
can be used to match them. The following traits are typical to human 
faces:
 The upper-cheeks are lighter than the area around the eyes.
 The eyes are lighter than the area around the nasal bridge.
Ingredients that combine to create face traits that can be matched:
 Position and dimensions: eyes, mouth, and nose bridge
 Value: pixel intensity gradients that are directed.
Value = Σ (pixels in black area) - Σ (pixels in white area)
(Difference in brightness between the white and black rectangles over a 
specific area)

### STAGE-2: Integral image 
The input image is made into an integral image in the next step of the 
Viola-Jones face detection algorithm. The process is finished by creating 
each new pixel in an amount equal to the sum of all pixels to its left 
and right.
Integral image reduces the number of values needed to compute the 
addition of all the pixels inside any given rectangle to just 4. These 
values are the pixels in the integral image that match the corners of the 
rectangle in the input image.

### STAGE-3: Adabost training
The Viola Jones algorithm starts by analysing all the features in a given 
image using a basic window size of 24x24. If we consider all Haar 
features, then we will need to calculate more than 160,000 features in 
each given window. 
The main goal is to get rid of as many unnecessary and redundant 
features as possible. Adaboost has choses only those features that are 
extremely helpful to us and eliminate all the extra features.
Following the establishment of these elements, a weighted sum of all 
these features is utilised to assess and determine whether or not a 
given window has a face. Weak classifiers are another name for these 
features.
Selecting the best performing feature requires analysing each feature 
across all training samples for every new poor classifier. This is said to 
be the training’s most time-consuming step.

### STAGE-4: Cascade classifiers
The cascaded classifier is collection of stages that contains a strong 
classifier. The work of every phase is to verify whether a particular subwindow is definitely not a face or may be a face. When a sub-window is 
classify to be a non-face by a given phase it is discarded. A sub-window 
classified as a may be face is passed on to the next stage in the cascade

## YOLO Object Detection

YOLO (You Only Look Once) object detection system uses deep learning
algorithms to detect objects in images or videos. The system divides 
the image into a grid and assigns each cell the task of detecting objects 
that fall within it.
YOLO processes the entire image at once and predicts the objects and 
their corresponding bounding boxes in a single step
YOLO uses a convolutional neural network (CNN) to learn features 
from the input image. The network is trained on a large dataset of 
annotated images.
It works even in different lighting conditions and viewpoints.
