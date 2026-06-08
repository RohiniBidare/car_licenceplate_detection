# car_licenceplate_detection
Project Objective

Develop an automated Car License Plate Recognition (ALPR) system using pretrained YOLOv8 models (YOLOv8n, YOLOv8s, and YOLOv8m) for license plate detection and OCR for character recognition. The project compares different YOLOv8 variants in terms of accuracy, speed, and deployment efficiency.

Dataset Used


Dataset: Andrew Car License Plate Dataset
Total Images: 433 annotated vehicle images
Classes: License Plate
Split: 80% Training, 10% Validation, 10% Testing
Images were annotated in YOLO format and used for transfer learning.
CNN Architecture
Object Detection Models: YOLOv8n, YOLOv8s, YOLOv8m
Technique: Transfer Learning using pretrained YOLOv8 weights
OCR Engine: Used after plate detection to extract alphanumeric characters from cropped license plate regions
Pipeline: Image → YOLOv8 Detection → Plate Cropping → OCR Recognition → License Plate Text Output
📈 Results and Accuracy
Model	Precision	Recall	mAP@50	mAP@50-95
YOLOv8n	97.45%	87.14%	94.23%	60.56%
YOLOv8s	88.71%	86.36%	92.15%	56.81%
YOLOv8m	87.57%	81.81%	91.75%	56.60%

Key Findings:

YOLOv8n achieved the highest overall detection performance.
YOLOv8s provided the best balance between speed and accuracy.
YOLOv8m handled challenging license plate images more effectively but required higher computational resources.

Output Flow:

Input Vehicle Image ->
        
YOLOv8 License Plate Detection ->
        
Crop Detected Plate ->
        
OCR Character Recognition ->
        
Extracted License Plate Number

This project demonstrates an efficient deep learning-based solution for automatic license plate detection and recognition suitable for intelligent transportation and surveillance systems.
