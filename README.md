# GenAI-NullClass Internship Project

Welcome to the repository for my NullClass internship project, featuring three key tasks focused on image colorization using deep learning techniques.

## Project Overview

This project addresses advanced image colorization with multiple objectives, leveraging deep learning models and practical augmentations for improved results. 

The repository contains:

- **Task 1: Visualizing the Colorization Process**  
  Visualization tools and code to observe intermediate stages of colorization from grayscale input to fully colorized output. Includes layer-wise feature map extraction, color difference maps, and metrics plots to understand model behavior.

- **Task 2: Dataset Augmentation to Improve Colorization**  
  Implementation of different data augmentation techniques (rotation, flipping, brightness adjustments) for grayscale images to augment the training dataset. Demonstrates enhanced model performance on colorization after training on augmented data with before/after result comparisons.

- **Task 3: Interactive User-Guided Colorization**  
  A user-interactive colorization system allowing users to upload images, specify colors in select regions, and obtain dynamically influenced colorized images. Includes a basic GUI interface facilitating user inputs for personalized color guidance.

## Repository Structure

```
GenAI-NullClass/
│
├── Task1_Colorization_Visualization/
│   ├── colorization_visualization.ipynb           # Jupyter notebook with model & visualization code
│   ├── model_weights_task1.pth                     # Saved model weights for Task 1
│   └── README.md                                   # Documentation specific to Task 1
│
├── Task2_Data_Augmentation/
│   ├── data_augmentation_colorization.ipynb       # Notebook with augmented data pipeline & training
│   ├── model_weights_task2.pth                     # Saved model weights trained on augmented data
│   └── README.md                                   # Documentation specific to Task 2
│
├── Task3_Interactive_User_Guided_Colorization/
│   ├── user_guided_colorization.ipynb              # Notebook integrating user input with colorization model
│   ├── app/                                        # GUI app files (e.g., Flask, Streamlit, or other)
│   ├── model_weights_task3.pth                     # Model weights for Task 3
│   └── README.md                                   # Documentation specific to Task 3
│
├── requirements.txt                                # Python dependencies for entire project
└── README.md                                      # This main overview README
```

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ved0104/GenAI-NullClass.git
   cd GenAI-NullClass
   ```

2. Create and activate a Python virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Navigate to each task folder to run Jupyter notebooks for code execution and experimentation.

## Model Performance & Metrics

- The colorization models were evaluated using:
  - **Confusion Matrix**
  - **Precision**
  - **Recall**
  - **Perceptual Metrics (SSIM, LPIPS)**
  - **Colorfulness Scores**

- Models achieved a minimum accuracy of 70% on the evaluation dataset, improving after augmentation.

- Detailed metric reports and comparison plots are available in individual task notebooks.

## Usage

- Launch Jupyter notebooks in each task directory to train/evaluate models and see results.
- For Task 3, run the GUI application to enable interactive colorization:
  
  Example (if using Streamlit):
  ```bash
  streamlit run app/user_guided_colorization.py
  ```

## Saved Models

- Large model weights files are included in each task folder.
- Backup download links (Google Drive) are provided in the README files within each task folder for convenience.

## Contact

For questions or suggestions, please reach out to me via GitHub or email.
