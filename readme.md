This is the project for the module Computer Vision prepared by Paulina Zal, Stefanie Palten and Elisabeth Freimann.

The main goal is to prepare a tool for detection of faces in pictures, classification of emotions on the detected face and lastly painting the face based on the emotion. Each emotion has its specific style.

The data was downloaded from: 
faces:
emotions:

The whole repository should be downoloaded and all folders loaded to google drive. The Notebooks are prepared for google colab due to memory restrictions on local machines and needs GPU assistance.

In the repository we have four folders:
1. Code : all notebooks and yaml files.
2. Models: the model trained by us for a later use.
3. Data: Folder containing images for emotion classification, face detection and style transfer.
4. Style_Pictures: pictures used for style transfer (style representation).
5. Our Pictures: Pictures used as a content for style transfer.

This project answer the following research questions:

Q1. What is the best model performance for diffrent network architectures for the emotion classification task? Which model achieves the best results?
Q2. Has the number of annotated images an influence on the performance of the object detection algorithm in terms of MAP​?
Q3. Can style transfer help to quickly capture the emotions of a group of people?


For answering the questions we prepared few notebooks (in the folder code):

Q1: 
Emotion Detection - Simple Model.ipynb - Unsing only Danse Layers
Emotion Detection_CNN.ipynb - Using Convolutional Neural Network
emotion_detection_VGG16.ipynb - Using pretrained models
emotion_detection_VGG16 - metrics_calculation.ipynb Testing the models built with pretrained models.

Q2:
YOLO_60_pics.ipynb - Finetuning YOLOv8 for face detection (only one class learnt: faces) on 60 annotated pictures
YOLO_350_pics.ipynb - Finetuning YOLOv8 for face detection (only one class learnt: faces) on 350 annotated pictures + augmentation( overall 800 pictures)
  helping scripts:
  Resize_images_60_faces.ipynb - take 60 pictures (choosed manualy from bigger data set) and resize to 512 x 512 and then save on google drive
  Resize_images_350_faces.ipynb - take 60 pictures (choosed manualy from bigger data set) and resize to 512 x 512 and then save on google drive

Q3:
style_transfer_putting_all_together.ipynb - final script combining creating a texture in RoIs specified by the face detection algorithm. The texture depends on emotion detected in RoIs.


                    
