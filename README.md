# 🧠 Shape Detection in Images Using OpenCV
A computer vision project that uses Python and OpenCV to detect and classify basic geometric shapes such as circles, triangles, rectangles, squares, and stars in static images.

## 🔍 Project Overview
This project implements a **shape detection pipeline** using **OpenCV** in Python. It accurately identifies and labels shapes by analyzing their contours and polygonal approximations. The system is designed to work on images with simple shapes and clean backgrounds, making it ideal for educational use and basic computer vision tasks.

Two core notebooks are included:
 - gg.ipynb: Performs image preprocessing (grayscale conversion, edge detection).
 - shape.ipynb: Executes contour extraction, shape classification, and visual labeling.

## 🛠️ Tech Stack
 - Python 3.x
 - OpenCV (cv2)
 - NumPy
 - Jupyter Notebook

## 🖼️ Input Files
 - shapes-basic.png: Image used during preprocessing stage.
 - shapes.jpg: Main test image containing various shapes for final detection.
 - shape.pdf: IEEE-style report with full documentation, results, and discussion.

## 🧪 Key Features
### 📁 Image Preprocessing (gg.ipynb)
 - Load image using cv2.imread
 - Convert to grayscale using cv2.cvtColor
 - Apply edge detection via cv2.Canny with thresholds of 50 and 200

### 📐 Shape Detection (shape.ipynb)
 - Contour detection with cv2.findContours (external contours only)
 - Polygon approximation using cv2.approxPolyDP
 - Shape classification based on vertex count:
    - 3 → Triangle
    - 4 → Square or Rectangle (width ≈ height check)
    - 8 → Circle
    - 10 → Star

 - Centroid labeling with cv2.moments and cv2.putText
 - Visual rendering with cv2.drawContours (green outlines)

## 📊 Sample Output
In the sample image shapes.jpg, the system detected:

|Shape Type	|Vertices|	Status|
|-----|-----|-----|
|Triangl|	3	|✅ Detected|
|Square|	4	|✅ Detected|
|Rectangle|	4|✅ Detected|
|Circle|	8	|✅ Detected|
|Star	|10	|✅ Detected|
|Noise|	16|⚠️ Likely over-approximated|

## 🚀 How to Run the Project
### 🔧 Step 1: Clone the Repository
```bash
git clone https://github.com/pallavi01bs/ShapeDetectionOpenCV.git  
cd ShapeDetectionOpenCV
```

### 📦 Step 2: Install Dependencies
```bash
pip install opencv-python numpy
```

### ▶️ Step 3: Launch Notebooks
 - Run gg.ipynb to preprocess the image
 - Run shape.ipynb to detect, classify, and label the shapes
     - 💡 Tip: Use Jupyter Notebook or VSCode for best experience.

## ✅ System Requirements
### 🖥️ Hardware
 - Dual-core CPU or higher
 - Minimum 4 GB RAM

### 🧰 Software
 - Python 3.7+
 - Jupyter Notebook / Google Colab

## 📚 References
 - OpenCV Documentation
 - J. Canny, *A Computational Approach to Edge Detection*, IEEE TPAMI, 1986
 - Project Report: Report.dox (included)

## 📄 License
This project is licensed under the [MIT License](LICENSE).
