This is the project for the module Computer Vision prepared by Paulina Zal, Stefanie Palten and Elisabeth Freimann.

The main goal is to prepare a tool for the detection of faces in pictures, classification of emotions on the detected faces and lastly painting the face based on the emotion. Each emotion has its specific style.

The data was downloaded from: 
faces ( only train and validation folders were uploaded to colab) : https://www.kaggle.com/datasets/sbaghbidi/human-faces-object-detection <br>
emotions: https://www.kaggle.com/datasets/jonathanoheix/face-expression-recognition-dataset

The whole repository should be downloaded and all folders loaded to google drive. The Notebooks are prepared for google colab due to memory restrictions on local machines and needs for GPU assistance.

In the repository we have four folders:
1. Code: all notebooks and yaml files.
2. Models: the model trained by us for a later use.
3. Data: Folder containing images for emotion classification, face detection and style transfer.
4. Style_Pictures: pictures used for style transfer (style representation).
5. Our Pictures: Pictures used as a content for style transfer.

This project answers the following research questions:

Q1. What is the best model performance for different network architectures for the emotion classification task - FCN, CNN or model-based on a pretrained architecture? Which model achieves the best results?<br>
Q2. Has the number of annotated images an influence on the performance of the object detection algorithm in terms of MAP​? <br>
Q3. Can style transfer help to quickly capture the emotions of a group of people? <br>


For answering the questions we prepared some notebooks (in the folder code):

Q1: 
Emotion Detection - Simple Model.ipynb - Unsing only Dense Layers
Emotion Detection_CNN.ipynb - Using Convolutional Neural Network
emotion_detection_VGG16.ipynb - Using pretrained models

Q2:
YOLO_60_pics.ipynb - Fine-tuning YOLOv8 for face detection (only one class learned: faces) on 60 annotated pictures
YOLO_350_pics.ipynb - Fine-tuning YOLOv8 for face detection (only one class learned: faces) on 350 annotated pictures + augmentation( overall 800 pictures)
VGG16 Face Detection (not good).ipynb - experiment with fine-tuning of VGG16 for face detection. The performance is really bad.  
  helping scripts:
  Resize_images_60_faces.ipynb - take 60 pictures (manually chosen from bigger data set) and resize to 512 x 512 px and then save on google drive
  Resize_images_350_faces.ipynb - take 350 pictures (manually chosen from bigger data set) and resize to 512 x 512 px and then save on google drive

Q3:
style_transfer_putting_all_together.ipynb - final script combining creating a texture in RoIs specified by the face detection algorithm. The texture depends on emotion detected in RoIs.


                    
