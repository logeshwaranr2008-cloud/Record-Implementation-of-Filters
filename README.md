## Record-Implementation-of-Filters

## Image Smoothing and Sharpening Using OpenCV:

## Aim:

To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.


## The program performs the following operations:

* Read and display an input image
* Apply Averaging filter
* Apply Weighted Averaging filter
* Apply Gaussian filter
* Apply Median filter
* Apply Laplacian sharpening using kernel
* Apply Laplacian operator
* Display all outputs for comparison

## Software Used:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## Algorithm:

## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Read the input image (e.g., image.jpg).

## Step 3:
Convert the image from BGR to RGB format for display.

## Step 4:
Apply Averaging Filter using cv2.blur().

## Step 5:
Apply Weighted Averaging Filter using a custom kernel with cv2.filter2D().

## Step 6:
Apply Gaussian Filter using cv2.GaussianBlur().

## Step 7:
Apply Median Filter using cv2.medianBlur().

## Step 8:
Apply Laplacian Sharpening using Kernel with cv2.filter2D().

## Step 9:
Convert image to grayscale and apply Laplacian Operator using cv2.Laplacian().

## Step 10:
Display all filtered images using a grid layout for comparison.

## Program:

## Developed By : LOGESHWARAN R

## Register No : 212225040205

## Smoothing Filters:

## Averaging Filter Image:

```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("sai1.jpeg")
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

## Weighted Averaging Filter Image:

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

## Gaussian Blur:

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

## Median Blur:

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

## Sharpening Filters:

## Laplacian kernel:

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

## Laplacian Operator:

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

## Output:

## Smoothing Filters:

## Original Image And Averaging Filter Image:

<img width="816" height="730" alt="image" src="https://github.com/user-attachments/assets/a66047b0-a611-412c-a876-0f8de9a6780d" />

## Original Image And Weighted Averaging Filter Image:

<img width="525" height="407" alt="image" src="https://github.com/user-attachments/assets/6bb93596-72af-4950-9210-f1d68aceb6ce" />

## Original Image And Gaussian Blur:

<img width="463" height="417" alt="image" src="https://github.com/user-attachments/assets/a3f2778c-6db9-4ea9-9938-822e03ff797c" />

## Original Image And Median Blur:

<img width="717" height="737" alt="image" src="https://github.com/user-attachments/assets/8da4fb02-4a71-4ffb-812f-59ce0ad5282f" />

## Sharpening Filters:

## Original Image And Laplacian kernel:

<img width="483" height="421" alt="image" src="https://github.com/user-attachments/assets/5372b1b2-6cb7-4057-8800-b8cca7733c56" />

## Original Image And Laplacian Operator:

<img width="472" height="428" alt="image" src="https://github.com/user-attachments/assets/a78ef8c9-6ec4-455f-afa2-2f4e8ca68e28" />

## Result:

Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.

The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.
