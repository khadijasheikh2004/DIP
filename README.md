# Image Processing Assignments - MATLAB

This repository contains multiple assignments focused on implementing and understanding classical image processing techniques using **MATLAB**. The work includes both spatial and morphological filtering, noise handling, edge detection, region growing, and bit-plane analysis, all implemented manually without relying on high-level built-in functions wherever possible.

---

## Assignment Overview

### Assignment 1
Processes each frame of a video to demonstrate the effects of different filtering and edge detection techniques.

**Key Operations:**
- Converts each frame to grayscale.
- Applies:
  - **5×5 Averaging Filter** (manual convolution).
  - **Sobel Edge Detection** (gradient magnitude using Sobel X and Y).
  - **Laplacian Filter** (edge detection via second derivative).
  - **Salt-and-Pepper Noise Injection** between 2–4 seconds.
  - **7×7 Median Filter** for denoising.

**Outputs:** 5 processed videos: `Averaging`, `Sobel`, `Laplacian`, `Noisy`, and `MedianFiltered`.

---

### Assignment 2
Compares **standard** vs **adaptive median filters** on images with various noise densities.

**Key Features:**
- Adds salt & pepper noise at 30%, 50%, and 70% levels.
- Implements:
  - **Standard Median Filter** (fixed-size window).
  - **Adaptive Median Filter** (dynamically expanding window).
- Computes **Mean Squared Error (MSE)** for quality comparison.
- Displays and saves all output images.

---

### Assignment 3
Implements **Region Growing** to extract tumors or key regions from grayscale medical images.

**Workflow:**
- Allows user to **click a seed point** on the image.
- Performs **intensity-based region growing** using an 8-connected neighborhood.
- Highlights detected region on the original image.
- Saves both **binary mask** and **overlay image**.

**Use Case:** Tumor segmentation in brain MRI or X-ray images.

---

### Assignment 4
A two-part assignment combining **morphological processing** and **bit-plane slicing**.

#### **Part A – Morphological Boundary Extraction**
- Binarizes a grayscale X-ray image.
- Applies:
  - **Opening** (Erosion → Dilation) for denoising.
  - **Closing** (Dilation → Erosion) for crack/gap filling.
  - **External Boundary Extraction** via morphological subtraction.
- Displays and saves each processing stage.

#### **Part B – Bit-Plane Slicing and Structural Analysis**
- Extracts all **8 bit planes** from the original image using logical operations.
- Applies **custom morphological filters** to enhance structural features in each bit plane.
- Saves both raw and enhanced versions.
- Useful for analyzing **fine vs coarse image details** in binary decomposition.
 
