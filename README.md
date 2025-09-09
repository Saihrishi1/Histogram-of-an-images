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

### Developed By: SAI HRISHI M
### Register Number: 212224240140

### Input Grayscale Image and Color Image
```python
import cv2
from matplotlib import pyplot as plt
image = cv2.imread(r"C:\Users\admin\Pictures\Screenshots\Screenshots for thumbnails\CROW.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## Output:

<img width="641" height="474" alt="Screenshot 2025-09-10 020731" src="https://github.com/user-attachments/assets/3a9b468e-43ae-4deb-9168-c70635dc235a" />

### Histogram of Grayscale Image
```python
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Output:

<img width="726" height="552" alt="Screenshot 2025-09-10 020739" src="https://github.com/user-attachments/assets/04e8199e-8f31-475c-9d2d-b23a5015aa71" />

### Histogram Equalization of Grayscale Image.
```python
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
## Output:

<img width="659" height="465" alt="Screenshot 2025-09-10 020746" src="https://github.com/user-attachments/assets/7dea7309-780a-444d-8404-aeeee8317fa2" />

## Equalized Histogram
```python
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:

<img width="739" height="547" alt="Screenshot 2025-09-10 020754" src="https://github.com/user-attachments/assets/c8742971-9b32-4942-9149-2b68f011d4b0" />

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
