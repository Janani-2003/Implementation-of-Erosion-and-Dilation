# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>Import the necessary packages.
### Step2:
<br>Create the Text using cv2.putText.
### Step3:
<br>Create the structuring element.

### Step4:
<br>Erode the image.

### Step5:
<br>Dilate the image.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((90,250),dtype='uint8')
img2=cv2.cvtColor(img1,cv2.COLOR_BGR2RGB)
font=cv2.FONT_HERSHEY_DUPLEX
cv2.putText(img2,'JANANI',(5,70),font,2,(218, 112, 214),3,cv2.LINE_8)
plt.imshow(img2)

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode1=cv2.erode(img2,kernel1)
plt.imshow(image_erode1)
# Dilate the image
image_dilate=cv2.dilate(img2,kernel1)
plt.imshow(image_dilate)
```
## Output:

### Display the input Image
<br>![image](https://github.com/Janani-2003/Implementation-of-Erosion-and-Dilation/assets/94288340/c3148e88-245a-46b1-aff7-1242e74c51ed)

<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
<br>![image](https://github.com/Janani-2003/Implementation-of-Erosion-and-Dilation/assets/94288340/fb5094db-3f48-4127-87cb-1afe19952313)

<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
<br>![image](https://github.com/Janani-2003/Implementation-of-Erosion-and-Dilation/assets/94288340/240be1ff-7949-4cbf-9413-3f2de062628d)

<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
