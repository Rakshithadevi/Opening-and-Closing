# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages.

## Step 2:
Create the Text using cv2.putText.

## Step 3:
Create the structuring element.

## Step 4:
Use Opening operation.

## Step 5:
Use Closing Operation.

## Step 6:
Print the output and end the program.

 
## Program:
```
# Developed By   : Rakshitha devi J
# Register Number: 212221230082

import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
import numpy as np

# Create the Text using cv2.putText
img1 = np.zeros((100,600), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'RAKSHITHA DEVI J',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')

# Create the structuring element
kernel = np.ones((5,5),np.uint8)
erosion = cv2.dilate(img1,kernel,iterations = 1)
cv2.erode(img1, kernel)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1, 'gray')

# Dilate the image
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2, 'gray')


```
## Output:

### Display the input Image
![image](https://github.com/Rakshithadevi/Opening-and-Closing/assets/94165326/4c9f5dac-ea07-4831-9376-fae9a5f28f5c)
### Display the result of Opening
![image](https://github.com/Rakshithadevi/Opening-and-Closing/assets/94165326/f6828447-e1f3-4757-802f-7f3e16760f84)
### Display the result of Closing
![image](https://github.com/Rakshithadevi/Opening-and-Closing/assets/94165326/c9ea4bec-a19e-4803-bba7-59d0bc1659a6)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
