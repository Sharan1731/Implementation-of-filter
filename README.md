### Exp-5- Record-Implementation of Filters
### NAME : SHARAN G
### REG NO : 212223230203
# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Using Averaging Filter
</br> 

### Step2
</br>
Using Weighted Averaging Filter
</br> 

### Step3
</br>
Using Gaussian Filter
</br> 

### Step4
</br>
Using Median Filter
</br> 

### Step5
</br>
Using Laplacian Kernal
</br>

### Step6
</br>
Using Laplacian Operator
</br> 

## Program:
### Developed By   :  Nirmal  N
### Register Number: 212223240107
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.png")
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
</br>

i) Using Averaging Filter
</br>
</br>
<img width="717" height="465" alt="download" src="https://github.com/user-attachments/assets/42b75214-2d8c-4eb5-ba54-0c94621c4779" />

</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
<img width="717" height="465" alt="download" src="https://github.com/user-attachments/assets/8bd4fbb5-b52a-4bf3-9ede-6c5dcf4fdffb" />


</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
<img width="531" height="342" alt="download" src="https://github.com/user-attachments/assets/42dab9cc-3df8-4387-90b2-f2e98d4f8bf3" />


</br>
</br>

iv) Using Median Filter
</br>
</br>
<img width="515" height="342" alt="download" src="https://github.com/user-attachments/assets/dc406a15-bead-4c08-bb9e-07f6572a8a40" />

</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
<img width="515" height="342" alt="download" src="https://github.com/user-attachments/assets/898426e1-ac4c-42a5-9b74-b9342dc47baa" />

</br>
</br>

ii) Using Laplacian Operator
</br>
</br>

<img width="515" height="342" alt="download" src="https://github.com/user-attachments/assets/3eb42cf7-2181-4d80-8253-dc16eddc4d5d" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
