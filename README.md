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

2. **Convert to Grayscale**:
   - Converts the loaded image to grayscale because the Canny edge detection works on single-channel (grayscale) images.
     
3. **Canny Edge Detection**:
   - Detects edges in the grayscale image using the Canny edge detection algorithm.
   - 150 and 200 are the lower and upper threshold values for detecting edges.

4. **Dilation Process**:
   - Dilation enlarges the edges detected by the Canny algorithm. It uses a structuring element (kernel) and slides it over the image. Wherever the kernel overlaps the white edges (non-zero pixels), the pixels within the kernel area are turned white (non-zero).
     
   **a. Create Kernels**:
      - Creates square kernels (structuring elements) of sizes 1×11 \times 11×1, 3×33 \times 33×3, 5×55 \times 55×5, 7×77 \times 77×7, and 9×99 \times 99×9.
      - np.uint8 specifies the data type for the kernel.

   **b. Apply Dilation**:
      - Expands the white regions (edges) in the input image (canny_image).
      - Summarize the results and their implications for practical applications.
        
   **c. Display Results**
      - Each dilated image is displayed.
      - Larger kernels result in more significant edge expansion because the dilation operation includes more surrounding pixels in the kernel's region.

# Conclusion

## Findings
- Morphological dilation effectively enhances fragmented or faint strokes in handwritten digits.
- Models trained on the dilated dataset showed improved recognition accuracy, particularly for challenging samples.

## Challenges
- Over-dilation occasionally caused merging of distinct strokes, leading to recognition errors.
- Selecting the optimal kernel size and shape required iterative experimentation.

## Outcomes
This project demonstrates the potential of morphological dilation as a preprocessing step for handwritten digit recognition tasks. 
Future work could focus on dynamically adjusting kernel parameters based on input features or extending the method to other datasets with more complex handwriting styles.
