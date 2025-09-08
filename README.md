# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.

## Program:
### Developed By   : JEFFY BRAILIN T
### Register Number: 212223040076
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("C:/Users/admin/Downloads/Digital images/ex_6_image.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()



```
ii) Using Weighted Averaging Filter
```

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()


```
iii) Using Gaussian Filter
```


gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()

```
iv)Using Median Filter
```


median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()


```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

<img width="822" height="287" alt="image" src="https://github.com/user-attachments/assets/bb14710b-f966-4c7c-8485-249828931047" />


ii)Using Weighted Averaging Filter

<img width="746" height="259" alt="image" src="https://github.com/user-attachments/assets/e29a7141-c8ea-419a-870d-c459d1c245e8" />

iii)Using Gaussian Filter

<img width="728" height="237" alt="image" src="https://github.com/user-attachments/assets/0f14b91b-ed77-457c-8792-5173156223ff" />


iv) Using Median Filter

<img width="833" height="279" alt="image" src="https://github.com/user-attachments/assets/04af352b-c777-4856-9536-b1e8bfdb5410" />


### 2. Sharpening Filters


i) Using Laplacian Kernal

<img width="612" height="204" alt="image" src="https://github.com/user-attachments/assets/34803021-e898-48bb-862e-dcfcbda82bb8" />


ii) Using Laplacian Operator

<img width="617" height="221" alt="image" src="https://github.com/user-attachments/assets/508fa7d4-54ab-413d-aee9-9a9838c66f50" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
