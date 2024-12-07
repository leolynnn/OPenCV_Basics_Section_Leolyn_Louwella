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

1. **Dataset Selection**:
   - Use the MNIST dataset for handwritten digit images.
   - Divide data into training and testing sets.

2. **Preprocessing**:
   - Convert digit images to binary format using thresholding.
   - Apply morphological dilation with varying kernel sizes and shapes to repair fragmented strokes.

3. **Model Development**:
   - Train a simple Convolutional Neural Network (CNN) on the original MNIST dataset as a baseline.
   - Train the same model on the preprocessed dataset with dilated digits.

4. **Evaluation**:
   - Compare recognition accuracy between the baseline and the dilated dataset models.
   - Analyze the performance improvement on challenging samples with faint or broken strokes.

5. **Visualization**:
   - Display examples of original and dilated images.
   - Show performance metrics (accuracy, precision, recall) for both models.

6. **Documentation**:
   - Record challenges faced during preprocessing.
   - Summarize the results and their implications for practical applications.
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
