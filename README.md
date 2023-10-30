# POSE-DETECTION-SYSTEMS-COMPUTER-VISION-

![image](https://github.com/dapzwalt/POSE-DETECTION-SYSTEMS-COMPUTER-VISION-/assets/125368548/a4967cba-9149-4d57-9e02-8841f807f630)

## Table of Contents
- [Introduction](#introduction)
- [Getting started](#getting-started)
- [Importing Necessary Libraries](#importing-necessary-libraries)
- [Real-time Pose Detection](#real-time-pose-detection)
- [Contribution](#contribution)
- [License](#license)

## Introduction
The MediaPipe Pose Landmarker task lets you detect landmarks of human bodies in an image or video. You can use this task to identify key
body locations, analyze posture, and categorize movements. This task uses machine learning (ML) models that work with single images or videos. Pose detection and recognition 
system is one that uses computer vision to detect the overall body figure. This project showcases pose detection using computer vision and a mediapipe algorithm or library. As we progress, you will see its applications in our everyday lives.

## Getting Started...

## Importing Necessary Libraries
I imported two important libraries, which are openCV and MediaPipe. OpenCV is used for the identification of my webcam in my computer system, while MediaPipe is used for pose detection.
> *import cv2
import MediaPipe as mp*

## Real-time Pose Detection
Once we import our libraries, we then leverage the power of MediaPipe to detect key landmarks in the body. The mp.solutions.drawing_utils allows us to draw, making it easy for us to visualize the pose estimation.
After this, your webcam captures the video frames using the code, converts them from BGR to RGB color code format, applies pose detection, and draws the landmark.
The code is as follows:
> *while True:
    _, img = cap.read()
    imgRGB = cv2.cvtColor img, cv2.COLOR_BGR2RGB
    results = pose.process(imgRGB)
    if results.pose_landmarks:
        mpDraw.draw_landmarks(img, results.pose_landmarks, mpPose.POSE_CONNECTIONS)
    cv2.putText(img, '10Alytics Pose Detection', (10, 55), cv2.FONT_HERSHLEY_PLAIN, 2, (0,255,255), 2)
    cv2.imshow('10Alytics Pose Detection', img)
    if cv2.waitkey(1) & 0xff == ord('q'):
        break*

## Contribution
Your contribution is highly welcome as this project is open source, and you can open issues or submit pull requests as we are here to grow and learn together.

##License
This project is released under the MIT licensing board, which means you can use it to the best of your ability and be flexible around it. 



