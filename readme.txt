# 🖼️ Image Processing Studio

A Python-based desktop application for performing basic **image processing, filtering, edge detection, and pixel analysis** using **CustomTkinter, OpenCV, NumPy, and Pillow**.

The application provides an interactive graphical interface where users can upload an image, view the original image, convert it to grayscale, apply different image-processing operators, view the corresponding kernels/masks, and inspect pixel values.

## ✨ Features

* 📁 Upload images
* 🖼️ Display input and processed images
* ⚫ Convert input images to grayscale
* 🟨 Apply Mean Filter
* 🟪 Apply Gaussian Filter
* 🟧 Apply Sobel Edge Detection
* 🩷 Apply Laplacian Edge Detection
* 🧮 Display the kernel/mask used for processing
* 🔢 Display image pixel values
* 📊 Display image dimensions and processing information
* 🔄 Reset the application
* 💻 User-friendly graphical interface

## 🛠️ Technologies Used

* **Python**
* **CustomTkinter** – Graphical User Interface
* **OpenCV (cv2)** – Image processing
* **NumPy** – Numerical operations and kernels
* **Pillow (PIL)** – Image conversion and display
* **Tkinter** – File selection and message boxes

## 🔧 Image Processing Operators

### 1. Mean Filter

A 3 × 3 averaging filter is used to smooth the image.

```text
[ 0.111  0.111  0.111 ]
[ 0.111  0.111  0.111 ]
[ 0.111  0.111  0.111 ]
```

The filter is implemented using a 3 × 3 kernel whose values are `1/9`.

### 2. Gaussian Filter

The application generates a 3 × 3 Gaussian kernel using OpenCV and applies Gaussian blur to the grayscale image.

### 3. Sobel Operator

The Sobel operator detects edges in both horizontal and vertical directions.

**Sobel X:**

```text
[ -1   0   1 ]
[ -2   0   2 ]
[ -1   0   1 ]
```

**Sobel Y:**

```text
[ -1  -2  -1 ]
[  0   0   0 ]
[  1   2   1 ]
```

The final output is calculated from the magnitude of the X and Y gradients.

### 4. Laplacian Operator

The Laplacian operator detects rapid changes in image intensity using the following 3 × 3 kernel:

```text
[  0   1   0 ]
[  1  -4   1 ]
[  0   1   0 ]
```

The resulting image is converted to an absolute 8-bit representation for display.

## 🖥️ Application Interface

The application contains:

* **Upload Image** button
* **Reset** button
* **Input Image** panel
* **Processed Output** panel
* **Mean Filter** button
* **Gaussian** button
* **Sobel** button
* **Laplacian** button
* **Apply Operator** button
* **Kernel / Mask** display
* **Pixel Matrix** display
* **Image Processing Information** section
* **Status bar**

These components are implemented using CustomTkinter widgets.

## 📌 How to Run

### 1. Install Python

Make sure Python 3.x is installed on your system.

### 2. Install Required Libraries

```bash
pip install customtkinter opencv-python numpy pillow
```

### 3. Run the Application

Save the Python program as:

```text
image_processing_studio.py
```

Then run:

```bash
python image_processing_studio.py
```

The application starts through:

```python
if __name__ == "__main__":
    app = ImageProcessingApp()
    app.mainloop()
```

## 🚀 How to Use

1. Launch the application.
2. Click **UPLOAD IMAGE**.
3. Select a `.jpg`, `.jpeg`, `.png`, `.bmp`, `.tif`, or `.tiff` image.
4. The original image is displayed in the **Input Image** section.
5. The image is automatically converted to grayscale.
6. Select an image-processing operator:

   * Mean Filter
   * Gaussian
   * Sobel
   * Laplacian
7. Click **APPLY OPERATOR**.
8. The processed image appears in the **Processed Output** section.
9. The corresponding kernel/mask is displayed.
10. Pixel values are shown in the **Pixel Matrix** section.
11. Click **RESET** to clear the application.

The upload function supports the listed image formats and automatically converts the uploaded image to grayscale.

## 🔢 Pixel Analysis

After an image is uploaded, the application displays its grayscale pixel values.

For large images, the application displays the **first 15 × 20 pixels** to keep the matrix readable.

## 📊 Output

For the demonstrated execution:

* **Input Image:** `Lotus.png`
* **Image Size:** `360 × 360 pixels`
* **Input:** Grayscale
* **Selected Operator:** Sobel
* **Processing:** 3 × 3 Kernel
* **Output:** Edge-detected grayscale image

The screenshot shows the original lotus image on the left and the Sobel edge-detected output on the right.

### Example Output

```text
IMAGE PROCESSING STUDIO

Input Image:
Lotus.png
360 × 360 pixels

Selected Operator:
SOBEL

Processed Output:
Sobel edge-detected image

Kernel / Mask:

SOBEL X:
[ -1   0   1 ]
[ -2   0   2 ]
[ -1   0   1 ]

SOBEL Y:
[ -1  -2  -1 ]
[  0   0   0 ]
[  1   2   1 ]

Image Processing Information:
Operator: Sobel
Output Size: 360 × 360
Input: Grayscale
Processing: 3 × 3 Kernel
```

The application updates the output image, pixel matrix, processing information, and status message after applying the selected operator.

## 🔄 Reset

The **RESET** button clears the input image, processed output, pixel matrix, kernel information, image details, and status information, returning the application to its initial state.

## 📂 Project Structure

```text
Image-Processing-Studio/
│
├── image_processing_studio.py
├── README.md
└── images/
    └── sample.png
```

## 🎯 Objective

The main objective of this project is to provide an easy-to-use graphical environment for understanding fundamental image-processing techniques such as:

* Image smoothing
* Gaussian filtering
* Edge detection
* Pixel-level analysis
* Kernel-based image processing

## 👩‍💻 Conclusion

**Image Processing Studio** demonstrates how Python and OpenCV can be combined with a graphical user interface to perform fundamental image-processing operations interactively.

It is useful for students and beginners who want to understand how filters, kernels, grayscale images, edge detection, and pixel matrices work in practical image processing.
