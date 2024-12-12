# OPenCV_Basics_Section_Leolyn_Louwella
# Improving Handwritten Digit Recognition Using Morphological Dilation

## Introduction
Handwritten digit recognition is a fundamental problem in computer vision with applications in digitizing documents, postal mail sorting, and banking. 
However, handwritten digits often contain fragmented strokes or faded lines, reducing recognition accuracy. 
Morphological dilation is a preprocessing technique that enhances such features by filling gaps and improving stroke connectivity, which can significantly improve digit recognition performance.
## Abstract
This project explores the use of morphological dilation to enhance the clarity of handwritten digits with fragmented strokes. 
Using the MNIST dataset, we preprocess images to repair broken strokes, then evaluate the impact of this enhancement on digit recognition models. 
The project aims to demonstrate how dilation can improve recognition accuracy, particularly for challenging samples, by enhancing stroke connectivity and structure.
# Project Methods

## Step-by-Step Methodology

1. **Read the Image**:
   - The image file "012345.jpg" is loaded using cv2.imread.
   - If the image is not found or cannot be loaded, image will be None, and a message is printed.

