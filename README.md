# -EX-6-Record-EDGE-DETECTION
# Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1: Import all the necessary modules for the program.

Step2: Load a image using imread() from cv2 module.

Step3: Convert the image to grayscale

Step4: Using Sobel operator from cv2,detect the edges of the image.

Step5: Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM :

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

```

# OUTPUT :


## ORIGINAL IMAGE :
<img width="643" height="465" alt="image" src="https://github.com/user-attachments/assets/ba593cbc-3cd3-4c5f-99b4-4ea273fd0c9d" />

## SOBEL EDGE DETECTOR:
<img width="833" height="484" alt="image" src="https://github.com/user-attachments/assets/9b5570c1-82de-4209-939c-443851981c20" />

## LAPLACIAN EDGE DETECTOR:


<img width="759" height="488" alt="image" src="https://github.com/user-attachments/assets/32dbe677-99d0-4581-9164-5a98b258452e" />

## CANNY EDGE DETECTOR:
<img width="727" height="485" alt="image" src="https://github.com/user-attachments/assets/aa2bd61b-43cc-4d6e-b325-3f41e2e05bf5" />


# RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

