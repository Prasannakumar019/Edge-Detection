## EX NO:07
## DATE:12.5.22
# <p align="center">Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale.

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image.

### Step6:
Using Canny operator from cv2,detect the edges of the image.
 
## Program:

```python
 Developed By: Prasanna Kumar
 Register Number : 212220230035
# Import the packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Load the image, Convert to grayscale and remove noise
image1=cv2.imread('hhusskyy.jpg',0)
plt.imshow(image)
# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(image1,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(image1,cv2.CV_64F,0,1,ksize=5)
sobelxy= cv2.Sobel(image1,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.imshow(sobely,cmap='gray')
plt.imshow(sobelxy,cmap='gray')
# LAPLACIAN EDGE DETECTOR
dst = cv2.Laplacian(image1,cv2.CV_16S,ksize=3)
plt.imshow(dst,cmap='gray')
abs_dst = cv2.convertScaleAbs(dst)
plt.imshow(abs_dst,cmap='gray')
# CANNY EDGE DETECTOR
edges = cv2.Canny(image1,100,200)
plt.imshow(image1,cmap = 'gray')
plt.title('Original Image'), plt.xticks([]), plt.yticks([])
plt.imshow(edges,cmap = 'gray')
plt.title('Edge Image'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
![Screenshot (320)](https://user-images.githubusercontent.com/75235090/168481393-17727510-d422-46d8-8560-b8ac3584add0.png)


### LAPLACIAN EDGE DETECTOR
![Screenshot (322)](https://user-images.githubusercontent.com/75235090/168481463-fdbc4736-7fe0-4ef3-bb19-02a9330e2d18.png)

### CANNY EDGE DETECTOR
![Screenshot (324)](https://user-images.githubusercontent.com/75235090/168481640-f0d0e33c-99bd-4e00-835d-a3c559691454.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
