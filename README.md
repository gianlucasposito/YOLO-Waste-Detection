# YOLO-Waste-Detection

**YOLO-Waste-Detection** is an object-detection project built on the Ultralytics YOLOv8 framework to classify and localize five types of waste,Glass, Metal, Paper, Plastic, and Waste in images. 
Waste accumulation in urban and natural environments poses serious threats to human health, biodiversity, and climate. Computer vision offers scalable, accurate, and real-time monitoring of waste streams, boosting recycling yields and support proactive environmental management. 

## 📂 Repository Structure

```text
├── Image/                   # Folder containing sample images
├── runs/
│   └── detect/              # YOLOv8 inference outputs (predictions, annotated images)
├── best_model.pt            # Best YOLO model weights
├── Waste_Detection.ipynb    # Interactive Jupyter notebook demonstrating inference & training
├── requirements.txt         # Python dependencies
├── LICENSE                  # Project license
└── README.md                # Project overview
```

## 📊 Dataset

This project leverages the publicly available “Waste Detection” dataset from [utpalpaul108/waste-detection-using-yoloV5](https://github.com/utpalpaul108/waste-detection-using-yoloV5). It contains annotated images of five types of waste.

| 📂 Attribute            | 📈 Details                                                                                           |
|-------------------------|------------------------------------------------------------------------------------------------------|
| **Number of images**    | 4127                                                                                                |
| **Splits**              | • **Train:** 3502 images <br>• **Validation:** 580 images <br>• **Test:** 45 images                  |
| **Classes**             | 5                                                                                                    |
| **Class names**         | `Glass`, `Metal`, `Paper`, `Plastic`, `Waste`                                                         |
| **Source repo**         | [utpalpaul108/waste-detection-using-yoloV5](https://github.com/utpalpaul108/waste-detection-using-yoloV5) |


### 🚀 Project Content

Below is an overview of the main components in this repository:

---

### 🔄 1. Data Handling
- **Download & unzip**  
  Fetch the annotated dataset archive from Google Drive and extract into your project folder.  
- **Inspect & explore**  
  • Compute class-wise counts, image resolutions, and annotation statistics.  
  • Plot distribution charts (e.g. bar plots of class frequencies).  
- **Visualize samples**  
  Display a grid of representative images overlaid with their YOLO-format bounding boxes.

---

### 🏋️‍♂️ 2. Model Training & Evaluation
- **Train YOLOv8-nano**  
  • Configurable hyperparameters: epochs, batch size, learning rate, image size.  
  • Launch training with a single CLI command or via the provided Python script.  
- **Checkpoint selection**  
  Automatically track mAP@0.5 on validation split and save the “best” weights.  
- **Comprehensive evaluation**  
  After training, evaluate on both validation and test splits, reporting:  
  - **mAP@0.5**  
  - **mAP@0.75**  
  - **COCO mAP@0.5:0.95**  

---

### 🔍 3. Inference & Visualization
- **Batch inference**  
  Run the best model on your test-set folder to generate predictions.  
- **Result overlays**  
  Annotate images with predicted boxes, class labels, and confidence scores.  
- **Custom image testing**  
  Drop in your own photos (e.g. smartphone snapshots) to assess real-world generalization.

---

> 💡 _Tip:_ All scripts accept `--help` flags for detailed usage instructions and alternative workflows.  


















### A

It includes:

- **Data Handling**:  
  - Download & unzip dataset from Google Drive  
  - Explore data distribution and visualize sample images  

- **Model Training & Evaluation**:  
  - Train YOLOv8-nano with configurable epoch schedules  
  - Track and select the best model based on mAP@0.5  
  - Evaluate performance on validation and test splits (mAP@0.5, mAP@0.75, mAP@0.5:0.95)

- **Inference & Visualization**:  
  - Display predictions on test-set images  
  - Test generalization on user-provided photos  

### Installation

```bash
git clone https://github.com/gianlucasposito/YOLO-Waste-Detection.git    
cd Waste_Detection
pip install -r requirements.txt
