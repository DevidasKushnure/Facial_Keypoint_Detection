# Facial_Keypoint_detection
Facial keypoint detection using the deep learning approach

- Readme_keypoint_detection.pdf is provided for detailed analysis 

Objective: The objective is to detect facial keypoint positions on face images from the given facial dataset. 

Image Keypoints:
Image keypoints are distinct points or places in an image that are picked because they represent unique and distinguishable features. 
These points are crucial in computer vision and image processing for various tasks such as image recognition, object detection, and image matching. 

Problem categorization:
Keypoint detection is a regression task where output is a continuous value of predicted keypoints. The input images are and the corresponding keypoints are the input to the network and the output is the keypoints predicted by the model.

Dataset: 
Each keypoint is specified by an (x,y) real-valued pair in the space of pixel indices. There are 15 keypoints in the dataset, which represent the following elements of the face:
Left_eye_center, right_eye_center, left_eye_inner_corner, left_eye_outer_corner, right_eye_inner_corner, right_eye_outer_corner, left_eyebrow_inner_end, left_eyebrow_outer_end, right_eyebrow_inner_end, right_eyebrow_outer_end, nose_tip, mouth_left_corner, mouth_right_corner, mouth_center_top_lip, mouth_center_bottom_lip
Dataset_link: https://www.kaggle.com/datasets/nagasai524/facial-keypoint-detection/data 

Challenges in the Facial Keypoint detection:
Detecting facial keypoints is a very challenging problem. Facial features vary greatly from one individual to another, and even for a single individual, there is a large amount of variation due to 3D pose, size, position, viewing angle, and illumination conditions.

Steps followed in the development of the project:
- Data analysis for understanding the nature of images and keypoints in the dataset, data preprocessing such as filling in missing keypoints.
(Notebook: data_analysis_yeypoint_detection.ipynb )
- The dataset validation after preprocessing.
Data Loading and converting dataset into numpy array for easy loading and processing while training
- Loading numpy array and splitting the dataset into train, validation, and test (Total samples = 7049, Train = 5639, Validation = 705, Test = 705)
- Two models were developed:
-Base_model
- Model_v1
- Saved summary, plots, predictions and performance of the models
- Model notebook
base_model_keypoint_detection_script.ipynb
model_v1_ keypoint_detection_script.ipynb
- Trained two models separately using the following training configuration
Optimizer: Adam
Learning rate: 1Xe-5
Loss: mean squared error
Metric: mean absolute error
Training callback: EarlyStopping
Batch Size: 32
Epochs: 200
- Saved the trained model and plot for losses
- Load the model and Model predictions saved in CSV
- visualization of the ground truth and predictions on the sample images
- Performance evaluation using mean absolute error and accuracy of the model for three threshold values (5, 10, 15) of pixels in percentage
- Saved the evaluation performance in CSV file
