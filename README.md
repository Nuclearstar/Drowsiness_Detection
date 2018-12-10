# Drowsiness_Detection

This repository contains two implementations for driver drowsiness detection via 
1. Eye monitoring being it closed or opened (Detection_for_images).
2. Real-time video stream (Detection_for_videos). 

### Code Requirements
1. pip install dlib
2. pip install skimage
3. pip install scipy
4. pip install numpy
5. pip install cv2
6. pip install imutils

### Dataset
You can download a trained facial shape predictor from: http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2

### Procedure in Implementation 1
Python code: Simple app to detect the status of eye being closed or opened (sleep_detection.py (test1.jpg and test2.jpg are for testing))

Run using the command, python sleep_detection.py /path/to/shape_predictor_68_face_landmarks.dat test1.jpg

### Procedure in Implementation 2
To run the code, type python Drowsiness_Detection.py

### Algorithm
Each eye is represented by 6 (x, y)-coordinates, starting at the left-corner of the eye (as if you were looking at the person), and then working clockwise around the eye:
![alt text](https://raw.githubusercontent.com/Nuclearstar/Drowsiness_Detection/Detection_for_videos/eye1.jpg)

### Condition
It checks 20 consecutive frames and if the Eye Aspect ratio is lesst than 0.25, Alert is generated.

#### Relationship
![alt text](https://raw.githubusercontent.com/Nuclearstar/Drowsiness_Detection/Detection_for_videos/eye2.jpg)

#### Summing up
![alt text](https://raw.githubusercontent.com/Nuclearstar/Drowsiness_Detection/Detection_for_videos/eye3.jpg)

For more information [look here](https://www.pyimagesearch.com/2017/05/08/drowsiness-detection-opencv/).

### References and Credits:
This implementation is inspired by Akshay Bahadur's project
This implementation also took inspiration from Taha Emara's work.
