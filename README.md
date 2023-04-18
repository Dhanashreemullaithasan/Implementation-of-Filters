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
### Developed By   :
### Register Number:
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(image1)
plt.title('original')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image2)
plt.title('Filtered')
plt.axis('off')



```
ii) Using Weighted Averaging Filter
```Python





```
iii) Using Gaussian Filter
```Python





```

iv) Using Median Filter
```Python





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python





```
ii) Using Laplacian Operator
```Python





```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter

![ex6dip1](https://user-images.githubusercontent.com/94165415/232837167-d8862c39-66c9-42d3-ab4a-372f898f2ffd.png)

ii) Using Weighted Averaging Filter
</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
