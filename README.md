### EX NO: 10
### DATE:
# <p align="center">IMPLEMENTATION OF EROSION AND DILATION</p>

# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion.

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
Plot the images using plt.imshow.
 
## Program:
```
### Developed By   : N Sandhya Charu
### Register Number: 212220230041
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Sandhya ",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235167/170851526-df329a0d-188d-497f-92a0-7967311009c2.png)

### Display the Eroded Image
![image](https://user-images.githubusercontent.com/75235167/170851546-d3f18e1f-c8a5-4576-b1b5-eea59e092207.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/75235167/170851552-0d8d0438-122c-435d-af56-b42f2d1183e9.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
