# Histogram-of-an-images
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
# Developed By: CHAITANYA P S
# Register Number: 212222230024

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.png")
color_image = cv2.imread("color.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
import cv2
Gray_image = cv2.imread("gray.png")
Color_image = cv2.imread("color.png")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()

plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

import cv2
gray_image = cv2.imread("gray.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
<img src = "https://github.com/chaitanya18c/Histogram-of-an-images/assets/119392724/2744a181-fb41-4d85-9be1-35374dd772dd" width="300">
<img src ="https://github.com/chaitanya18c/Histogram-of-an-images/assets/119392724/65ecf62d-403d-4c64-aa4b-ce6bac6d1d84" width="300">

### Histogram of Grayscale Image and any channel of Color Image
<img src = "https://github.com/chaitanya18c/Histogram-of-an-images/assets/119392724/8b8d5d74-65ba-478b-81b3-d73600d7eecb" width="300">
<img src = "https://github.com/chaitanya18c/Histogram-of-an-images/assets/119392724/7c44f152-d5ec-49a6-8ac1-0d4052b9ee00" width="300">

### Histogram Equalization of Grayscale Image.
<img src ="https://github.com/chaitanya18c/Histogram-of-an-images/assets/119392724/9c853a1a-564a-423d-8016-dc75dd1b333a" width="300">
<img src ="https://github.com/chaitanya18c/Histogram-of-an-images/assets/119392724/d0e3d764-0671-4a16-893a-53635acdd723" width="300">

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
