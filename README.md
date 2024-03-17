# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Read the gray and color image using imread()

## Step2:
Print the image using imshow().

## Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

## Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```py
'''
# Developed By: K KESAVA SAI
# Register Number: 212223230105
'''
```
## Gray Image and Color Image
```py
import cv2
gray_img = cv2.imread('graycat.jpg')
gray_img = cv2.resize(gray_img,(300,200))
color_img = cv2.imread('house.jpg')
color_img = cv2.resize(color_img,(300,200))
cv2.imshow("Gray Image",gray_img)
cv2.imshow("Colour Image",color_img)
cv2.waitKey(0)
```
## Histogram of Grayscale Image
```py
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('graycat.jpg')
color_img = cv2.imread('house.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(gray_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
## Histogram of Color Image
```py
import cv2
import matplotlib.pyplot as plt
gray_img = cv2.imread('graycat.jpeg')
color_img = cv2.imread('house.jpg')
hist = cv2.calcHist([gray_img],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_img],[1],None,[256],[0,256])
plt.figure()
plt.imshow(color_img)
plt.show()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
## Histogram Equilization of GrayScale Image
```py
import cv2
gray_img = cv2.imread('graycat.jpg',0)
gray_img = cv2.resize(gray_img,(300,200))
cv2.imshow('Grey Scale Image',gray_img)
equ = cv2.equalizeHist(gray_img)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
```

## Output:
## Input Grayscale Image and Color Image
![image](https://github.com/Kesavasai20/Histogram-of-an-images/assets/138849303/57d403fd-d77a-4c90-9b1c-ef0e26c8f1fc)

## Histogram of Grayscale Image
![image](https://github.com/Kesavasai20/Histogram-of-an-images/assets/138849303/c5b4741e-dd8c-486d-a80c-8d2cd9af97b1)

## Histogram of Color Image
![image](https://github.com/Kesavasai20/Histogram-of-an-images/assets/138849303/0090aebd-e3cc-4310-be89-685732421c34)

## Histogram Equalization of Grayscale Image
![image](https://github.com/Kesavasai20/Histogram-of-an-images/assets/138849303/1a38ca90-e6d9-4b39-a93b-04006251e12b)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
