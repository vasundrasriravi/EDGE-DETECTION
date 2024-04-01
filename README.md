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

## program:
```
Developed by: VASUNDRA SRI R
Register number: 212222230168
```
## IMPORT PACKAGES AND LOAD IMAGES
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("daisy.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
## SOBEL X:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## SOBEL Y:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY:
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
### ORIGINAL IMAGE:
![daisy](https://github.com/vasundrasriravi/EDGE-DETECTION/assets/119393983/758807b6-4336-483e-9983-19a28bc73f5c)

### SOBEL EDGE DETECTOR
![sobel x](https://github.com/vasundrasriravi/EDGE-DETECTION/assets/119393983/4f673061-3150-4575-bbca-7f5c098e4297)

![sobel y](https://github.com/vasundrasriravi/EDGE-DETECTION/assets/119393983/6ac17fe3-426c-4860-b158-5da42be0dbb0)

![sobel xy](https://github.com/vasundrasriravi/EDGE-DETECTION/assets/119393983/a6cbc839-ca0c-411b-9e68-97c92065b163)

### LAPLACIAN EDGE DETECTOR
![laplacian](https://github.com/vasundrasriravi/EDGE-DETECTION/assets/119393983/6e5aa7c0-55e6-4d1d-bf64-e6d122b23e6e)

### CANNY EDGE DETECTOR
![canny](https://github.com/vasundrasriravi/EDGE-DETECTION/assets/119393983/d858bb76-c707-47eb-b8b6-31a3ad24486c)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
