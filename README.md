# Brain Tumor Detection and Localization in MRI Images

## 1.0 INTRODUCTION
This project focuses on the development of a robust model for the detection and localization of tumors in brain MRIs. Two distinct approaches were employed: a convolutional neural network (CNN) model trained from scratch and a pre-trained YOLOv8 model. Due to the scarcity of accurate data for this specific task, various techniques were implemented to enhance the model's accuracy and precision.

## 1.1 Problem statement
This report addresses the critical issue of detecting and localizing tumors in brain MRIs, which has significant implications for healthcare due to the high stakes involved. The field of AI has seen substantial advancements aimed at expediting and improving the accuracy of diagnosing such diseases. However, the scarcity of accurate data poses a significant challenge. Patient data confidentiality and the high costs associated with medical exams and tests contribute to this challenge.

## 1.2 Agile management
Despite being an individual endeavor, this project was managed using agile principles, with tasks and subtasks defined in the Jira platform. This approach aimed to simulate the process of executing the project within predetermined time and budget constraints. The agile methodology proved invaluable in managing uncertainties, including unforeseen issues that arose during the project. Regular communication with other teams, facilitated by acting as scrum masters, enabled the evaluation of the project's progress and each sprint's effectiveness.

## 1.3 Data
The "Brain tumor object detection datasets" served as the primary dataset for this project, comprising 1100 MRI images along with corresponding bounding boxes of tumors. This dataset is categorized into three subsets based on the direction of scanning in the MRI images.

## Preprocessing Data
In the initial phase of the project, before training the model, it was imperative to preprocess the data to make it suitable for feeding into the model. This involved creating lists of images in both the training and test directories and subsequently reading the contents of the label files, which contained information about the labels and bounding box details for tumors in the MRIs.

## 2.0 METHODOLOGY
This project encompasses the exploration of two primary models, each delving into various aspects of training and object detection concepts.

### 2.1 Model-1: Convolutional Neural Network (CNN) from Scratch
The first model involves a CNN architecture designed for the classification and localization of tumors in brain MRIs. We sought to optimize the model's architecture by incorporating various layers, such as Conv2D, Batch Normalization, ReLU Activation, Max Pooling2D, skip Connection, Dense, and Dropout.

### 2.2 Model-2: YOLOv8 for Tumor Detection
The second model employed YOLOv8 for detecting tumors in MRI images. However, due to the limited data availability and the model's large size, overfitting became a significant concern. To mitigate this issue, we employed the auto-augmentation method, L2 penalty factor, and dropout feature of the YOLO model.

## 3.0 RESULTS
This section presents the outcomes obtained from each model, along with the corresponding efficiency metrics.

### 3.1 Model-1: without augmentation
After training, the model achieved an accuracy of approximately 0.4886. The mean square error of bounding boxes was approximately 0.0112, and the F1 score for classification was also around 0.4886.

### 3.2 Model-1: with augmentation
This model is similar to the previous model but using an augmentation function in input data. After training and validation, the model, the output accuracy is about 0.5455 and mean square error of bounding boxes equals to 0.0116 and finally the F1 score of the classification is equal to 0.5454.

### 3.3 Model-2: YOLO v8 model
Model-2 utilizes YOLO as a sophisticated model that automates the training and validation processes, yielding a multitude of results. The model benefits from being pre-trained on a vast dataset, enabling it to converge to superior results compared to Model-1, which was trained from scratch.

## 4.0 CONCLUSIONS
This project aimed to develop effective models for the detection and localization of brain tumors in MRI images. Two main models were explored: a CNN model trained from scratch and a YOLOv8 model. While the CNN model showed limited performance due to data scarcity, the YOLOv8 model demonstrated significant improvements. Further improvements and additional data are essential for practical application and enhanced predictive capabilities.

## 5.0 REFERENCES
- [Brain tumor object detection datasets](https://www.kaggle.com/datasets/davidbroberts/brain-tumor-object-detection-datasets)
- [Ultralytics Documentation](https://docs.ultralytics.com/usage/python/)
