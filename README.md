# Object-Detection-and-Multi-Object-Classification
Object Detection and Multi-Object Classification Using YOLOv1
What is Object Detection?
Object Detection is a computer vision task that involves:

Locating objects within an image (bounding box coordinates)

Classifying each detected object (e.g., car, person, dog)

Unlike image classification (which predicts one label per image), object detection outputs multiple labels and locations per image.

Multi-Object Classification
This refers to detecting multiple objects of potentially different classes within a single image. The model must:

Predict multiple bounding boxes

Assign a class label to each box

Compute confidence scores for predictions

YOLO (You Only Look Once) – Overview
YOLOv1 is one of the earliest and most popular real-time object detection models. It formulates object detection as a single regression problem, directly predicting:

Bounding box coordinates

Class probabilities

Confidence scores

Key Concepts of YOLOv1:
Grid-Based Prediction:

The input image is divided into an S×S grid.

Each grid cell is responsible for predicting bounding boxes and class probabilities for objects whose center falls inside the cell.

Bounding Box Prediction:

Each box predicts:

x, y (center of the box relative to the grid cell)

w, h (width and height relative to the whole image)

Confidence score (probability that a box contains an object × IoU)

Unified Architecture:

YOLO uses a single CNN model to do all predictions in one forward pass, making it extremely fast.

Loss Function:

Combines classification loss, localization loss (for bounding boxes), and confidence loss.

Advantages of YOLOv1
Real-time performance (45+ FPS)

Global reasoning across the image

End-to-end training with unified loss function

Limitations of YOLOv1
Struggles with small objects

May produce coarse localization

Fixed number of bounding boxes per grid cell

Evaluation Metrics
IoU (Intersection over Union): Measures the overlap between predicted and ground truth boxes.

mAP (mean Average Precision): Averaged precision over all classes.

Precision/Recall: Useful for understanding detection trade-offs.

Applications of Object Detection
Autonomous vehicles (detecting pedestrians, cars, signs)

Video surveillance (tracking persons or objects)

Retail (product recognition)

Healthcare (localizing tumors in X-rays or MRIs)

