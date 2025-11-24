# 🐠 YOLOv8 – Object Detection on Aquarium Dataset  
This project implements **Ultralytics YOLOv8** for detecting underwater objects from the **Aquarium Dataset**, including different species of fish and aquatic animals. The repository contains the full workflow — dataset preparation, training scripts, evaluation metrics, and inference pipeline.

## 🚀 Project Summary  
The goal of this project is to build an efficient and accurate underwater object detection model using **YOLOv8**, the latest iteration of the YOLO (You Only Look Once) family.  
YOLOv8 provides improved detection accuracy, better training stability, and faster inference compared to its predecessors.  

This model is trained on the **Aquarium Dataset**, which contains labeled images of multiple aquatic species in varying underwater conditions. The system can classify and localize objects such as:  
- Fish species  
- Jellyfish  
- Penguins  
- Starfish  
- Sharks  
- Other underwater organisms  

## 📁 Dataset: Aquarium Dataset  
The dataset includes:  
- High-resolution underwater images  
- Multiple classes of aquatic species  
- Varying lighting, water clarity, and backgrounds  
- Bounding-box annotations in YOLO format  

Dataset link: *(Add your dataset link here)*  

## 🧠 YOLOv8 Architecture Explained  
YOLOv8 follows a modernized object detection architecture consisting of three main parts:

### **1. Backbone – CSPDarknet-inspired**  
- Extracts hierarchical visual features  
- Uses **C2f modules** for efficient gradient flow  
- Includes **SPPF** for multi‑scale feature learning  

### **2. Neck – Feature Fusion**
- PAN-based architecture  
- Combines features from different layers  
- Strengthens multi-scale detection  

### **3. Head – Decoupled Detection Head**  
- Separate branches for classification & regression  
- Predicts bounding boxes, objectness, and class scores  
- Anchor‑free → simpler and faster  

## 📦 Installation  
```
pip install ultralytics
```

## 🛠️ Training the Model  
```
yolo detect train data=aquarium.yaml model=yolov8n.pt epochs=50 imgsz=640
```

## 🔍 Inference  
```
yolo detect predict model=runs/detect/train/weights/best.pt source=sample.jpg
```

## 📊 Evaluation Metrics  
- mAP50  
- mAP50‑95  
- Precision  
- Recall  
- Loss curves  

## 📈 Results  
(Add sample predictions, curves, or weights link)

## 🧩 Folder Structure  
```
├── datasets/
├── runs/
├── aquarium.yaml
├── README.md
└── requirements.txt
```

## 📝 Conclusion  
This project demonstrates how **YOLOv8** can be effectively used for underwater object detection tasks. Its improved architecture and strong multi‑scale detection ability help achieve solid performance on the **Aquarium Dataset**, making it valuable for marine biology research, underwater robotics, and environmental monitoring.
