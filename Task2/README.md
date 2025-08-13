# README.md

## Dataset Augmentation to Improve Colorization

This project implements a convolutional neural network (CNN) model for automatic colorization of grayscale images. The colorization model leverages dataset augmentation (rotation, flipping, brightness/contrast adjustment) to improve both the robustness and the accuracy of colorization. The pipeline is written in PyTorch and demonstrated on the CIFAR-10 dataset.

### Features

- Converts color images to grayscale as inputs and uses the originals as color ground truth.
- Augments training data using random rotations, flips, and brightness/contrast changes.
- Trains a CNN-based autoencoder to learn colorization.
- Utilizes GPU acceleration via PyTorch when available.
- Visualizes and compares colorization results before and after augmentation.

## Getting Started

### 1. Installation

First, clone this repository and navigate to its directory.

Then, install the required packages using **pip**:

```bash
pip install -r requirements.txt
```

### 2. Running the Code

1. **Prepare the dataset:**  
   The script downloads CIFAR-10 automatically. No manual setup needed.

2. **Training:**
   - To train with both the original and augmented dataset, run the main script.
   - The code detects and uses available GPU automatically.

3. **Evaluation and Visualization:**
   - The script will plot comparison figures: input grayscale, ground truth color, and model output.
   - Evaluate both the baseline and augmented models for qualitative and quantitative comparison.

### 3. Project Structure

| File/Folder          | Description                                           |
|----------------------|------------------------------------------------------|
| `main.py`            | Main training and evaluation script                  |
| `requirements.txt`   | Lists required Python packages                       |
| `README.md`          | This file                                            |

### 4. Requirements

- Python 3.7+
- CUDA-compatible GPU (optional but recommended)

All other requirements are handled by pip (see `requirements.txt`).

## Example Usage

After installation, train and evaluate the model:

```bash
python main.py
```

You should see training loss messages followed by matplotlib plots showing original grayscale inputs, ground truth, and predicted colorizations.

## Customization

- To use a different dataset, adjust the `torchvision.datasets.CIFAR10` loader in the script.
- Add or modify augmentation techniques in the `aug_transform` within the code.
- Adjust network architecture in the model definition as needed.

## Notes

- Data augmentation here is implemented using `torchvision.transforms` for efficiency and flexibility.
- The project can be further improved with more advanced models like U-Net or GAN-based colorization.
