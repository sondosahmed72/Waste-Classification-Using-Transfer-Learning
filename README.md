# Waste Classification Using Transfer Learning

This project aims to classify waste images into **recyclable** and **organic** categories using **transfer learning** with the **VGG16** model. It automates waste sorting to improve efficiency and reduce contamination.

## Project Scenario
The city of GreenCity struggles with waste management, especially distinguishing between recyclable and organic waste. EcoClean wants an AI-powered solution to automatically classify waste products using image recognition.

## Aim
Develop an automated waste classification model capable of accurately differentiating between recyclable and organic waste.

## Dataset
The dataset is organized in the following directory structure:

o-vs-r-split/
├── train
│ ├── O
│ └── R
└── test
├── O
└── R


- **O**: Organic waste  
- **R**: Recyclable waste  

## Project Steps / Tasks
1. Print the version of TensorFlow.  
2. Create a `test_generator` using the `test_datagen` object.  
3. Print the length of the `train_generator`.  
4. Print the summary of the model.  
5. Compile the model.  
6. Plot accuracy curves for training and validation sets (Extract Features Model).  
7. Plot loss curves for training and validation sets (Fine-Tune Model).  
8. Plot accuracy curves for training and validation sets (Fine-Tune Model).  
9. Plot a test image using the Extract Features Model.  
10. Plot a test image using the Fine-Tuned Model.  

## Model Architecture
- Base: Pre-trained **VGG16** without top layers (weights from ImageNet).  
- Added layers:
  - Flatten  
  - Dense(512, activation='relu')  
  - Dropout(0.3)  
  - Dense(512, activation='relu')  
  - Dropout(0.3)  
  - Dense(1, activation='sigmoid')  

- **Loss function**: Binary Crossentropy  
- **Optimizer**: RMSprop (learning_rate=1e-4)  
- **Metrics**: Accuracy  

## Results
- Accuracy and loss curves are plotted for training and validation sets.  
- Model predictions on test images are visualized with actual and predicted labels.  

## Requirements
- Python 3.x  
- TensorFlow 2.x  
- Keras  
- Matplotlib  
- NumPy  

