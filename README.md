# Computer Vision Final Project

This repository contains the practical final assignments for the **Computer Vision (Visió per Computador)** course. The projects are developed in **MATLAB** and focus on image processing, feature extraction, and pattern recognition techniques.

## 👥 Authors
* **Joan Bernaus**
* **Joan Bennassar**

---

## 💾 Dataset Download (Required)
Due to GitHub's file size limits, the image datasets required to run the scripts are hosted externally.

**⚠️ Action Required:**
1. **[Download the Dataset here (Google Drive)](https://drive.google.com/drive/folders/1bZjK2QjClOOCr9aJgGgtbFUHfaU2UgwF?usp=sharing)**
2. Unzip/Place the folders inside the root directory of this repository.
3. Ensure you have the following directory structure:
    * `./plants/` (For PF-1)
    * `./referencia/` (For PF-2)
    * `./text/` (For PF-2)

---

## 📂 Repository Structure

The repository contains the source code (Live Scripts) and their exported PDF versions for easy viewing.

| File | Type | Description |
| :--- | :--- | :--- |
| `PF-1.mlx` | MATLAB Script | **Project 1:** Source code for Plant Recognition. |
| `PF-2.1.mlx` | MATLAB Script | **Project 2 (Part 1):** Training/Template generation for OCR. |
| `PF-2.2.mlx` | MATLAB Script | **Project 2 (Part 2):** Text Recognition and testing. |
| `*.pdf` | Document | Exported versions of the scripts showing code + output results. |
| `enunciat.pdf` | Documentation | Original assignment instructions/problem statement. |

---

## 🌱 Project 1: Plant Classification (PF-1)
**Goal:** Develop a system to identify plant species based on the morphological features of their leaves.

### Methodology
1.  **Preprocessing:** Conversion to grayscale and noise reduction.
2.  **Segmentation:** Binarization using **Otsu's method** to separate the leaf from the background.
3.  **Feature Extraction:** Calculation of geometric descriptors such as:
    * Area & Perimeter
    * Compactness (Roundness)
    * Euler Number
    * Solidity / Extent
4.  **Classification:** Comparison of the extracted feature vector against a database of known species using **Euclidean distance**.

---

## 🔤 Project 2: Optical Character Recognition (PF-2)
**Goal:** Implement an OCR system capable of reading text from images using correlation-based template matching.

### Part 2.1: Knowledge Base Creation (`PF-2.1`)
* **Input:** Images from the `referencia/` folder containing samples of letters and numbers.
* **Process:** Segments each character and stores it as a binary template (or feature vector) to build the system's "alphabet" database.

### Part 2.2: Text Recognition (`PF-2.2`)
* **Input:** Images from the `text/` folder.
* **Process:**
    1.  **Segmentation:** Detects lines of text and isolates individual characters.
    2.  **Correlation:** Compares each segmented character against the templates generated in Part 2.1.
    3.  **Transcription:** Outputs the recognized text string based on the highest correlation score.

---

## ⚙️ Usage Instructions

1.  **Clone the repository**:
    ```bash
    git clone [https://github.com/your-username/computer-vision-projects.git](https://github.com/your-username/computer-vision-projects.git)
    ```
2.  **Download the images** from the Google Drive link above and place them in the project folder.
3.  **Open MATLAB** and navigate to the project directory.
4.  Open the desired **`.mlx`** file (e.g., `PF-1.mlx`).
5.  Click **"Run All"** in the Live Editor tab to execute the full pipeline.

## 🛠️ Requirements
* **MATLAB** (R2021b or later recommended)
* **Image Processing Toolbox**
* **Computer Vision Toolbox**
