# Handwritten Character Recognition (HCR) System

This repository contains the code and documentation for a **Handwritten Character Recognition (HCR) System**, developed to convert scanned images of handwritten English text into machine-readable digital text. The project is implemented using a combination of image processing and deep learning techniques, with a Convolutional Neural Network (CNN) model as the core of the recognition system.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Architecture](#architecture)
- [Algorithms](#algorithms)
- [Datasets and Tools](#datasets-and-tools)
- [Installation](#installation)
- [Usage](#usage)
- [Testing and Results](#testing-and-results)
- [Limitations and Future Enhancements](#limitations-and-future-enhancements)
- [Contributors](#contributors)
- [License](#license)

## Introduction
Handwritten Character Recognition (HCR) is a system for converting images of handwritten English text into digital text. It processes scanned documents by segmenting them into lines, words, and characters before feeding each character into a CNN model to predict the text. The project supports simple English handwriting, providing an accessible tool for digitizing handwritten notes and documents.

## Features
- **Segmentation**: Efficiently segments lines, words, and individual characters from a scanned document.
- **Recognition**: Employs a CNN model to recognize characters in segmented images with high accuracy.
- **User Interface**: Allows users to upload scanned handwritten documents and receive digital text output.
- **Applications**: Useful for educational purposes, digitizing archives, and making handwritten content searchable.

## Architecture
The system architecture includes several stages:
1. **Preprocessing**: Converts scanned images to grayscale and binarizes them for better segmentation.
2. **Segmentation**:
   - Line Segmentation
   - Word Segmentation
   - Character Segmentation
3. **Recognition**: Uses a Convolutional Neural Network (CNN) model to predict each segmented character.
4. **Post-Processing**: Assembles recognized characters back into words and lines to reconstruct the document text.

## Algorithms
- **Segmentation Techniques**:
  - *Line Segmentation*: Projection Profile Method.
  - *Word and Character Segmentation*: Scale-space technique based on the method by R. Manmatha and N. Srimal.
- **Deep Learning Model**: Convolutional Neural Network (CNN)
  - Input Layer: Accepts 28x28 grayscale images of characters.
  - Convolutional, Pooling, and Fully-Connected Layers: Extract features and classify characters with ReLU and Softmax activation functions.
  - Achieved **87% accuracy** on the EMNIST dataset.

## Datasets and Tools
### Dataset
- **EMNIST By-Class Dataset**: Contains 814,255 samples across 62 classes, including both upper and lowercase English letters and digits.

### Tools and Technologies
- **Programming Language**: Python
- **Libraries**: OpenCV, Keras, TensorFlow
- **Development Environments**: Google Colab, Jupyter Notebook, Visual Studio Code
- **Frameworks**: Django for the Graphical User Interface

## Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/username/HCR-System.git
    cd HCR-System
    ```
2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the Django server to start the web interface:
    ```bash
    python manage.py runserver
    ```

## Usage
1. Upload a scanned image of handwritten English text via the user interface.
2. The system processes the image and displays the predicted digital text on the screen alongside the uploaded image.

## Testing and Results
- **Accuracy**: The CNN model achieved 87% accuracy on the EMNIST dataset during training and testing.
- **Example Results**:
    - **Sample Document 1**: 89% accuracy for character recognition.
    - **Sample Document 2**: 96% accuracy for character recognition.

## Limitations and Future Enhancements
### Current Limitations
- Scanned documents should be clear and minimally noisy for accurate results.
- Works best with simple English handwriting; cursive or overly stylized writing may lead to inaccuracies.
- Some similar-looking characters (e.g., "I" and "1") may be misclassified due to their shape similarity.

### Future Enhancements
- **Support for Cursive Handwriting**: Train a model on a dataset containing various cursive styles.
- **Custom Dataset**: Enhance accuracy by training on a more diverse dataset representing various handwriting styles.
- **Context-Based Prediction**: Improve recognition accuracy by incorporating context to distinguish similar characters based on surrounding text.

## Contributors
- Aditya Thakkar
- Sagar Thakkar
- Sagar Vala

Developed under the guidance of Prof. Ashish K. Gor at Dharmsinh Desai University.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
