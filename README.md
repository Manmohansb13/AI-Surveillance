# AI-Surveillance

Use the working.ipynb file.
If windows laptops/Systems use CUDA torch instead of MPS.


# Overview

This project is an AI-based surveillance system for real-time video analysis. It detects and tracks individuals and identifies suspicious behavior such as loitering and meandering inside user-defined restricted zones.
The system uses YOLOv8 for person detection and DeepSort for multi-object tracking. Movement patterns and time spent in restricted areas are analyzed to flag suspicious activity, which is logged for later review.

# Key Features

Real-time person detection using YOLOv8 (Nano)

Multi-object tracking with persistent IDs using DeepSort

Restricted zone (ROI) monitoring

Loitering detection based on dwell time

Meandering detection using movement path analysis

CSV logging of suspicious events

Annotated output video with alerts

# Tech Stack

Python 3.12
YOLOv8 (Ultralytics)
DeepSort Realtime
OpenCV
Pandas
PyTorch

# Installation
pip install ultralytics deep-sort-realtime opencv-python pandas torch torchvision

# Usage

Place the input video (e.g., crowd.mp4) in the project directory.

Update paths in the script:

VIDEO_PATH = "crowd.mp4"
OUTPUT_PATH = "output_surveillance.mp4"


Run the script or notebook to process the video.

# Output

output_surveillance.mp4: Video with bounding boxes, tracking IDs, and alerts

suspicious_activity_log.csv: Logged suspicious events with timestamp and reason