# Scene Text Recognition

## Overview

This project focuses on Scene Text Recognition using advanced deep learning techniques. It combines text detection and recognition models to extract and interpret text from images. The project leverages YOLO for text detection and CRNN for text recognition, making it suitable for various OCR (Optical Character Recognition) applications.

## Features

- **Text Detection**: Utilizes YOLO models (`yolov8m.pt` and `yolo11n.pt`) for detecting text regions in images.
- **Text Recognition**: Employs a CRNN model (`ocr_crnn.pt`) for recognizing text within detected regions.
- **Dataset Management**: Includes tools for dataset preparation and annotation.
- **Visualization**: Provides utilities for visualizing detection and recognition results.

## Project Structure

```
source/
├── all.ipynb               # Combined notebook for end-to-end processing
├── TextDetection.ipynb     # Notebook for text detection
├── TextRecognition.ipynb   # Notebook for text recognition
├── ocr_crnn.pt             # Pre-trained CRNN model
├── yolov8m.pt              # YOLOv8 model for text detection
├── yolo11n.pt              # YOLO model for text detection
├── datasets/               # Dataset directory
│   ├── yolo_data/          # YOLO formatted data
│   │   ├── data.yaml       # Dataset configuration
│   │   ├── train/          # Training data
│   │   ├── val/            # Validation data
│   │   └── test/           # Test data
├── runs/                   # Directory for model outputs
│   ├── detect/             # Detection results
│   │   ├── train/          # Training results
│   │   └── val/            # Validation results
├── SceneTrialTrain/        # Raw image data and annotations
│   ├── locations.xml       # Location annotations
│   ├── segmentation.xml    # Segmentation annotations
│   ├── words.xml           # Word-level annotations
│   └── apan...
```

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/KietAPCS/Scene_Text_Recognition.git
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the pre-trained models (`ocr_crnn.pt`, `yolov8m.pt`, `yolo11n.pt`) and place them in the `source/` directory.

## Usage

### Text Detection

1. Open `TextDetection.ipynb`.
2. Follow the instructions to detect text regions in images.

### Text Recognition

1. Open `TextRecognition.ipynb`.
2. Follow the instructions to recognize text from detected regions.

### End-to-End Processing

1. Open `all.ipynb`.
2. Run the notebook to perform text detection and recognition in a single pipeline.

## Dataset Preparation

1. Place your images in the `SceneTrialTrain/` directory.
2. Update the `data.yaml` file in `datasets/yolo_data/` with the correct paths.
3. Use the provided tools to convert annotations to YOLO format if necessary.

## Results

- Detection and recognition results are saved in the `runs/` directory.
- Visualizations of detections and recognized text are available for review.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- YOLO: [Ultralytics YOLO](https://github.com/ultralytics/yolov5)
- CRNN: [CRNN for OCR](https://github.com/meijieru/crnn.pytorch)
