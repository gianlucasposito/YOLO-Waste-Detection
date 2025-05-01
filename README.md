# YOLO-Waste-Detection

**YOLO-Waste-Detection** is an object-detection project built on the Ultralytics YOLOv8 framework to classify and localize five types of waste,Glass, Metal, Paper, Plastic, and Waste in images. It includes:

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
