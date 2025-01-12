# Brain Disease Detection System

## Overview
### Brain Stroke
A brain stroke, also known as a cerebrovascular accident (CVA), occurs when blood flow to a part of the brain is interrupted, leading to brain cell damage. Symptoms may include sudden numbness, difficulty speaking, and severe headache. Timely diagnosis and treatment are critical, as early intervention can significantly improve recovery outcomes.

### Brain Tumor
A brain tumor is an abnormal growth of cells within the brain or surrounding tissues. Tumors can be benign (non-cancerous) or malignant (cancerous) and can arise from brain cells or spread from other parts of the body.

This project is a comprehensive and efficient Brain Stroke and Tumor Detection System built using advanced machine learning and medical imaging techniques. It aims to aid medical professionals in the early diagnosis of strokes and brain tumors, potentially improving patient outcomes through timely intervention.

## Key Features
### Brain Stroke Detection 
- **Enhanced MLP Neural Network:** Utilizes a Multi-Layer Perceptron (MLP) model to predict the likelihood of a brain stroke based on various input features.
- **Classification of Brain Stroke:** Implements a Convolutional Neural Network (CNN) to analyze MRI/CT images and classify brain strokes as either **ischemic** or **hemorrhagic** once predicted.
  
### Brain Tumor Detection and Segmentation 
- **U-Net Model for Segmentation:** Employs a U-Net architecture to segment brain tumors in medical images. This model is specifically trained to identify and classify the following features:
    - **No Tumor:** Indicates the absence of any tumor.
    - **Necrotic/Core:** Represents dead or dying tissue within a tumor, suggesting advanced tumor progression.
    - **Edema:** Detects swelling caused by excess fluid around the tumor, which can indicate the tumor's impact on surrounding brain tissue.
    - **Enhancing:** Identifies areas of the tumor that show abnormal blood vessels and a disrupted blood-brain barrier.

### Web-Based Implementation
- **Frontend Technologies:** Developed using HTML, JavaScript, and CSS, providing a user-friendly interface for interaction.
- **Backend Framework:** Utilizes Flask to handle requests and manage the backend logic of the application, including model predictions and image processing.

### Predictive and Diagnostic Capabilities
- **Predictive Analysis:** Provides predictions on stroke likelihood based on user-input features, aiding in early diagnosis.
- **Tumor Feature Identification:** Helps in identifying specific tumor characteristics, which can guide treatment decisions.
  
**Technologies used -** 
 - Frontend: HTML, CSS, JavaScript
 - Backend: Python, Flask
 - Machine Learning: NumPy, Pandas, scikit-learn, TensorFlow or Keras
 - Deep Learning: Convolutional Neural Networks (CNN), U-Net architecture, Multi-Layer Perceptron (MLP)
 - Data Visualization: Matplotlib 

## Dataset
### Sources
- <a href="https://www.kaggle.com/code/alphajr7/95-accuracy/input?select=brains_Stroke_final+-+brains_Stroke_final.csv" target="_blank">Brain Stroke Dataset</a>
- <a href="https://www.kaggle.com/datasets/noshintasnia/brain-stroke-prediction-ct-scan-image-dataset/data" target="_blank">CT Scan Image Dataset</a>
- <a href="https://www.kaggle.com/datasets/awsaf49/brats2020-training-data" target="_blank">BRATS 2020 Training Data</a>
- <a href='https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/44RCPZ'>Replication Data for: Prediction of Cerebral Stroke</a>

### Pre-Processing
- **Data Augmentation** was performed on MRI Scans in order to prevent overfitting and and memoization.
- **Rescaling** and **Resize** was performed for better segmentations.
- **Normalization** was performed for faster convergence and reduced risk of Exploding/Vanishing Gradients.
 
## Model Performance
### Evaluation Metrics
- Accuracy
- Precision
- Recall
- Confusion Matrix
- F1-score
- ROC-AUC
- Validation Loss
- Sensitivity
- Specificity
  
### Best Models Results
**Multi-Layer Perceptron (MLP):**
- Accuracy: 94.67%
- Precision: 0.91
- F1 Score: 0.95
- Validation Loss: 0.0136
  
**CNN Architecture:**
- Test Accuracy: 98.1%
- Test Loss: 0.627
  
**U-Net Architecture:**
- Test Accuracy: 99.26%
- Precision: 99.4%
- Specificity: 99.79%
- Sensitivity: 99.04%
  
## Model Evaluation and Visualizations
<details>
  <summary><b>Multi-Layer Perceptron (MLP)</b></summary>
  
  <p>Confusion Matrix:</p>
  <img src="stats_images/confusion_matrix.png" alt="drawing" width="500"/>

  <p>Precision-Recall Curve:</p>
  <img src="stats_images/precision_recall.png" alt="drawing" width="500"/>

  <p>ROC-AUC Curve:</p>
  <img src="stats_images/ROC-AUC.png" alt="drawing" width="500"/>
</details>

<details>
  <summary><b>CNN Architecture</b></summary>
  
  <p>Data Distribution:</p>
  <img src="stats_images/distrCNN.png" alt="drawing" width="500"/>

  <p>Accuracy VS Epoch:</p>
  <img src="stats_images/accuracyVSepoch.png" alt="drawing" width="500"/>

  <p>Loss VS Epoch:</p>
  <img src="stats_images/LossVSEpoch.png" alt="drawing" width="500"/>
</details>

<details>
  <summary><b>U-Net Architecture</b></summary>
  <p>Data Distribution:</p>
  <img src="stats_images/distrU-net.png" alt="drawing" width="500" />

  <p>Accuracy Graph:</p>
  <img src="stats_images/accuracyU-net.png" alt="drawing" width="500"/>

  <p>Predicted VS Original Segmentation:</p>
  <img src="stats_images/outputU-net.png" alt="drawing" width="500"/>
  
</details>

## Contact
### Authors
- Avyukth Inna
- Ayman Khan
- Brijesh S G
- Samraat Dabolay

## References
- <a href='https://wseas.com/journals/bab/2023/a425108-017(2023).pdf'>Deep Learning based Brain Stroke Detection using VGGNet</a>
- <a href='https://www.kaggle.com/code/noshintasnia/neurostrokenet-an-innovative-neural-architecture'>NeuroStrokeNet: An Innovative Neural Architecture</a>
- <a href='https://paperswithcode.com/paper/u-net-convolutional-networks-for-biomedical'>U-Net: Convolutional Networks for Biomedical Image Segmentation</a>
- <a href='https://www.kaggle.com/code/alphajr7/95-accuracy/notebook'>Kaggle NoteBook</a>
