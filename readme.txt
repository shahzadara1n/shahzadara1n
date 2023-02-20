Hand Gesture Recognition

Overview:
This repository contains two Python scripts that use OpenCV and the CVZone library to perform hand gesture recognition:

1. dataCollection.py -->
This script captures images of the user's hand in various gestures and saves them to a folder, which can be used to train
a machine learning model for recognizing those gestures.

2. gestureTest.py -->
This script uses a pre-trained machine learning model to recognize the gestures made by the user's hand in real-time video.


Dependencies:
The scripts require the following libraries to be installed:

    o OpenCV (pip install opencv-python)
    o CVZone (pip install cvzone)
    o MediaPipe (pip install mediapipe)


Usage:
    To use the scripts, follow these steps:

    - Run dataCollection.py and follow the instructions on-screen to collect images of your hand in various gestures.
      The images will be saved to the specified folder.
    - Train a machine learning model using the images collected in step 1.
    - Replace the classifier object in test.py with your trained machine learning model.
    - Run test.py and make the appropriate gestures in front of your webcam to see the recognized output in real-time.


Acknowledgements:
    The HandDetector and Classifier classes used in these scripts are part of the CVZone library, which provides useful
    OpenCV tools for computer vision applications.



Modules Used:
    •   OpenCV (cv2) for accessing the camera and image processing
    •   cvzone.HandTrackingModule for detecting hands in the video stream
    •   cvzone.ClassificationModule for classifying the hand gesture
    •   numpy for numerical computations
    •   math for mathematical operations
    •   time for accessing time-related fun ctions


Code Working:
    •	The code initializes a videoCapture object to capture the frames from laptop’s webcam.
    •	The HandDetector object is created to detect hands in the video, with a maximum number of hands to detect
        set to 1.
    •	A folder is created to store the images that will be captured during the detection process.
    •	using while loop, the code reads frames from the camera and passes them to the HandDetector object to
        detect the hand in the frame.
    •	If the detector finds at least one hand, the code crops the image to the bounding box of the hand and
        resizes it to a fixed size.
    •	The resized image is saved to the specified folder if the "s" key is pressed.
    •   The second module contains cvzone.ClassificationModule sets up a Classifier object, which loads a pre-trained
        model and label file for hand gesture recognition.
    •	The original and processed images are displayed on the screen.


Summary:
    It captures video frames from the camera, processes them to extract the hand region, and resizes it to a
    fixed size. Then it displays the original and the cropped hand images. When the user presses the 's' key,
    it saves the cropped hand image and the corresponding label in "data" folder. Then the code uses a pre-trained
    deep learning model to classify the hand gesture and display the predicted label on the video stream.
