# Interactive User-Guided Image Colorization

## Overview
This project implements an interactive application for user-guided colorization of grayscale images. Users can upload grayscale photos, specify pixel locations as hints, and assign individual colors to each hint point to influence the final colorized output. A deep neural network based on a U-Net architecture with residual blocks processes the image along with these hints to produce a personalized, high-quality colorization.

## Features
- Upload grayscale images and resize to 256x256 for model processing.
- Specify multiple pixel locations (`x, y`) for color hints.
- Assign distinct hex color codes to each hint point for precise control.
- Add or reset hint points using interactive buttons.
- Dynamic colorization output reflecting user hint colors.
- Display image metrics such as resolution, unique grayscale levels, and hint count.

## Usage
1. Run the app to launch a web-based GUI.
2. Upload a grayscale image.
3. Use **Add Hint** to add rows; specify the coordinate and hex color per hint.
4. Use **Reset Hints** to clear all hint points.
5. Click **Colorize** to process and see the colorized image.
6. View relevant image and hint metrics below the output.

## Architecture
- Input tensor consists of luminance (L) and user-provided ab color hints plus a hint mask.
- Encoder downsamples input and extracts multi-scale features using convolutional layers and residual blocks.
- Bottleneck applies deeper feature transformations.
- Decoder upsamples with transposed convolutions, concatenates corresponding encoder features via skip connections, and refines via residual blocks.
- Output predicts ab color channels normalized in LAB space.
- Postprocessing converts LAB output with the original luminance to RGB color images.

## Technologies
- **PyTorch:** Deep learning framework for model architecture and inference.
- **OpenCV & PIL:** Image preprocessing, color space conversions.
- **Gradio:** Web-based interactive GUI.
- **Pandas:** For robust handling of hint points table input.

## Limitations
- The model requires pretrained weights for high-quality results; current code provides architecture scaffold.
- Input coordinates must match resized image dimensions (256x256).
- Color accuracy relies on user-provided hints distribution and colors.

## Potential Improvements
- Train and integrate pretrained colorization models.
- Add freehand or brush-based hint inputs.
- Support higher resolution images with multi-scale architectures.
- UI enhancements such as undo, redo, and real-time hint visualization.

## Installation
1. Install Python 3.8+ and required packages:
   ```
   pip install -r requirements.txt
   ```
2. Run the main script to launch the application.

## License
This project is open source for academic and personal use.
