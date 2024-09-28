# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: Prajin S
# Register Number: 212223230151
```
### Input Grayscale Image and Color Image
```python
import cv2
import numpy as np
from matplotlib import pyplot as plt
image = cv2.imread('light.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('on')
```
```python
image1 = cv2.imread('dark.jpg')
gray_image1 = cv2.cvtColor(image1, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image1, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('on')
```
### Histogram of Grayscale Image and any channel of Color Image
```python
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original)
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```python
hist_original1 = cv2.calcHist([gray_image1], [0], None, [256], [0, 256])
plt.plot(hist_original1)
plt.title('Original Histogram')
plt.xlim([0, 256])
```
### Histogram Equalization of Grayscale Image
```python
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('on')
```
```python
equalized_image1 = cv2.equalizeHist(gray_image1)
plt.imshow(equalized_image1, cmap='gray')
plt.title('Equalized Image')
plt.axis('on')
```
```python
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized)
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
```python
hist_equalized1 = cv2.calcHist([equalized_image1], [0], None, [256], [0, 256])
plt.plot(hist_equalized1)
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/19c61268-1eb7-4d21-8161-064ad68ab3c1)
![image](https://github.com/user-attachments/assets/ff49fa92-eaf8-4c37-acab-0f77a49f353d)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/cfbd3b08-fab0-41e7-9c80-02c76ae77ce1)
![image](https://github.com/user-attachments/assets/1fb1c215-0b9e-4273-ba11-612592c494cf)



### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/8338c3de-47f2-45f0-b1e5-ecbc09712dba)
![image](https://github.com/user-attachments/assets/af5a2c4e-a3f1-4096-a62d-3afe395d4a2d)
![image](https://github.com/user-attachments/assets/199fcbf9-c133-4799-acd8-1113b18f618e)
![image](https://github.com/user-attachments/assets/9408bd24-fcc1-49d5-a802-f3d48ab2eb53)





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
