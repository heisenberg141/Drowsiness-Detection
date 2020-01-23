# Drowsiness Detection
## Introduction
This project is aimed towards solving the problem of detecting the tiredness level of
drivers. If the driver is found to be drowsy, an alarm will be triggered to make him
or her more attentive.
This is done using the techniques like deep learning and computer
vision for object detection. The project was implemented on a raspberry pi and a video camera.

## Hardware Required:
1. Raspberry Pi 3
2. Picamera

This project uses python 3 along with openCV for image processing and dlib for facial landmarks
detection. Since raspberry pi provides limited memory and processing speed, we used a combination
of Haar Cascades and HOG to detect the face and the eyes of the driver.

Haar cascade was used for detecting the face since it is inexpensive from a computation standpoint
whereas HOG was used for detecting eyes in the face. HOG although, computationally expensive provides
accurate boundaries for eyes. To perform this successfully, we used dlib, which is a free to use library
on python to detect eyes using HOG.

Once the boundary of the eyes are found, we then find the aspect ratio, ie length/height of the eye and if
it is below a certain threshold the program triggers an alarm


