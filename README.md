# Edge-Detection
## AIM:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary modules.

### Step 2:
For performing edge detection on a image. 
- Sobel 
```python
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)
```
- Laplacian
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
```
- Canny
```python
canny=cv2.Canny(gray,120,150)
```

### Step 3:
Display all the images with their respective edge detected images.

## PROGRAM:
```
/*
Developed by: U.Bhavya
Registration Number : 212220230055
*/
```

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("kgf.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

# SOBEL EDGE DETECTOR
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# LAPLACIAN EDGE DETECTOR
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# CANNY EDGE DETECTOR
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
## OUTPUT:
### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/75235293/168720055-454d0e47-a92c-4b82-ab50-4cdef2563bd9.png)

![image](https://user-images.githubusercontent.com/75235293/168720133-1a50d048-fdcb-461c-93df-41a022e216ed.png)

![image](https://user-images.githubusercontent.com/75235293/168720170-614618d2-1e58-4d64-a694-955a5baf86f9.png)



### LAPLACIAN EDGE DETECTOR

![image](https://user-images.githubusercontent.com/75235293/168720237-b6ce2fb2-88fd-4134-a40b-e8b407727b10.png)



### CANNY EDGE DETECTOR

![image](https://user-images.githubusercontent.com/75235293/168720273-6ca7bb29-0fd8-4f6a-a08c-5944ab4ffff7.png)



## RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
