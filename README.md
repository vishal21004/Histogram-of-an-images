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
```python
# Developed By: VISHAL M.A
# Register Number: 212222230177






```
## Output:
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("i1")
color_image = cv2.imread("i3",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("i1")
Color_image = cv2.imread("i3")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```


### Histogram Equalization of Grayscale Image.
```
import cv2
gray_image = cv2.imread("i1",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Input Grayscale Image and Color Image
![vj out 1](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/d42252d4-ff3a-4dce-842f-e330802bbd26)


![out 1 dipt](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/2ac2d6bb-d115-4ed8-b8b1-1259e1cd4073)


### Histogram of Grayscale Image and any channel of Color Image

![bluue dala](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/68f9be3b-c2e6-4bd4-902b-5c3e122cdc42)

![out dala](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/28a74ae6-829d-4027-a2ef-664a08ca789f)

![vj blue](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/90d501f1-3618-4768-b3ba-758d056a9d63)

![vj out](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/4a744870-0802-45a8-8608-a73f73c2712c)




### Histogram Equalization of Grayscale Image.


![asith out](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/7446905c-e48e-42d6-bd86-ec2d13428eb0)

![asith out 2](https://github.com/vishal21004/Histogram-of-an-images/assets/119560110/f1295b3b-49ca-4f0a-a973-dde955559155)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
