# Hateful Meme Detection Project

## Overview
This project aims to develop a multimodal model that can detect hateful content in memes by analyzing both image and text components.

## Prerequisites
Before running the project, ensure that you have the following installed:
- Python 3.6 or later
- Google Colab (for code execution)
- Basic understanding of Python, and familiarity with deep learning frameworks such as PyTorch, torchvision, and FastText.

## Dataset
The project uses the Facebook Hateful Meme Dataset, which can be downloaded from Kaggle:

- **Dataset Link**: [Facebook Hateful Meme Dataset](https://www.kaggle.com)

## Step-by-Step Instructions

### Step 1: Download and Prepare the Dataset
1. Go to the Kaggle link above and download the dataset as a zip file.
2. Rename the downloaded zip file to `archive.zip`.

### Step 2: Upload the Dataset to Google Drive
1. Access [Google Drive](https://drive.google.com).
2. Upload the `archive.zip` file to Google Drive, preferably in a dedicated project folder for better organization.

### Step 3: Access Google Colab
1. Open [Google Colab](https://colab.research.google.com).
2. Create a new notebook by selecting **File > New Notebook**.

### Step 4: Mount Google Drive in Colab and Unzip the Dataset
In your Colab notebook, run the following code to mount Google Drive and unzip the dataset. Be sure to replace `path_to_your_folder` with the actual path where you uploaded `archive.zip`:

### Step 5: Install Required Libraries
Install necessary libraries specified in src.ipynb to ensure the project runs correctly.

### Step 6: Execute the Project Code
After setting up, execute the code cells in the notebook in order. Ensure each cell runs sequentially to avoid issues.

### Step 7: Train the Model
Follow the instructions provided in the notebook to train the multimodal model using the dataset.

## Models Used in the Project

### 1. Vision Model: Torchvision
- **Purpose**: To extract features from meme images.
- **Architecture**: Common architectures include ResNet, EfficientNet, or MobileNet.
- **Functionality**:
  - Pre-trained on large datasets (such as ImageNet) for transfer learning.
  - Capable of capturing complex visual patterns and representations in memes.
- **Visual**: Diagram or image of the ResNet architecture (or other chosen model) for better understanding.

### 2. Language Model: FastText
- **Purpose**: To extract features from the text associated with memes.
- **Features**:
  - Generates word embeddings for input text.
  - Captures semantic meaning and word context.
- **Advantages**:
  - Handles out-of-vocabulary words better by using subword information.
  - Efficient and fast for training on large text datasets.
- **Visual**: Illustration demonstrating how FastText creates word embeddings, with example text and corresponding vector representations.

### 3. Multimodal Fusion Model: PyTorch
- **Purpose**: To combine features from both the vision and language models for meme classification.
- **Architecture**:
  - **Mid-level Concat Fusion**: Combines extracted features from vision and language models by concatenating them, then passes them through a classifier.
  - **Model Layers**:
    - Includes a series of fully connected layers for interpreting the fused features.
    - Dropout layers to reduce overfitting.
- **Training Framework**:
  - Uses PyTorch Lightning for streamlined training and validation processes.
- **Visual**: Diagram showing how outputs from the vision and language models are concatenated and passed through the final classifier layers.


