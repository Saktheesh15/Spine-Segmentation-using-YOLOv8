# Spine Segmentation using YOLOv8

A computer vision application for detecting and identifying different regions of the lumbar spine using the YOLOv8 object detection model.

The application detects six spine regions — **L1, L2, L3, L4, L5, and S1** — from uploaded medical images and displays the detected regions using bounding boxes.

> **Disclaimer:** This project is intended for educational and research purposes only. It is not a clinically validated medical application and should not be used for medical diagnosis or treatment decisions.

---

## Project Overview

Spine image analysis is an important area of medical imaging and computer vision. Identifying individual vertebrae manually can be a time-consuming process.

This project demonstrates how a YOLOv8-based deep learning model can be used to automatically detect different lumbar vertebrae and the sacral region from spine images.

A Streamlit-based user interface allows users to upload an image, run the trained YOLOv8 model, and visualize the detected spine regions.

---

## Features

- Spine region detection using YOLOv8
- Detection of six anatomical regions
- Image upload functionality
- Automatic model inference
- Bounding box visualization
- Class-specific visualization
- Interactive Streamlit web application
- Support for testing with sample images

---

## Detected Classes

The model is designed to detect the following six classes:

| Class | Description |
|---|---|
| L1 | First Lumbar Vertebra |
| L2 | Second Lumbar Vertebra |
| L3 | Third Lumbar Vertebra |
| L4 | Fourth Lumbar Vertebra |
| L5 | Fifth Lumbar Vertebra |
| S1 | First Sacral Vertebra |

---

## Why Spine Detection?

Automated spine region detection can support research in medical image analysis by helping identify and localize vertebral regions.

Potential research applications include:

- Automated identification of vertebral regions
- Medical image analysis research
- Computer-assisted image annotation
- Deep learning research on spinal imaging
- Development of medical computer vision systems
- Preparation of annotated data for further research

This project demonstrates the technical application of deep learning to spine image analysis and is not intended to replace professional medical evaluation.

---

## Technologies Used

- Python
- YOLOv8
- Ultralytics
- OpenCV
- Streamlit
- NumPy
- Computer Vision
- Deep Learning
- Machine Learning

---

## Project Structure

```text
Spine-Segmentation-using-YOLOv8/
│
├── datasets/
│   ├── data.yaml
│   └── weights/
│       ├── best.pt
│       └── last.pt
│
├── test_images/
│   └── Sample images
│
├── main.py
├── requirements.txt
├── .gitignore
└── README.md
```

> The exact folder structure may vary depending on how the dataset and trained model files are stored locally.

---

## Getting Started

### Prerequisites

Make sure Python is installed on your system.

Python 3.12 or a compatible version is recommended.

You can check your Python version using:

```bash
python --version
```

---

## Clone the Repository

Clone this repository using:

```bash
git clone https://github.com/Saktheesh15/Spine-Segmentation-using-YOLOv8.git
```

Navigate to the project directory:

```bash
cd Spine-Segmentation-using-YOLOv8
```

---

## Install Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

The project may require libraries such as:

```text
ultralytics
streamlit
opencv-python
numpy
Pillow
```

---

## Model Weights

The trained YOLOv8 model uses model weight files such as:

```text
best.pt
last.pt
```

`best.pt` represents the best-performing model checkpoint saved during training.

`last.pt` represents the model checkpoint from the latest training epoch.

If the model files are not included in this repository because of GitHub file-size limitations, place the required model weights in the appropriate local directory before running the application.

Example:

```text
datasets/
└── weights/
    └── best.pt
```

Make sure the model path used inside the Python application matches the actual location of the model file.

---

## Running the Application

Start the Streamlit application using:

```bash
streamlit run main.py
```

After running the command, Streamlit will start a local development server.

Open the displayed local address in your web browser.

It is typically:

```text
http://localhost:8501
```

---

## How to Use

1. Start the Streamlit application.
2. Open the application in your browser.
3. Upload a compatible spine image.
4. The image is processed by the YOLOv8 model.
5. The model detects the corresponding spine regions.
6. Bounding boxes and class labels are displayed on the processed image.
7. Review the model's prediction results.

---

## Test Images

Sample test images can be stored inside the:

```text
test_images/
```

directory.

These images can be used to test the model and verify the inference workflow.

---

## Class Visualization

The application detects the following classes:

```text
L1
L2
L3
L4
L5
S1
```

Different colors may be used to visually distinguish the detected classes.

Example:

| Class | Color |
|---|---|
| L1 | Red |
| L2 | Green |
| L3 | Blue |
| L4 | Cyan |
| L5 | Magenta |
| S1 | Yellow |

The actual colors displayed may depend on the visualization implementation used in the application.

---

## Model Workflow

The general workflow of the project is:

```text
Input Spine Image
        ↓
Image Preprocessing
        ↓
YOLOv8 Model
        ↓
Object Detection
        ↓
L1, L2, L3, L4, L5, S1 Detection
        ↓
Bounding Box Visualization
        ↓
Output Image
```

---

## Future Improvements

Possible future improvements include:

- Improve model accuracy using a larger dataset
- Add more diverse spine images
- Apply advanced data augmentation
- Experiment with different YOLO model variants
- Improve model performance through hyperparameter tuning
- Add confidence score visualization
- Deploy the Streamlit application online
- Add REST API support for model inference
- Compare YOLOv8 performance with other computer vision architectures

---

## Limitations

The performance of the model depends on several factors, including:

- Quality of the training dataset
- Accuracy of image annotations
- Number of training samples
- Image quality
- Model configuration
- Training parameters

Predictions generated by this project should not be considered medical diagnoses.

---

## Disclaimer

This project is developed for **educational, research, and portfolio purposes only**.

The model has not been clinically validated and must not be used for:

- Medical diagnosis
- Treatment recommendations
- Surgical planning
- Clinical decision-making

Always consult qualified healthcare professionals for medical evaluation and advice.

---

## Author

**Saktheesh**

GitHub: `Saktheesh15`

---

## Acknowledgements

This project uses the YOLOv8 framework provided by Ultralytics.

If any part of this project, including source code, model weights, datasets, or implementation, was adapted from an existing open-source repository or tutorial, the original project and authors should be credited here in accordance with the applicable license.

---

## License

Before distributing or modifying this project, verify the licenses of the original dataset, model weights, and any third-party source code used in the project.
