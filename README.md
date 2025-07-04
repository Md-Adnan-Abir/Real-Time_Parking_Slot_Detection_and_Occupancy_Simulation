# Real-Time Vehicle Occupancy Monitoring in Parking Lots Using OpenCV and Streamlit

---

## Overview

**ParkVision** is a real-time smart parking system that uses **OpenCV** for computer vision and **Streamlit** for visualization.  
It analyzes live or recorded video feeds to detect occupied and free parking slots, simulates vehicle movement over time, and displays results in a web-based dashboard.

This project was developed as part of the **Advanced Modeling and Simulation** course to showcase:

- Image processing and filtering
- Discrete event simulation
- Real-time visualization

---

## Features

• Automatic parking slot occupancy detection  
• Stochastic simulation of vehicle arrivals and departures  
• Real-time dashboard with live video feed and charts  
• Customizable parking layouts (manual slot definition)  
• Exportable CSV reports (optional)

---

## How It Works

1. **Mark parking spots** manually in a reference image using `ParkingSpacePicker.py`.
2. **Run the main Streamlit app** to process video frames.
3. The system applies:
   - Grayscale conversion
   - Gaussian blur
   - Adaptive thresholding
   - Contour dilation
4. Each parking area is cropped and analyzed for pixel density.
5. Results are displayed live and simulated with random variability.

---

## Installation

### Prerequisites

- Python 3.7+
- pip

### Quick Setup

Clone the repository:

```bash
git clone https://github.com/Md-Adnan-Abir/Real-Time_Vehicle_Occupancy_Monitoring
cd Real-Time_Vehicle_Occupancy_Monitoring
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install opencv-python streamlit numpy
```

---

## 🛠️ Usage

### 1️. Define Parking Slots

Run the slot picker tool:

```bash
python ParkingSpacePicker.py
```

- Click each parking slot on the displayed image.
- Close the window when done. The positions will be saved to `carParkPos`.

---

### 2️. Start the Detection & Simulation Dashboard

Run the main app:

```bash
streamlit run main.py
```

- Use the checkbox to start/stop simulation.
- View real-time occupancy and trends.

---


##  Future Enhancements

- YOLO-based slot and vehicle detection
- Night-time image processing improvements
- Cloud deployment (Streamlit sharing)

---

##  License

This project is for educational purposes. You may adapt and share under the MIT License.

---
