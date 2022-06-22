# Thresholding
## AIM:
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV

## ALGORITHM:

### Step 1:
Load the necessary packages.

### Step 2:
Read the Image and convert to grayscale.

### Step 3:
Use Global thresholding to segment the image.

### Step 4:
Use Adaptive thresholding to segment the image.

### Step 5:
Use Otsu's method to segment the image.

### Step 6:
Display the results.

</br>
</br>
</br>

## PROGRAM:
```python
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale
image=cv2.imread("porsche.jpg",1)
image=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray=cv2.imread("porsche.jpg",0)

# Use Global thresholding to segment the image
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)

# Use Adaptive thresholding to segment the image
thresh_img7=cv2.adaptive Threshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptive Threshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)

# Use Otsu's method to segment the image 
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)

# Display the results
titles=["Gray Image","Threshold Image (Binary)","Threshold Image (Binary Inverse)",
"Threshold Image (To Zero)"
       ,"Threshold Image (To Zero-Inverse)","Threshold Image (Truncate)","Otsu",
       "Adaptive Threshold (Mean)","Adaptive Threshold (Gaussian)"]
images=[image_gray,thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,
thresh_img6,thresh_img7,thresh_img8]
for i in range(0,9):
    plt.figure(figsize=(10,10))
    plt.subplot(1,2,1)
    plt.title("Original Image")
    plt.imshow(image)
    plt.axis("off")
    plt.subplot(1,2,2)
    plt.title(titles[i])
    plt.imshow(cv2.cvtColor(images[i],cv2.COLOR_BGR2RGB))
    plt.axis("off")
    plt.show()
```

</br>
</br>
</br>

## OUTPUT:

### Original Image and Grayscale Image

![Screenshot_653](https://user-images.githubusercontent.com/75235455/169496333-8e2526b8-8206-4f49-99a4-f7bb85939d93.png)

### Global Thresholding

![Screenshot_654](https://user-images.githubusercontent.com/75235455/169496436-acbb39f1-5722-4f41-929c-0eeca3d5bf8b.png)

![Screenshot_655](https://user-images.githubusercontent.com/75235455/169496452-4b1d7ed7-3f3f-443c-8eaa-e03ecb303dce.png)

![Screenshot_656](https://user-images.githubusercontent.com/75235455/169496473-3820f17d-4be5-4b11-a1b6-e714618db679.png)

![Screenshot_657](https://user-images.githubusercontent.com/75235455/169496487-1d0e4b5a-276f-4e0e-815e-5e1903b308a4.png)

![Screenshot_658](https://user-images.githubusercontent.com/75235455/169496503-ec96bf3f-27d3-4e58-8e1a-63f513dd34a3.png)


### Adaptive Thresholding

![Screenshot_659](https://user-images.githubusercontent.com/75235455/169496599-eb698ae2-eb45-4164-b7db-f06dfdc7fb27.png)

![Screenshot_660](https://user-images.githubusercontent.com/75235455/169496625-e0d707a5-edeb-4956-b585-cb598cd3ac11.png)


### Optimum Global Thesholding using Otsu's Method

![Screenshot_661](https://user-images.githubusercontent.com/75235455/169496683-58d6f8ca-3f4d-4931-8075-d49b3bf0585b.png)


## RESULT:
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
