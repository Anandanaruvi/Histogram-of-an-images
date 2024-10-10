# Histogram-of-an-images.
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: A.ARUVI.
# Register Number: 212222230014.

import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('butterfly.jpg')

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [255], [0, 255])
# Plot histogram of the original grayscale image
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

# Plot histogram of the equalized image
hist_equalized = cv2.calcHist([equalized_image], [0], None, [255], [0, 255])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 255])




```
## Output:
### Input Grayscale Image and Color Image.
![PHO 1 EX 3](https://github.com/user-attachments/assets/296cba44-d0c7-4982-b886-f37bcc242944)


### Histogram of Grayscale Image and any channel of Color Image
![PHO 2 EX 3 ](https://github.com/user-attachments/assets/9c31ff56-1e29-4fd1-93d4-8330b466599a)



### Histogram Equalization of Grayscale Image.

![PHO 3 EX 3](https://github.com/user-attachments/assets/8257115e-96b0-4caa-8653-bbfd7b963b01)

### Histogram of the equalized image.

![PHO 4 EX 3](https://github.com/user-attachments/assets/b834c6e1-fda2-4c16-8141-d6578421b079)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
