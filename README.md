```md
# Ego-Centric Hand Detection and Segmentation

This repository provides a Jupyter Notebook implementation for ego-centric hand detection and pixel-level segmentation. The pipeline combines lightweight object detection models from the YOLO family with prompt-based segmentation using the Segment Anything Model (SAM and SAM 2). The approach is designed to work robustly in real-world scenes with occlusions, cluttered backgrounds, and varying hand poses, while minimizing annotation effort.

---

## Features

- Ego-centric hand detection using YOLO models (YOLOv8–YOLOv11)
- Support for transformer-based detection with RT-DETR
- Prompt-based segmentation using SAM and SAM 2
- High detection and segmentation accuracy
- Reduced annotation effort through zero-shot segmentation
- Fully reproducible Jupyter Notebook workflow

---

## Pipeline

1. Hand detection using YOLO and RT-DETR models  
2. Selection of the best-performing detector (YOLOv9s)  
3. Use of detector bounding boxes as prompts for SAM-based segmentation  
4. Pixel-accurate hand mask generation  
5. Quantitative evaluation of detection and segmentation performance  

---

## Results

| Task | Metric | Value |
|------|-------|-------|
| Detection | mAP@0.5 | 98.8% |
| Detection | mAP@0.5:0.95 | 82.1% |
| Segmentation | Dice Score | 95.5% |
| Segmentation | IoU | 93.5% |

---

## Repository Structure

```

.
├── CODE
├── README.md


````

---

## Getting Started

### Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/USERNAME/REPO_NAME.git
   cd REPO_NAME
````

2. Install required dependencies:

   ```bash
   pip install torch ultralytics segment-anything opencv-python numpy matplotlib
   ```

3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open the `.ipynb` file and run all cells sequentially.

---

### Run on Google Colab

1. Open the notebook file on GitHub
2. Click **Open in Colab**
3. Run the notebook without local installation

---

## Requirements

* Python 3.x
* PyTorch
* Ultralytics YOLO
* RT-DETR
* Segment Anything Model (SAM / SAM 2)
* OpenCV
* NumPy
* Matplotlib

---

## Applications

* Human–robot interaction
* Ego-centric and first-person vision
* Augmented and mixed reality
* Assistive and wearable technologies

---

## Notes

* GPU acceleration is recommended for faster inference
* This repository is intended for research and educational use


