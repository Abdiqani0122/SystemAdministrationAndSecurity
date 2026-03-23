UAV Object Detection Project (Colab)
Project Overview

This project detects and classifies cotton plants and weeds from UAV images using deep learning models:

YOLOv8
Faster R-CNN

The project was developed and run entirely in Google Colab, so no local setup is required.

How to Run
Open Google Colab
Upload or open the notebook:
UAV_Object_Detection_Project.ipynb
Mount Google Drive:
from google.colab import drive
drive.mount('/content/drive')
Make sure your dataset path is set to:
/content/drive/MyDrive/DataScience/ProjectUAV/
Run all notebook cells from top to bottom
Dataset
Dataset is stored in Google Drive
Format: YOLO (images + .txt labels)
Classes:
Cotton

Folder Structure
ProjectUAV/
│
├── data/
│   ├── train/
│   │   ├── images/
│   │   └── labels/
│   │
│   ├── val/
│   │   ├── images/
│   │   └── labels/
│   │
│   ├── test/
│   │   ├── images/
│   │   └── labels/
│   │
│   └── data.yaml
│
├── runs/
│   ├── yolov8_sgd/
│   ├── yolov8_adamw/
│   └── faster_rcnn_model.pth
│
├── models/
│   └── faster_rcnn_model.pth
│
├── Images/
│   ├── results, graphs, confusion matrices
│
├── Weed-Dataset.zip
├── UAV_Object_Detection_Project.ipynb
Models
YOLOv8
Used for fast object detection
Two versions trained:
SGD optimizer
AdamW optimizer
Faster R-CNN
Used for higher precision detection
Saved model:
models/faster_rcnn_model.pth
Output

Results are saved in:

runs/

Includes:

trained weights (best.pt, last.pt)
training graphs
confusion matrices
prediction images
Notes
Project was run entirely in Google Colab
No extra installation required
Dataset is already preprocessed and split into:
train / validation / test
