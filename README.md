# Real Time IDcard Detection and OCR
![](https://github.com/RodzanIskandar/IDcard_detection_and_OCR/blob/main/images/realtime%20detection.png)
## Overview
The main idea of this projects is to simplify administration process in indonesia using existing id card. This idea comes up cause there are complicated administration process in Indonesia especially in the state administrative affairs for civilians. So here I am designed the ID card detection and Optical Character Recognition (OCR) to its able to detect and record the information into csv file using camera. To detect the idcard I am using Tensorflow object detection algortihm with SSD MobileNet V2 FPNLite 320x320 as pretrained model from Tensorflow. In order to detect the characters on the id card, I am using library easyocr based on pytorch.

## Libraries and Resources used
**Libraries:** Tensorflow Object detection, EasyOCR

**Resource:** 

- [https://github.com/nicknochnack/TFODCourse](https://github.com/nicknochnack/TFODCourse)
- [https://github.com/tzutalin/labelImg](https://github.com/tzutalin/labelImg)
- [https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md)
- [https://github.com/nicknochnack/RealTimeAutomaticNumberPlateRecognition](https://github.com/nicknochnack/RealTimeAutomaticNumberPlateRecognition)

## The Training data
I am collected my own id card images using webcam with various light condition and orientation and label it using labelimg. I am training it with only 20 photos. After 3000 step of training, I got around 0.17 loss and evaluation metrics Precision and Recall 0.95

![](https://github.com/RodzanIskandar/IDcard_detection_and_OCR/blob/main/images/total%20loss.PNG) ![](https://github.com/RodzanIskandar/IDcard_detection_and_OCR/blob/main/images/Evaluation%20metrics.PNG)

## Further Research
To be able get more generalised model, the model have to train with more data or photo of some id cards with some various conditions. for the better detecting the characters component in id card (OCR), its better if using special camera for documents with fixed place, so its not distracted by the motion of the user
