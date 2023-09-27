# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules


### Step2:
```

For performing edge detection on a image.

Sobel
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```
```
Laplacian
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
Canny
canny=cv2.Canny(img,120,150)
```
### Step3:
Display all the images with their respective edge detected images.


 
## Program:
```
DEVELOPED BY : MOHAMED FAREED F
REG.NO: 212222230082
```
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread ('CAR IMAGE.PNG') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)

plt.title('GRAY IMAGE')
plt.imshow(gray_image,cmap = 'gray')

img = cv2.GaussianBlur(gray_image,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray_image,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])

plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()
# cv2.waitKey(0)
laplacian = cv2.Laplacian(gray_image,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()

canny_edges = cv2.Canny(gray_image, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()



```
## Output:
### SOBEL EDGE DETECTOR
![image](https://github.com/MOHAMED-FAREED-22001617/EDGEDETECTION/assets/121412904/b64392e2-3b3e-4142-ac02-678b9ac33e83)
![image](https://github.com/MOHAMED-FAREED-22001617/EDGEDETECTION/assets/121412904/48e1e325-fcb4-46b5-8a12-76d369a3a239)
![image](https://github.com/MOHAMED-FAREED-22001617/EDGEDETECTION/assets/121412904/587d12f7-35ff-42fc-a845-3d2b338cd9e4)
![image](https://github.com/MOHAMED-FAREED-22001617/EDGEDETECTION/assets/121412904/f0276e86-24af-4d97-adc7-f6005fd7674a)



### LAPLACIAN EDGE DETECTOR

![image](https://github.com/MOHAMED-FAREED-22001617/EDGEDETECTION/assets/121412904/741f0ffc-4895-4de8-92ac-cbd059a5b069)


### CANNY EDGE DETECTOR
![image](https://github.com/MOHAMED-FAREED-22001617/EDGEDETECTION/assets/121412904/e17c4e8a-0515-4b11-89f9-671b99f327f5)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
