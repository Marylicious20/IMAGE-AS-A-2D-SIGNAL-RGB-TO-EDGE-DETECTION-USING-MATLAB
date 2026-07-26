# 🖼️ Image as a 2D Signal: RGB to Edge Detection using MATLAB

A MATLAB-based image processing project that demonstrates how digital images can be treated as **two-dimensional (2D) signals**. The project implements a complete image processing pipeline, converting an RGB image into grayscale, indexed, and binary representations before applying **Canny Edge Detection** to extract meaningful object boundaries.

This project was completed as part of the **Signals & Systems** course and provides practical experience in digital image representation, signal transformations, and feature extraction using MATLAB.

---

# 📖 Table of Contents

* Overview
* Project Objectives
* Features
* Theory
* Processing Pipeline
* Technologies Used
* Repository Structure
* Installation
* Usage
* Processing Stages
* Results
* Applications
* Learning Outcomes
* Future Improvements
* Screenshots
* Contributors
* References
* License

---

# 📌 Overview

Digital images can be represented as **2D signals**, where each pixel corresponds to a signal value defined by its spatial coordinates. Image processing techniques manipulate these signals to simplify data, enhance image quality, and extract important features.

This project demonstrates a step-by-step transformation of an RGB image through several representations:

* RGB Image
* Grayscale Image
* Indexed Image
* Binary Image
* Edge Detected Image

Each stage progressively reduces image complexity while preserving the information necessary for analysis.

---

# 🎯 Project Objectives

The objectives of this project are to:

* Represent an image as a two-dimensional signal.
* Convert RGB images into grayscale.
* Generate indexed image representations.
* Convert images into binary format using thresholding.
* Perform edge detection using the Canny algorithm.
* Analyze how each transformation affects image representation.
* Understand the relationship between signal processing and image processing.

---

# ✨ Features

* RGB image loading
* Grayscale conversion
* Indexed image generation
* Binary image creation
* Canny edge detection
* MATLAB implementation
* Interactive image selection
* Visualization of every processing stage
* Simple and modular code structure

---

# 🧠 Theory

Digital image processing extends traditional signal processing concepts into two dimensions.

An image can be viewed as a matrix where each element represents the intensity or color value of a pixel.

The processing pipeline follows these stages:

```text
RGB Image
     │
     ▼
Grayscale Conversion
     │
     ▼
Indexed Image
     │
     ▼
Binary Image
     │
     ▼
Canny Edge Detection
     │
     ▼
Extracted Object Boundaries
```

Each transformation simplifies the image while preserving the most significant structural information.

---

# ⚙️ Processing Pipeline

## 1. RGB Image

The input image is loaded into MATLAB.

RGB images contain three color channels:

* Red
* Green
* Blue

These channels provide complete color information but require more computational resources.

---

## 2. Grayscale Conversion

The RGB image is converted into grayscale using MATLAB's built-in function.

Benefits include:

* Reduced computational complexity
* Single intensity channel
* Easier image analysis

Function used:

```matlab
gray = rgb2gray(rgb);
```

---

## 3. Indexed Image

The grayscale image is converted into an indexed representation using a grayscale colormap.

Benefits:

* Efficient image storage
* Reduced memory usage
* Palette-based representation

Function used:

```matlab
[indexed, cmap] = gray2ind(gray,256);
```

---

## 4. Binary Image

Thresholding converts the indexed image into a binary image.

Pixels become:

* White (Foreground)
* Black (Background)

Function used:

```matlab
binary = imbinarize(indexed);
```

---

## 5. Edge Detection

The binary image is processed using the **Canny Edge Detection** algorithm.

Canny detects strong intensity changes corresponding to object boundaries.

Function used:

```matlab
edges = edge(binary,'Canny');
```

---

# 🛠️ Technologies Used

* MATLAB
* MATLAB Image Processing Toolbox
* Digital Image Processing
* Signal Processing Concepts
* Canny Edge Detection

---

# 📂 Repository Structure

```text
Image-as-a-2D-Signal/
│
├── Images/
│   ├── sample.jpg
│
├── Results/
│   ├── rgb.png
│   ├── grayscale.png
│   ├── indexed.png
│   ├── binary.png
│   └── edges.png
│
├── src/
│   └── image_processing.m
│
├── README.md
│
└── LICENSE
```

---

# 🚀 Installation

## Requirements

* MATLAB
* Image Processing Toolbox

Clone the repository:

```bash
git clone https://github.com/yourusername/Image-as-a-2D-Signal.git
```

Open MATLAB and navigate to the project folder.

---

# ▶️ Usage

Run the MATLAB script:

```matlab
image_processing
```

A file selection window will appear.

Choose any image in:

* JPG
* PNG
* BMP

The program automatically performs every processing stage and displays the results.

---

# 📊 Output

The application displays:

* Original RGB Image
* Grayscale Image
* Indexed Image
* Binary Image
* Edge Detected Image

A combined comparison window is also generated for easier visualization.

---

# 📈 Results

The project successfully demonstrates how different image representations simplify image analysis.

Observations include:

* Grayscale conversion significantly reduces data while preserving image structure.
* Indexed images provide compact image representation.
* Binary thresholding separates foreground and background effectively.
* Canny edge detection accurately extracts object boundaries.
* Each transformation progressively reduces complexity while maintaining useful information.

---

# 🌍 Applications

The concepts demonstrated in this project are widely used in:

* Computer Vision
* Object Detection
* Image Segmentation
* Medical Image Analysis
* Face Recognition
* Robotics
* Autonomous Vehicles
* Industrial Inspection
* Optical Character Recognition (OCR)
* Remote Sensing
* Pattern Recognition

---

# 🎓 Learning Outcomes

This project provided practical experience with:

* Digital Image Processing
* Signal Representation
* MATLAB Programming
* Image Transformation
* Thresholding Techniques
* Edge Detection
* Feature Extraction
* Spatial Domain Processing
* Computer Vision Fundamentals

---

# 🚀 Future Improvements

Possible enhancements include:

* Gaussian and Median Filtering
* Histogram Equalization
* Sobel and Prewitt Edge Detection
* Laplacian Edge Detection
* Image Segmentation
* Morphological Operations
* Fourier Transform Analysis
* Frequency Domain Filtering
* Feature Detection (SIFT, SURF, ORB)
* Deep Learning-Based Image Processing
* Object Detection using YOLO
* Image Classification using CNNs

---

# 📸 Screenshots

Include screenshots of:

* Original RGB Image
* Grayscale Output
* Indexed Image
* Binary Image
* Edge Detection Result
* Combined Visualization

Example folder:

```text
Results/
├── rgb.png
├── grayscale.png
├── indexed.png
├── binary.png
├── edges.png
└── comparison.png
```

---

# 👨‍💻 Contributors

* Hammad Raza
* Heba Saqib
* Mariam Shoaib

---

# 📚 References

* Gonzalez, R. C., & Woods, R. E. *Digital Image Processing*
* MATLAB Image Processing Toolbox Documentation
* J. Canny, *A Computational Approach to Edge Detection*, IEEE Transactions on Pattern Analysis and Machine Intelligence, 1986

---

# 📄 License

This project is intended for educational and academic purposes. It demonstrates the application of image processing and signal processing concepts using MATLAB.

If you found this project helpful, consider giving the repository a ⭐.
