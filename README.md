# Edge-Linking-using-Hough-Transformm
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.


## Program:
## Developed by: Yamuna M
## Register no: 212223230248
## Read image and convert it to grayscale image:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("books img.png",0)
img_c=cv2.imread("books img.png",1)
img_c=cv2.cvtColor(img_c,cv2.COLOR_BGR2RGB)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.figure(figsize=(13,13))
plt.subplot(1,2,1)
plt.imshow(img_c)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gray)
plt.title("Gray Image")
plt.axis("off")
plt.show()
```
![322913694-fdcd9b9c-0740-4fda-b2be-c14c6bf81b0d](https://github.com/user-attachments/assets/38f7bbfd-411c-4cb9-ae83-27cd3f7f7a65)
### Canny Edge detector output
```
canny=cv2.Canny(gray,70,90)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
![322914022-953071e5-1bd4-4fae-b7b3-b40d15d31889](https://github.com/user-attachments/assets/e33ad797-ffc6-4dbe-8d24-7f0cebe058ac)
## Draw lines on the image:
```
for line in lines:
    x1,y1,x2,y2=line[0]
    cv2.line(img_c,(x1,y1),(x2,y2),(0,0,255),3)
```
```
plt.imshow(img_c)
plt.title("Result Image")
plt.axis("off")
plt.show()
```

![322914176-90cd6a3c-886a-4a5f-a4d7-d0a6ccf6bf23](https://github.com/user-attachments/assets/d3381622-1384-455e-9b0d-0b9b48a2f78a)

## Result:
Thus, the program is written with python and OpenCV to detect lines using Hough transform.
