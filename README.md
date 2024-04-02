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
Developed By: M Gautham
Register Number: 212221230027
```
```
import cv2
import matplotlib.pyplot as plt

gray_image=cv2.imread('cat.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
```
color_image=cv2.imread('leo.jpg')
hist1=cv2.calcHist([color_image],[1],None,[250],[0,250])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram of color image :Green channel")
plt.xlabel('intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
```
gray_image = cv2.imread('cat.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image:
![image](https://github.com/muppirgautham/Histogram-of-an-images/assets/94810884/d0761c8b-107b-442b-8d94-fc83804b36f9)
![image](https://github.com/muppirgautham/Histogram-of-an-images/assets/94810884/9c30a8d9-9182-4eac-876a-43e2687820f6)

### Histogram of Grayscale Image and any channel of Color Image:
### Grey scale:
![image](https://github.com/muppirgautham/Histogram-of-an-images/assets/94810884/8e68f523-d842-4cde-b189-0366e497768f)
### Color Image:
![image](https://github.com/muppirgautham/Histogram-of-an-images/assets/94810884/43f14fa7-84a6-46b1-9e9a-416f55af0654)


### Histogram Equalization of Grayscale Image:
![image](https://github.com/muppirgautham/Histogram-of-an-images/assets/94810884/2bcd5309-6c1c-4953-99a2-d33e602b566c)

### Result:
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
