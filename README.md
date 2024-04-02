# EX-6 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
### Step2:
Load a image using imread() from cv2 module.
### Step3:
Convert the image to grayscale
### Step4:
Using Sobel operator from cv2,detect the edges of the image.
### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY: DEVADARSHAN A S
REGISTER NUMBER: 212222110007
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("mase.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![Screenshot 2024-04-02 114731](https://github.com/DEVADARSHAN2/EDGE-DETECTION/assets/119432150/66d2b9c3-ecf2-4bce-8030-18f0eeb57687)
### SOBEL EDGE DETECTOR:
![Screenshot 2024-04-02 113222](https://github.com/DEVADARSHAN2/EDGE-DETECTION/assets/119432150/c22a78c6-ab0c-4f31-bf6f-ec75e7d80ecf)
![Screenshot 2024-04-02 113227](https://github.com/DEVADARSHAN2/EDGE-DETECTION/assets/119432150/d1a8a9d3-66f1-4abd-a6fb-dd6c63b2d246)
![Screenshot 2024-04-02 113233](https://github.com/DEVADARSHAN2/EDGE-DETECTION/assets/119432150/8253d061-43e3-4348-992b-a4203453a6ad)
### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-02 113238](https://github.com/DEVADARSHAN2/EDGE-DETECTION/assets/119432150/2d125678-7b3f-4156-89e5-0eed7a82dece)
### CANNY EDGE DETECTOR
![Screenshot 2024-04-02 113249](https://github.com/DEVADARSHAN2/EDGE-DETECTION/assets/119432150/7500715b-e4e9-40cf-85a7-1a44146db5a4)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
