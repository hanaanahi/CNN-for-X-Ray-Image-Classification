# Project Overview

This project uses a Convolutional Neural Network (CNN) based on DenseNet121 to classify chest X-ray images into three categories: **NORMAL**, **PNEUMONIA**, and **TUBERCULOSIS**.

It is designed to run in **Google Colab**, with the dataset stored in **Google Drive**.

## Model Overview

- **Backbone**: DenseNet121 (pretrained on ImageNet)
- **Classifier Head**:
  - Global Average Pooling
  - Dense Layer (256 units, ReLU)
  - Dropout (0.5)
  - Final Dense Layer (3 units, softmax)
- **Loss**: Sparse Categorical Crossentropy
- **Optimizer**: Adam

## Dataset

**Data Access**

Not included in this repository. Due to file size limitations, the dataset is stored externally.

📁 [Download from Google Drive](https://drive.google.com/drive/folders/1J6ofaFcxfRwT96SHL6hcqD0rL0Hzr49p?usp=drive_link)

To use the data:
1. Download the file
2. Place it in the `data/` directory
3. Run the preprocessing script

**Expected Folder Structure in Drive:**

```
CS123B_Project/
├── train/
│   ├── NORMAL/
│   ├── PNEUMONIA/
│   └── TUBERCULOSIS/
├── test/
│   ├── NORMAL/
│   ├── PNEUMONIA/
│   └── TUBERCULOSIS/
└── Example_Patient_Xray.jpeg

```
**How to Run**

1. Open the `.ipynb` file in **Google Colab**
 
3. Run all cells to:
   
- Mount your Google Drive in colab

- Load and split the dataset

- Build and train the model

- Evaluate on validation and test sets

- Predict on an example image

<br>
  
**Output Metrics**

- Validation Accuracy

- Test Accuracy

- Training & Validation Loss Plot

- Example prediction for a patient image

<br>

**Test Case: Predict on a New X-ray Image**

1. Upload your image to Google Drive at the following path:

```markdown
img_path = '/content/drive/MyDrive/Example_Patient_Xray.jpeg'
```
2. Run the example case code block


### Note

This repository does not include the dataset due to GitHub's file size limitations. Please upload the dataset to your Google Drive manually as instructed.

## Author

**Hina Dawar** — [GitHub](https://github.com/hanaanahi)

This project was developed for the CS123B course on Deep Learning and Image Analysis.

