# Image Colorization with Intermediate Stage Visualization (512×512)

This project demonstrates an **image colorization pipeline** using a deep learning model that converts **grayscale images to color**.  
It also **visualizes intermediate stages** of the colorization process so you can see how the network gradually adds colors layer-by-layer.

## Features
- Trains a CNN-based model to colorize images.
- Works with **512×512 resolution** images for higher-quality results.
- Uses a real-world dataset (**COCO** or similar large image dataset via TensorFlow/Keras API).
- Plots **loss curves** and evaluation metrics.
- Displays intermediate layer outputs for visualization.
- Saves the trained model as `colorization_model.h5`.
- Prints **training logs** in the notebook output.

---

## Dataset
The example code downloads a subset of the **COCO dataset** using `tensorflow_datasets`.
You can change the dataset source in the code if you want to train on your own custom dataset.

---

## Installation
```bash
git clone <your-repo-url>
cd <your-project-folder>
pip install -r requirements.txt
````

---

## Usage

1. Open the `colorization_visualization.ipynb` file in **Jupyter Notebook** or **JupyterLab**.
2. Run the notebook cells to:

   * Load dataset
   * Preprocess images
   * Train the model
   * Visualize intermediate colorization stages
   * Save the model
3. Model will be saved as:

   ```bash
   colorization_model.h5
   ```

---

## Output Example

* **Training Loss Plot**
* **PSNR and SSIM Scores**
* **Intermediate Layer Outputs** (grayscale → partial color → final color)
* **HD 512×512 colorized images**

---

## Model Architecture

A U-Net-style CNN is used, where:

* Encoder extracts features from grayscale input.
* Decoder predicts the `a` and `b` color channels in Lab color space.
* Final output is converted back to RGB.

---

## Metrics Used

* **Mean Squared Error (MSE)**
* **Peak Signal-to-Noise Ratio (PSNR)**
* **Structural Similarity Index (SSIM)**

---

## Example Visualization

```
Layer 1 Output → Layer 3 Output → Layer 5 Output → Final Color Image
```

This helps in understanding how the network learns color gradually.

---

## Requirements

See [requirements.txt](requirements.txt)

---

## License

MIT License

````

---

## **`requirements.txt`**
```txt
tensorflow
tensorflow-datasets
numpy
matplotlib
scikit-image
opencv-python
tqdm
````