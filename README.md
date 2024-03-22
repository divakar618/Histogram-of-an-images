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
# Developed By: Divakar R
# Register Number: 212222240026


import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('grayscale.jpeg')
color_image = cv2.imread('color.jpeg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpeg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![313135759-cf331f99-77d8-464c-b26b-6cd679a939e7](https://github.com/divakar618/Histogram-of-an-images/assets/121932143/ba69f808-bdba-4f5b-9c44-875266b5ede7)

### COLOR IMAGE:
![313136113-01876521-e212-4b0e-9831-ca1f7269490a](https://github.com/divakar618/Histogram-of-an-images/assets/121932143/707a9270-10d9-4aa5-aa95-92e212e1e949)



### Histogram of Grayscale Image and any channel of Color Image
### GREY SCALE:
![313136345-1801eb6a-712e-4da1-b002-5766cd3b96a9](https://github.com/divakar618/Histogram-of-an-images/assets/121932143/f8f9fac0-2e61-42d1-ab73-689ba5f96e03)

### COLOR SCALE IMAGE:
![313136670-629cb394-9dea-4460-b6b5-e8cc0a28d66e](https://github.com/divakar618/Histogram-of-an-images/assets/121932143/bdfb99da-7d20-4c5d-a0da-30de13976ca8)


### Histogram Equalization of Grayscale Image.
### ORIGINAL:
![313136773-8656e9db-ed92-4ff4-9e8c-5ddfb4db38fc](https://github.com/divakar618/Histogram-of-an-images/assets/121932143/c5ac094c-b012-4e3a-8b4d-988c49723548)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
