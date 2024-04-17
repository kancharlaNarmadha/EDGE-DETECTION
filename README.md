# EDGE-DETECTION
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
## Program:
### IMPORT PACKAGES AND LOAD IMAGES
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("Dhoni.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
SOBEL X:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
SOBEL Y:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
SOBEL XY:
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![image](https://github.com/kancharlaNarmadha/EDGE-DETECTION/assets/119559316/1cfc3bb3-fc7a-40c3-824b-042cd6e05708)

### SOBEL EDGE DETECTOR


![Untitled](https://github.com/kancharlaNarmadha/EDGE-DETECTION/assets/119559316/4a76ee1c-4915-4b02-9e18-a9f3983e97c3)

![Untitled](https://github.com/kancharlaNarmadha/EDGE-DETECTION/assets/119559316/fb9a7382-e92d-4106-89b1-1560a1fb5e5c)

![Untitled](https://github.com/kancharlaNarmadha/EDGE-DETECTION/assets/119559316/63829d63-ecfb-468a-9853-5ea73befcd43)


### LAPLACIAN EDGE DETECTOR

![Untitled](https://github.com/kancharlaNarmadha/EDGE-DETECTION/assets/119559316/57034665-b752-45b0-9267-e88f2f647a07)


### CANNY EDGE DETECTOR
![Untitled](https://github.com/kancharlaNarmadha/EDGE-DETECTION/assets/119559316/547abc0e-5d3c-4ad5-9490-ea1ca82a12e5)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
