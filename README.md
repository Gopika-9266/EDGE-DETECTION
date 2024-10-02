# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load a image using imread() from cv2 module.

### Step 3:
Convert the image to grayscale

### Step 4:
Using Sobel operator from cv2,detect the edges of the image.

### Step 5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
Developed By: Gopika R
Register No: 212222240031
```
```
# Import necessary packages
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("eiffel.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDE DETECTOR
```
(1) SOBEL X:

sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

(2) SOBEL Y:

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

(3) SOBEL XY:

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:

### ORIGINAL IMAGE
![eiffel](https://github.com/user-attachments/assets/f6e14021-af84-4bd4-812e-877c0e6059fc)


### SOBEL EDGE DETECTOR
![Screenshot 2024-10-02 094355](https://github.com/user-attachments/assets/3cc34b75-1ec1-41ed-a004-cb77c8eddcbd)

![Screenshot 2024-10-02 094405](https://github.com/user-attachments/assets/2a59060a-8e8a-4dc1-9fcf-39f04000af8b)

![Screenshot 2024-10-02 094415](https://github.com/user-attachments/assets/91f32947-a224-4d74-b537-4ac4a26420f7)


### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-10-02 094424](https://github.com/user-attachments/assets/aa625e17-d714-4145-b597-eafabaf5335f)


### CANNY EDGE DETECTOR

![Screenshot 2024-10-02 094442](https://github.com/user-attachments/assets/171289fc-d4c4-4740-83eb-8f0c2356d852)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
