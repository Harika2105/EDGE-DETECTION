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
```
Name : S.Harika
Reg no : 212224240155
```

## ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('puppy.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## SOBEL EDGE DETECTOR:
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## LAPLACIAN EDGE DETECTOR:
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
## CANNY EDGE DETECTOR:
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
## ORIGINAL IMAGE
<img width="808" height="653" alt="Screenshot 2025-10-07 222054" src="https://github.com/user-attachments/assets/c07fe752-1d81-4ec8-8853-a81c0bc6bf6c" />

## SOBEL EDGE DETECTOR:
<img width="820" height="650" alt="Screenshot 2025-10-07 222144" src="https://github.com/user-attachments/assets/ff0495d5-8bf1-44a1-baaf-ecaf530ba8db" />

## LAPLACIAN EDGE DETECTOR:
<img width="792" height="643" alt="Screenshot 2025-10-07 222229" src="https://github.com/user-attachments/assets/b4b31a7d-dc3f-49a2-b715-91925a6eac13" />

## CANNY EDGE DETECTOR:
<img width="825" height="644" alt="Screenshot 2025-10-07 222316" src="https://github.com/user-attachments/assets/7d817afb-90b8-4fea-b123-9d3054eb5ea1" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
