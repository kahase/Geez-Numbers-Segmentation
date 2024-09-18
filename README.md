# Geez Numbers Segmentation Using Projection Profile and Morphological Operations
This project implements a simple approach to segment Geez number images into individual lines and characters using  Projection Profile Algorithm and Morphological Operations in OpenCV.

# Overview
Geez numbers have unique structures, with untouching horizontal and vertical components. This makes segmentation challenging with simple thresholding. To overcome this, we apply morphological operations like closing and dilation to connect the disconnected parts of the numbers.

The program performs the following steps:

1. Preprocess the image (grayscale, inversion, thresholding).
2. Apply morphological closing and dilation to improve symbol connectivity.
3. Segment the image into individual lines.
4. Segment each line into individual characters.
5. Save the segmented characters and lines into separate files."# Geez-Numbers-Segmentation"
# Code Details
## 1. Preprocessing
    Grayscale: Converts the image to grayscale.
    Invert: Inverts the colors to match the binary format for segmentation.
    Thresholding: Applies Otsu's threshold to binarize the image.
## 2. Morphological Operations:
      Closing: Fills small gaps in the symbols.
      Dilation: Connects small components like horizontal and vertical strokes of Geez numbers.
# 3. Segmentation
    ## Line Segmentation:
        Detects and extracts individual lines from the image by scanning for non-empty rows.
    ##Character Segmentation: 
        Detects and extracts individual characters from each line by scanning for non-empty columns.
