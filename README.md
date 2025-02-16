# Otsu’s Thresholding for Image Segmentation  

## Description  

Otsu’s Thresholding is a method used to automatically segment an image into **foreground** and **background**. It finds an optimal threshold that separates pixel intensities based on their variance, assuming the image has two distinct pixel intensity distributions.  

This technique is widely used in **image processing** for **binarization** and **object detection**, especially in **grayscale images with a bimodal histogram**.  

## Algorithm  

1. Compute the **histogram** of the image.  
2. Calculate **global mean** and **global variance**.  
3. Iterate through each possible threshold and:  
   - Classify pixels into two classes.  
   - Compute class probabilities, means, and variances.  
   - Compute **between-class variance** and **within-class variance**.  
4. Select the threshold that maximizes between-class variance (or minimizes within-class variance).  
5. Apply the threshold to **segment the image into binary form**.  

## Features  

- **Automatic threshold selection** (no manual tuning required).  
- **Fast and efficient** for images with well-separated intensity levels.  
- **Python implementation using OpenCV & NumPy**.  
- **Post-processing using morphological operations** (e.g., opening & closing).  
- **Evaluation using accuracy, sensitivity, and specificity metrics**.  

## Installation & Setup  

### 1. Prerequisites  

Ensure you have **Python** installed with the necessary dependencies:  

```sh
pip install opencv-python numpy matplotlib seaborn
```

### 2. Usage  

1. **Load an image** (grayscale).  
2. **Compute the histogram** and determine the optimal threshold.  
3. **Apply Otsu’s thresholding** to segment the image.  
4. **Evaluate segmentation performance** using accuracy, sensitivity, and specificity.  
5. **Perform morphological operations** (dilation, erosion, opening, and closing) to enhance segmentation.  

Run the Python script:  

```sh
python otsu_thresholding.py
```

## Output  

- **Segmented Image**  
- **Accuracy Metrics (True Positives, False Positives, etc.)**  
- **Confusion Matrix Visualization**  

## Future Enhancements  

- Adaptive thresholding for complex images.  
- Deep learning-based segmentation.  
- Edge detection integration.  

## Author  

**Nandhini K**
