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
### ORIGINAL IMAGE
```
# NAME : POZHILAN V D
# REG NO : 212223240118



import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE
<img width="529" height="590" alt="image" src="https://github.com/user-attachments/assets/b68e9a39-b08c-4576-98a3-830cd7d3b6f5" />

### SOBEL EDGE DETECTOR
<img width="537" height="602" alt="image" src="https://github.com/user-attachments/assets/b3e85df6-478b-478d-9de1-bbf2aecae60c" />

### LAPLACIAN EDGE DETECTOR
<img width="531" height="618" alt="image" src="https://github.com/user-attachments/assets/68f4ab0c-5091-4040-b2e7-023ba95bcf39" />

### CANNY EDGE DETECTOR
<img width="546" height="611" alt="image" src="https://github.com/user-attachments/assets/f4035fac-c819-42de-a11f-ff5509946303" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
