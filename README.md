# REAL-TIME FACE RECOGNITION SYSTEM

## Overview

This project is a Real-time Face Recognition System developed using Python and the OpenCV library. The system is designed to collect face data, train a machine learning model, and identify users (e.g., students) in real-time from a camera stream (webcam or specified IP camera).

This project serves as a practical demonstration of applying basic **Computer Vision** and **Machine Learning** algorithms (specifically LBPH) to real-world security or attendance applications.

## Technology Stack

* **Language:** Python 3.x
* **Key Libraries:**
    * `opencv-python` (cv2): Image processing, data collection, and Face Recognition.
    * `numpy`: Array manipulation.
    * `json`: User data management.
* **Algorithms/Models:**
    * **Face Detection:** Haar Cascade Classifier (`haarcascade_frontalface_default.xml`).
    * **Face Recognition:** Local Binary Pattern Histograms (LBPH) Face Recognizer.

## Key Features

| File | Functionality | Description |
| :--- | :--- | :--- |
| `GetData.py` | Data Collection | Uses the camera to capture face samples for a specified user (StudentID), saved to the `images/[StudentID]` directory. |
| `Train.py` | Model Training | Reads images, performs pre-processing, and trains the LBPH model. The trained model is saved as `data/recognition.yml`. |
| `Recognize.py` | Real-time Recognition | Loads the trained model to perform real-time face identification, displaying the recognized ID, Name, and Class (fetched from `data.json`). |
| `utils/pre_process.py` | Image Pre-processing | Contains essential functions (Grayscale conversion, Histogram Equalization, Gaussian Blur) to enhance input
