# Histogram and Histogram Equalization of an image
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

### Step4:
cv2.equalize() is used to transform the gray image to equalized form.

### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
python
# Developed By:M.Pavan kishore
# Register Number:212221230076
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt

gray=cv2.imread("eren.jpg",0)
gray= cv2.resize(gray, (904,507))
cv2.imshow('gray image',gray)

color=cv2.imread("aot.jpg",1)
color= cv2.resize(color, (727,403))
cv2.imshow('color image',color)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

# Display the histogram of gray scale image and any one channel histogram from color image
```
gray_hist=cv2.calcHist([gray],[0],None,[256],[0,255])
color_hist=cv2.calcHist([color],[2],None,[256],[0,255])

plt.figure()
plt.title("gray image")
plt.xlabel("grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

plt.figure()
plt.title("color image")
plt.xlabel("colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

```




# Write the code to perform histogram equalization of the image. 
```
gray_equalized=cv2.equalizeHist(gray)
cv2.imshow('gray image',gray)
cv2.imshow('equalized gray image',gray_equalized)
cv2.waitKey(0)
cv2.destroyAllWindows()
```






## Output:
### Input Grayscale Image and Color Image
![Screenshot (2)](https://user-images.githubusercontent.com/94154941/231713306-0dfcb187-94e3-4348-86c8-b0bfeb65f255.png)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot (1)](https://user-images.githubusercontent.com/94154941/231713329-7a6abefa-4c9d-43a7-a667-bf161ca1ab8f.png)


### Histogram Equalization of Grayscale Image
![Screenshot (3)](https://user-images.githubusercontent.com/94154941/231713364-a20bce2e-54fa-42c7-8438-787b3dcc6185.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
