### Ex.No:09
### DATE: 
# <p align="center">Thresholding</p>

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

## Output
### Original Image
![Screenshot (136)](https://user-images.githubusercontent.com/75235334/169996777-98b4fdca-a385-4c88-94a3-535268f02e42.png)
### Global Thresholding
![Screenshot (137)](https://user-images.githubusercontent.com/75235334/169996934-deec590e-f052-45e7-a8c1-a35a0f84a029.png)
![Screenshot (138)](https://user-images.githubusercontent.com/75235334/169997164-3cc3820e-b866-430f-9733-62b977f8d150.png)
![Screenshot (139)](https://user-images.githubusercontent.com/75235334/169997319-08d03004-fcdc-4671-99b7-944e9b0701d9.png)
![Screenshot (140)](https://user-images.githubusercontent.com/75235334/169997513-b10d4be0-1e1e-48c5-8a66-f5f944e1ebbd.png)
![Screenshot (141)](https://user-images.githubusercontent.com/75235334/169997622-e25b2b9f-a7ad-4345-a703-f81990cc587d.png)
<br>
</br>
<br>
</br>
</br>
</br>
</br>

</br>
</br>
</br>

</br>
</br>

</br>
</br>

### Adaptive Thresholding
![Screenshot (143)](https://user-images.githubusercontent.com/75235334/169997865-ae9b7448-7958-4164-a0fd-35e201717d04.png)
![Screenshot (144)](https://user-images.githubusercontent.com/75235334/169998652-0cc03120-cdba-42f1-be78-d6fd1c2d735e.png)
<br>
</br>
<br>
</br>
</br>
</br>
</br>

</br>
</br>
</br>

</br>
</br>

</br>
</br>


### Optimum Global Thesholding using Otsu's Method
![Screenshot (142)](https://user-images.githubusercontent.com/75235334/169997731-b4c789cb-6688-4b77-8c08-55ab5843f383.png)



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.

