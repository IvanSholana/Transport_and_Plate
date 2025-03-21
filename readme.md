# License Plate Detection and Tracking System

## Overview
This project implements a **license plate detection and tracking system** using **YOLOv8 and OpenCV**. The system processes video footage captured on highways, detects vehicles, identifies license plates, and saves cropped license plate images.

## Features
- **Vehicle Detection & Tracking**: Identifies and tracks vehicles in a video stream.
- **License Plate Detection**: Detects license plates within the detected vehicles.
- **Automatic Cropping & Saving**: Extracts and saves detected license plates.
- **Real-time Processing**: Processes frames dynamically for real-time applications.
- **Optimized Display**: Resizes frames for better visualization on different screen resolutions.

## Technologies Used
- **YOLOv8**: Object detection model for vehicle and license plate recognition.
- **OpenCV**: Image processing and video handling.
- **NumPy**: Efficient numerical operations.
- **Matplotlib**: For debugging and visualizing results.
- **Google Cloud**: (Optional) Deployment of the model and service.

## Installation
### Prerequisites
Ensure you have Python installed (>=3.8) and install required dependencies:

```sh
pip install ultralytics opencv-python numpy matplotlib
```

## Usage
1. **Prepare the Model**
   - Place the trained YOLOv8 model (`best.pt`) inside `./model/client_model/`.

2. **Provide Video Input**
   - Store video files inside `./dataset/Video/` and update `video_path` accordingly.

3. **Run the Script**
   ```sh
   python main.py
   ```

4. **Output**
   - Detected license plate images are saved in `./license_predict/`.
   - The system displays real-time tracking in a resizable window.

## Code Structure
```
├── model/
│   ├── client_model/
│   │   ├─ best.pt  # YOLOv8 trained model
│
├── dataset/
│   ├── Video/
│   │   ├── sample.mp4  # Sample video for testing
│
├── license_predict/  # Directory for saving detected license plate images
│
├── main.py  # Main script for detection and tracking
│
├── README.md  # Project documentation
```

## Future Improvements
- Improve model accuracy with **better dataset augmentation**.
- Deploy as a web API for **real-time cloud processing**.
- Implement **OCR (Optical Character Recognition)** for reading license plate numbers.

## Acknowledgments
This project leverages **Ultralytics YOLOv8** and **OpenCV** for efficient detection and tracking.
