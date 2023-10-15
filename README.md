# OPENING--CLOSING

## Aim

To implement Opening and Closing using Python and OpenCV.

## Software Required

1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:

### Step1:

Import the necessary packages.

### Step2:

Create the Text using cv2.putText

### Step3:

Create the structuring element.

### Step4:

Use Opening operation.

### Step5:

Use Closing Operation.
 
## Program:
```
DEVELOPED BY:DHANUMALYA.D
REGISTER NUMBER:212222230030
``` 
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"DHANUMALYA",(5,80),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))
```
# Use Opening operation
```
image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')
```
# Use Closing Operation
```
image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')
```
## Output:

### Display the input Image

![Screenshot from 2023-10-15 10-55-19](https://github.com/Dhanudhanaraj/OPENING--CLOSING/assets/119218812/375a194c-c135-4bb2-b177-547c6b231692)

### Display the result of Opening

![Screenshot from 2023-10-15 10-55-28](https://github.com/Dhanudhanaraj/OPENING--CLOSING/assets/119218812/ccace4b8-16fb-4f49-b6bd-01f3a477e91f)


### Display the result of Closing

![Screenshot from 2023-10-15 10-55-37](https://github.com/Dhanudhanaraj/OPENING--CLOSING/assets/119218812/54430ade-4515-4929-8a90-0326c338be00)


## Result

Thus the Opening and Closing operation is used in the image using python and OpenCV.
