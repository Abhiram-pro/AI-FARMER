# AI-FARMER: Soil Image Classification

This project is a part of the **Soil Image Classification Challenge - 2025**. The goal is to classify soil images into four categories: Alluvial Soil, Black Soil, Clay Soil, and Red Soil.

## 👥 Team Name
**AI Farmer**

## 👨‍💻 Team Members
- Anish Raj  
- Utkarsh Umang  
- Abhiram Ganji  

## 🚀 Approach

- Used **ResNet50** with **pretrained ImageNet weights**
- Fine-tuned only the last block (`layer4`) and the fully connected (`fc`) layer
- Applied standard **224x224 resizing**, normalization, and **stratified split** of the dataset
- Trained using **CrossEntropyLoss** and **Adam optimizer**
- Used the **provided dataset** 
- Generated predictions on internal test images and visualized results using **confusion matrix** and **classification report**

## 🔍 Dataset

- `train_labels.csv`: Contains image IDs and soil types
- `test_ids.csv`: Contains test image IDs for prediction
- Image folders: `train/` and `test/`s

## 🧠 Model Summary

- **Backbone**: ResNet50
- **Image Size**: 224x224
- **Training Epochs**: 5
- **Loss**: CrossEntropyLoss
- **Optimizer**: Adam (`lr=1e-4`)
- **Batch Size**: 32

## 📊 Evaluation

- Weighted F1 score used as the primary metric
- Classification report and confusion matrix generated on the validation set

## 💾 Submission Format

Predictions are saved as `submission.csv` with columns:
- `image_id`
- `soil_type`

## 📌 How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the notebook:
   ```bash
   jupyter notebook soil_classification.ipynb
   ```

## 📬 Contact

For queries, reach out to any team member or open an issue in the repository.
