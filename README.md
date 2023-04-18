# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1
Import libraries and read the saved images using cv2.imread().

Step2
Convert the saved BGR image to RGB using cvtColor().

Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

Step4
Apply the filters using cv2.filter2D() for each respective filters.

Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

## Program:
### Developed By   : DHANASHREE M
### Register Number: 212221230018
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("temp.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
```

### 1. Smoothing Filters

i) Using Averaging Filter

```
kernel1 = np.ones((11,11),np.float32)/121
avg_filter = cv2.filter2D(original_image,-1,kernel1)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(avg_filter)
plt.title("Filtered")
plt.axis("off")



```
ii) Using Weighted Averaging Filter
```

kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Filtered")
plt.axis("off")



```
iii) Using Gaussian Filter
```
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Filtered")
plt.axis("off")

```

iv) Using Median Filter
```
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Filtered")
plt.axis("off")

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```

kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Filtered")
plt.axis("off")



```
ii) Using Laplacian Operator
```
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")

```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter

![ex6dip1](https://user-images.githubusercontent.com/94165415/232837167-d8862c39-66c9-42d3-ab4a-372f898f2ffd.png)

ii) Using Weighted Averaging Filter

![ex6 dip2](https://user-images.githubusercontent.com/94165415/232837703-beb5c8bd-d11a-45ef-ad0d-d40b93754ce0.png)


iii) Using Gaussian Filter

![sodapdf-converted (2)](https://user-images.githubusercontent.com/94165415/232838955-854a6c10-d655-44d2-85d1-2049a40318ea.jpg)


iv) Using Median Filter
![sodapdf-converted (1)](https://user-images.githubusercontent.com/94165415/232838837-57483100-5dc1-4a98-b886-8012f28f8281.jpg)


### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![sodapdf-converted (4)](https://user-images.githubusercontent.com/94165415/232839663-2df3553b-ab05-4ada-9bea-f37f2e042bc0.jpg)


ii) Using Laplacian Operator
![sodapdf-converted (5)](https://user-images.githubusercontent.com/94165415/232839732-14a0312f-d3c5-47c9-abd2-a9af848da288.jpg)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
