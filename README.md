
# Video Anomaly Detection Analysis

#### This project is focused on developing a machine learning model for anomaly detection in video data. The main objective is to classify video events as either normal or anomalous, which is crucial in various applications like security surveillance, safety monitoring, and event detection systems.

## Overview

The code provides a comprehensive workflow for video anomaly detection, starting from data preparation to model training, validation, and testing. It includes the following key components:

## Data Preparation
The dataset consists of video files categorized into normal and anomalous events, sourced from UCF-Crime dataset and derived from google drive.
Anomalous events are further divided into specific types such as Abuse, Arson, Assault, etc., while normal events are grouped under Normal categories.
Data is split into training and testing sets, ensuring a balanced representation of all event types.
## Preprocessing
Video frames are taken at an interval of 7, resulting in 50 frames per video. each frame is normalized and converted from BGR2RGB using CV2 library.The anomaly videos are already tagged by anomaly frame beginning untill anomaly frame end which helps the model learn exactly the features he needs to detect anomalous events.
The preprocessed data is then prepared for model input, including the application of data augmentation techniques for training robustness.
## Model Architecture
An I3D Convnet pretrained model is employed and the model architecture includes fully connected layers with Relu as an activation function and BatchNormalization and Dropout serving as regularization techniques. The output layer consists of a single neuron with a sigmoid activation function for binary classification.
## Training and Evaluation
The model is trained using the preprocessed training dataset, with validation performed on a separate validation set to monitor overfitting.
Performance is evaluated on the test dataset, with metrics such as accuracy, loss, and a confusion matrix and ROC Curve providing insight into model effectiveness.
Various callbacks like ModelCheckpoint, EarlyStopping and ReduceLROnPlateau are implemented to enhance training by saving the best model and preventing overfitting, respectively.
## Purpose
The project aims to automate the detection of anomalous events in video streams, which can significantly enhance the efficiency and effectiveness of surveillance and monitoring systems. By leveraging deep learning and attention mechanisms, the model can learn to identify intricate patterns and anomalies in diverse video contexts.

## Usage
To utilize this model for anomaly detection:

Prepare your video dataset, categorizing videos into normal and anomalous events.
Ensure the dataset follows a similar structure as described in the Data Preparation section.
Train the model using your dataset, adjusting hyperparameters and model architecture as necessary for optimal performance.
Deploy the trained model to analyze new video data, classifying events based on the learned patterns.
### Conclusion
This Video Anomaly Detection project demonstrates the power of deep learning in analyzing and understanding complex video data. The developed model can serve as a foundation for various applications requiring automated event detection and anomaly identification in video streams.
