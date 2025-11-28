# EDGE-DETECTION
# Name: Jayasree R
# Register No: 212223230087
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

## Output:
### SOBEL EDGE DETECTOR
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('/content/rome.jpeg')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray, (3, 3), 0)
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelx, cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobely, cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(sobelxy, cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

```
<img width="898" height="299" alt="Screenshot 2025-11-28 215901" src="https://github.com/user-attachments/assets/3a462a48-bd81-405e-8423-dab58beee0e5" />




### LAPLACIAN EDGE DETECTOR
```
    lap = cv2.Laplacian(gray, cv2.CV_64F)
    
    plt.figure(figsize=(8, 8))
    plt.subplot(1, 2, 1)
    plt.imshow(gray, cmap='gray')
    plt.title("Original Image")
    plt.axis("off")
    plt.subplot(1, 2, 2)
    plt.imshow(lap, cmap='gray')
    plt.title("Laplacian Edge Detector")
    plt.axis("off")
    plt.show()

```
<img width="869" height="305" alt="Screenshot 2025-11-28 215935" src="https://github.com/user-attachments/assets/bd743991-6028-4e5c-8e2f-90a09078b4eb" />


### CANNY EDGE DETECTOR
```
canny = cv2.Canny(gray, 120, 150)

plt.figure(figsize=(8, 8))
plt.subplot(1, 2, 1)
plt.imshow(gray, cmap='gray')
plt.title("Original Image")
plt.axis("off")
plt.subplot(1, 2, 2)
plt.imshow(canny, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()

```
<img width="865" height="305" alt="Screenshot 2025-11-28 215946" src="https://github.com/user-attachments/assets/285a740e-f5c2-45a7-94ae-375274f58856" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
