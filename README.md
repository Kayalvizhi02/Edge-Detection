### EX NO: 07
### DATE:
# <p align="center">Edge Detection</p>
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale.

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:
Using Laplacian operator from cv2,detect the edges of the image.

### Step6:
Using Canny operator from cv2,detect the edges of the image.
 
## Program:
```
Developed By : KAYALVIZHI M
Register Number :212220230024
```
``` Python
# Import the packages

import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise

image=cv2.imread("pikachu.jpg")
image1=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("IMAGE",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

img=cv2.GaussianBlur(image1,(3,3),0)
plt.figure(1)
plt.imshow(img,cmap='gray')
plt.title('Original')
plt.xticks([])
plt.yticks([])

# SOBEL EDGE DETECTOR

sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.imshow(sobelx,cmap='gray')
plt.title('Sobel x')
plt.xticks([])
plt.yticks([])
plt.imshow(sobely,cmap='gray')
plt.title('Sobel y')
plt.xticks([])
plt.yticks([])
plt.imshow(sobelxy,cmap='gray')
plt.title('Sobel xy')
plt.xticks([])
plt.yticks([])

# LAPLACIAN EDGE DETECTOR

laplacian=cv2.Laplacian(img,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])

# CANNY EDGE DETECTOR

canny_edges=cv2.Canny(img,120,150)
plt.imshow(canny_edges,cmap='gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
```
## Output:
### SOBEL EDGE DETECTOR

<img width="177" alt="image" src="https://user-images.githubusercontent.com/75413726/168777309-978e7e01-2232-42d0-9581-e4a4d23f05a4.png">

<img width="175" alt="image" src="https://user-images.githubusercontent.com/75413726/168777383-d6cfcd47-8c9b-43a4-a6c1-b795e1e9800e.png">

<img width="181" alt="image" src="https://user-images.githubusercontent.com/75413726/168777485-77c6a645-eb91-4c7b-9e00-b8ba9b380412.png">

### LAPLACIAN EDGE DETECTOR

<img width="176" alt="image" src="https://user-images.githubusercontent.com/75413726/168777556-0a7d3f30-f2bd-49eb-92f1-087cfb91232a.png">

### CANNY EDGE DETECTOR

<img width="185" alt="image" src="https://user-images.githubusercontent.com/75413726/168777666-96391f0d-87d9-44a0-9cab-b4989ed2a76d.png">


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
