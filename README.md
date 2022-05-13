# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
### Developed By:DurgaDevi P
### Register Number:212220230015

```python
# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('parrot.png')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('dog.jpg')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()





# Write the code to perform histogram equalization of the image. 
import cv2
Gray_image=cv2.imread('parrot.png',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![output](./static/img/h1.png)
![output](./static/img/h2.png)
<br>
<br>
<br>
<br>

### Histogram of Grayscale Image and any channel of Color Image
![output](./static/img/h3.png)
![output](./static/img/h4.png)
<br>
<br>
<br>
<br>

### Histogram Equalization of Grayscale Image
![output](./static/img/h5.png)
<br>
<br>
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
