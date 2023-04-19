# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required packages for further process.

## Step2:
Read the image and convert the bgr image to gray scale image.

## Step3:
Use any filters for smoothing the image to reduse the noise.

## Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

## Step5:
Display the filtered image using plot and imshow.

 
## Program:
## Import the packages and load the image, Convert to grayscale and remove noise
~~~
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("bike (1).jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
~~~


# SOBEL EDGE DETECTOR
~~~
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.imshow(sobelx)
plt.title("SOBEL_X")
plt.xticks([])
plt.yticks([])
plt.show()
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.imshow(sobely)
plt.title("SOBEL_Y")
plt.xticks([])
plt.yticks([])
plt.show()
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.imshow(sobelxy)
plt.title("SOBEL_XY")
plt.xticks([])
plt.yticks([])
plt.show()
~~~


# LAPLACIAN EDGE DETECTOR
~~~
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.imshow(laplacian)
plt.title('LAPLACIAN')
plt.axis("off")
plt.show()
~~~


# CANNY EDGE DETECTOR
~~~
canny_edges = cv2.Canny(new_image, 120, 150)
plt.figure(figsize = (8,8))
plt.imshow(canny_edges)
plt.title('CANNY_EDGES')
plt.axis("off")
plt.show()
~~~

## Output:
## ORIGINAL:
![image](https://user-images.githubusercontent.com/94165322/232963229-794aca36-d7c0-42db-a05d-221a023e8a70.png)

### SOBEL EDGE DETECTOR
![image](https://user-images.githubusercontent.com/94165322/232963257-cfec7f81-345d-4f94-8f03-149cb7eba816.png)
![image](https://user-images.githubusercontent.com/94165322/232963291-f5003cab-716d-4a2e-ae6d-c60733b120b5.png)
![image](https://user-images.githubusercontent.com/94165322/232963313-21831876-329a-4229-ab8f-0efcfd6b2954.png)



### LAPLACIAN EDGE DETECTOR
![image](https://user-images.githubusercontent.com/94165322/232963333-198cff1d-6838-4993-9da5-05c39a03462c.png)

### CANNY EDGE DETECTOR
![image](https://user-images.githubusercontent.com/94165322/232963363-d10c785b-73c3-416d-9756-7c1cc25439b5.png)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
