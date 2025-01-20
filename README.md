# Optical Character Recognition (OCR) Program

## Introduction
This project is a foundational Optical Character Recognition (OCR) system capable of identifying handwritten characters, including uppercase letters, lowercase letters, and numbers. The system is built from scratch, avoiding the use of pre-existing OCR libraries, and focuses on leveraging core image processing techniques and template matching.

The primary objective is to demonstrate the principles behind OCR systems in a modular, extensible manner suitable for educational purposes or controlled practical applications.

---

## Features
- **Character Recognition**: Detects and classifies uppercase letters, lowercase letters, and numbers from an input image.
- **Template Matching**: Uses a preloaded set of templates (32x32 pixels) for comparison.
- **Graphical User Interface (GUI)**: Developed using `tkinter`, allowing users to:
  - Load images.
  - Execute OCR.
  - View results interactively.
- **Error Handling**: Verifies the existence of templates and validity of input images.
- **Extensibility**: Can support additional characters or languages by adding new templates.

---

## Technologies Used
- **Python Libraries**:
  - `cv2` (OpenCV): For image processing (reading, resizing, contour detection, and binarization).
  - `numpy`: For mathematical operations and image comparisons.
  - `os`: For file and directory management.
  - `PIL` (Python Imaging Library): For advanced image manipulation.
  - `tkinter`: To build the graphical user interface.

---

## System Workflow
1. **Preprocessing**: Input images are resized to 50x50 pixels for consistency in analysis.
2. **Text Detection**: Identifies regions of text using thresholding and contour detection.
3. **Template Loading**: Loads character templates categorized into uppercase letters, lowercase letters, and numbers from designated directories.
4. **Character Recognition**:
   - Each detected text region is resized to 32x32 pixels.
   - Compared with templates using cross-correlation to identify the best match.
5. **GUI Display**:
   - Presents recognized characters and their classification.
   - Displays the processed image with bounding boxes around detected text.

---

## Folder Structure
```
OCR_Project/
|-- main.py                  # Main script for the OCR system
|-- Templates/               # Folder containing character templates
|   |-- 1/                   # Template set 1
|   |   |-- Mayusculas/      # Uppercase letters
|   |   |-- minusculas/      # Lowercase letters
|   |   |-- numeros/         # Numbers
|   |-- 2/                   # Template set 2 (same structure as above)
|-- README.md                # Project documentation
```

---

## Usage
### Prerequisites
Ensure you have Python installed along with the following libraries:
- OpenCV (`cv2`)
- NumPy
- PIL (Python Imaging Library)
- Tkinter

4. Use the GUI to load an image and view the OCR results.

### Supported Image Formats
- `.jpg`
- `.png`
- `.jpeg`

---

## Future Enhancements
- Incorporate deep learning techniques (e.g., Convolutional Neural Networks) for improved recognition accuracy.
- Add support for additional languages and special characters.
- Optimize performance for larger datasets.

---

## Credits
Developed by **Joaquín Rodríguez Figueroa** as part of the Artificial Intelligence course project at **Universidad Europea del Atlántico**.

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
