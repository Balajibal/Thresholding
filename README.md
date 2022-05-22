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
titles=["Gray Image","Threshold Image (Binary)","Threshold Image (Binary Inverse)","Threshold Image (To Zero)"
       ,"Threshold Image (To Zero-Inverse)","Threshold Image (Truncate)","Otsu","Adaptive Threshold (Mean)","Adaptive Threshold (Gaussian)"]
images=[image_gray,thresh_img1,thresh_img2,thresh_img3,thresh_img4,thresh_img5,thresh_img6,thresh_img7,thresh_img8]
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

### Original Image 

![Screenshot (174)](https://user-images.githubusercontent.com/75234946/169676930-09941170-79d1-466c-9bd7-94b0b72f67c6.png)


### Grayscale Image

![Screenshot (175)](https://user-images.githubusercontent.com/75234946/169676967-563d9a26-d054-4bd4-a24e-3fb3286adb0f.png)


### Global Thresholding

![Screenshot (176)](https://user-images.githubusercontent.com/75234946/169677005-d3698166-5d3f-4485-98a0-cbdff074bb19.png)


![Screenshot (177)](https://user-images.githubusercontent.com/75234946/169677034-a40d33d1-bb73-4b54-9174-a782a6256ac4.png)


![Screenshot (178)](https://user-images.githubusercontent.com/75234946/169677050-c573334c-d4a1-499e-b4be-b093047951e1.png)


![Screenshot (179)](https://user-images.githubusercontent.com/75234946/169677092-d4107218-ad6f-4d28-81f1-4ebac553f23e.png)


![Screenshot (180)](https://user-images.githubusercontent.com/75234946/169677114-fbe41df5-7d0b-431e-84fb-fb1cf6bf5151.png)



### Adaptive Thresholding

![Screenshot (185)](https://user-images.githubusercontent.com/75234946/169677148-f49b62ab-7557-4896-a7e5-719e88d239bf.png)


![Screenshot (182)](https://user-images.githubusercontent.com/75234946/169677186-addba1b4-428c-4185-907c-333361b53090.png)



### Optimum Global Thesholding using Otsu's Method

![Screenshot (183)](https://user-images.githubusercontent.com/75234946/169677227-76a1e947-c0a2-4df5-837f-59bd02044cf7.png)



## RESULT:
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
