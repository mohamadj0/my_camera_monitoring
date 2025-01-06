# Multi-Camera Monitoring Dashboard

A Python package for real-time monitoring and analysis of multiple camera feeds. This package allows you to detect various camera issues, including blur, resolution changes, occlusions, disconnections, and sudden impacts. It integrates with Streamlit for interactive visualization.

## Features

- **Blur Detection**: Detects if the camera feed is blurry based on the Laplacian operator.
- **Resolution Change Detection**: Monitors for resolution changes between frames.
- **Occlusion Detection**: Detects occlusions by analyzing the ratio of black or white pixels in the feed.
- **Disconnection Detection**: Detects if a camera feed is disconnected or if it stops sending data.
- **Sudden Impact Detection**: Identifies sudden changes in the video stream that might indicate an impact.

## Requirements

- Python 3.x
- OpenCV
- NumPy
- Streamlit

You can install the required dependencies using:

```bash
pip install -r requirements.txt
```
## Installation
### Installing from Wheel File
To install the package from a ```.whl``` file, run the following command:
```bash
pip install /path/to/your_package-name-version.whl
```
Replace ```/path/to/your_package-name-version.whl``` with the actual path to your downloaded ```.whl``` file.


## Usage
You can use this package easily by importing it into your code and utilizing its various functions to analyze images. For example:
```bash
import cv2
import numpy as np
from your_package_name import detect_blur_and_resolution_realtime, detect_occlusion, detect_disconnection, detect_sudden_impact

# Load image
image = cv2.imread('image.jpg')

# Detect blur and resolution
blur_percentage, resolution_status, current_resolution, prev_resolution = detect_blur_and_resolution_realtime(image)

# Display results
print(f"Blur Percentage: {blur_percentage}%")
print(f"Resolution Status: {resolution_status}")
```
