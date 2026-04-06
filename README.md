# 🚗 Vehicle Counting with YOLOv5 — Abbey Road Crossroad

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![YOLOv5](https://img.shields.io/badge/YOLOv5-s-green)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-red)
![License](https://img.shields.io/badge/License-MIT-yellow)

> Real-time vehicle detection and counting system applied to the iconic
> Abbey Road pedestrian crossing in London, using YOLOv5s and OpenCV.

---

## 📊 Results

| Metric | Value |
|---|---|
| Detection Confidence | **90%** |
| Processing Speed | **30 FPS** |
| Vehicles Counted | **50+** |
| Model | YOLOv5s |
| Input | MP4 video |

---

## 🎯 Overview

This project implements an automated vehicle counting pipeline on a
fixed-angle traffic video of Abbey Road, London. A virtual counting
line is drawn across the frame — any vehicle crossing it gets detected
and counted using YOLOv5s for object detection and OpenCV for tracking.

**Key features:**
- Real-time object detection with YOLOv5s (pretrained on COCO dataset)
- Virtual line crossing logic for accurate vehicle counting
- Works on any fixed-camera MP4 video input
- Bounding box visualization with class labels and confidence scores

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **YOLOv5s** — lightweight object detection model
- **OpenCV** — video processing and visualization
- **PyTorch** — YOLOv5 inference backend

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/rowan26/YoloV5-Tokyo_Car_Counting
cd YoloV5-Tokyo_Car_Counting
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the vehicle counter
```bash
python count.py --source video/abbey_road.mp4
```

---

## 📁 Project Structure
YoloV5-Tokyo_Car_Counting/
│
├── count.ipynb              # Main counting script
├── video/
│   └── abbey_road.mp4    # Input video
└── README.md

---

## 🧠 How It Works

1. **Load video** — OpenCV reads the MP4 frame by frame
2. **Detect vehicles** — YOLOv5s runs inference on each frame
3. **Filter classes** — only cars, trucks, buses, motorcycles are kept
4. **Count crossings** — a virtual line tracks when a vehicle crosses
5. **Display results** — bounding boxes and counter overlaid on video

---

## 📌 Limitations & Future Work

- Currently works on a single fixed video — no live stream support yet
- Could be extended with multi-class counters (cars vs trucks vs bikes)
- Future: add SORT/DeepSORT tracker for more robust multi-object tracking
- Future: deploy as a Streamlit web app for live demo

---

## 👤 Author

**Rowan HADJAZ**
- GitHub: [@rowan26](https://github.com/rowan26)
- LinkedIn: [rowan-hadjaz](https://linkedin.com/in/rowan-hadjaz)
