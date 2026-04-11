# AI-Powered-Defect-Detection-System
# AI-Powered Fabric Defect Detection System

An intelligent and lightweight computer vision system designed to automatically detect defects in **single-colour fabrics** using image processing and machine learning techniques.

---

## Project Overview

This system identifies three major types of fabric defects:

1. **Holes / Broken Yarn (Structural Defects)**
2. **Colour Variation (Shade Differences)**
3. **Dirt / Stains (Surface Contamination)**

The solution is optimized for:
- ✅ Single-colour fabric inspection  
- ✅ Low computational cost  
- ✅ Real-time or near real-time deployment  
- ✅ Small and medium-scale textile industries  

---

## System Architecture

The system follows a **parallel multi-module architecture**:

Input Image
↓
Global Preprocessing
↓
Parallel Analysis
├── Structure Analysis (Module 1)
├── Colour Analysis (Module 2)
└── Cleanliness Analysis (Module 3)
↓
Result Aggregation
↓
Final Decision (Pass / Defective)
↓
Inspection Report


---

## Modules Description

### Module 1: Holes / Broken Yarn Detection
- Converts image to grayscale  
- Uses AI model to detect structural defects  
- Applies Non-Max Suppression (NMS)  
- Outputs bounding boxes with defect labels  

---

### Module 2: Colour Variation Detection
- Converts RGB → LAB colour space  
- Computes colour difference using ΔE (2000)  
- Uses ML model to classify shade variations  
- Handles illumination changes using CLAHE  

---

### Module 3: Dirt / Stains Detection
- Retains RGB channels  
- Uses lightweight CNN + thresholding  
- Generates binary defect masks  
- Detects low-contrast stains under uneven lighting  

---

## Key Features

- 🎯 Specialized for **single-colour fabrics**
- ⚡ Lightweight and efficient models
- 💡 Uses **LAB colour space + ΔE** for accurate colour analysis
- 🔆 Robust to lighting variations (illumination normalization)
- 💰 Cost-effective for real-world deployment
- 📊 Modular and scalable architecture

---

## Technologies Used

### Core
- Python

### Image Processing
- OpenCV
- scikit-image

### Machine Learning / AI
- TensorFlow / PyTorch
- scikit-learn

### Colour Analysis
- colormath

### Data Handling & Visualization
- NumPy
- Pandas
- Matplotlib

---

## Project Structure

fabric-defect-detection/
│
├── data/
├── models/
├── src/
│ ├── preprocessing/
│ ├── module1_structure/
│ ├── module2_color/
│ ├── module3_cleanliness/
│ ├── aggregation/
│ └── utils/
│
├── outputs/
├── notebooks/
├── tests/
├── requirements.txt
└── README.md


---

## Installation

### 1. Clone the repository
```bash
git clone <your-repo-link>
cd AI-POWERED-DEFECT-DETECTION-SYSTEM