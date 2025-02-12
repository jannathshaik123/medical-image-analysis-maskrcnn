# Automated Reading of Skin Prick Test using Mask R-CNN

## Overview
This project implements an automated system for analyzing Skin Prick Test (SPT) results using Mask R-CNN and 3D reconstruction techniques. The system can detect and measure wheal reactions from SPT images, providing more accurate and consistent measurements compared to traditional manual methods.

## Features
- Wheal detection and segmentation using Mask R-CNN
- Automatic diameter calculation of wheal reactions
- Integration with TripoSR for 3D reconstruction
- Support for batch processing of SPT images
- Automated measurement system for clinical use

## Technical Details

### Model Architecture
- Base Model: Mask R-CNN with ResNet 101 backbone
- Framework: Detectron2 (Facebook AI Research)
- Configuration: COCO-InstanceSegmentation/mask_rcnn_R_101_FPN_3x.yaml

### Training Parameters
- Maximum Iterations: 2000
- Evaluation Period: 200
- Base Learning Rate: 0.001
- Number of Classes: 3 (including background)
- ROI Heads Batch Size: 64
- Images per Batch: 2
- Mask Format: bitmask

### Dataset
The dataset consists of two types of images:
1. "Good Pics": Regular SPT reaction images including both positive and negative reactions
2. "Ideal Pics": Clear positive SPT reaction images with prominent wheals

Data preparation was done using Roboflow with manual annotations in COCO segmentation format.

## Requirements
- Python 3.x
- PyTorch
- Detectron2
- Roboflow
- NVIDIA GPU (Tested on Tesla T4)

## Results
The model shows strong performance in both detection and segmentation tasks:
- Highest precision at IoU=0.50
- Strong performance in "mark" detection
- Accurate wheal diameter measurements
- Successful 3D reconstruction capabilities

## Future Improvements
- Integration into a mobile application
- Real-time processing capabilities
- Expanded dataset for improved accuracy
- Enhanced 3D reconstruction for single wheal analysis

## Citation
If you use this project in your research, please cite:
```
Shaik, J. (2024). Automated Reading of Skin Prick Test. 
BITS Pilani, Dubai Campus.
```

## License
This project is part of academic research at BITS Pilani, Dubai Campus.

## Contact
Jannath Shaik
Email: jannathshaik4@gmail.com
LinkedIn: linkedin.com/in/jannathshaik1511ac
