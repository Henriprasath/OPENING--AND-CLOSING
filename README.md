# EXP 10
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation. 
## Program:
```
DEVELOPED BY: HENRIPRASATH S
REGISTER NO: 212223230077
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'HENRI', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image

![Screenshot 2025-05-21 023602](https://github.com/user-attachments/assets/acd96f17-ebb3-4f07-8c50-eaac8a0385a6)




### Display the result of Opening

![Screenshot 2025-05-21 023608](https://github.com/user-attachments/assets/0a7d4285-4484-45e9-a7a1-9c8b5d457536)



### Display the result of Closing

![Screenshot 2025-05-21 023613](https://github.com/user-attachments/assets/3fcb49e9-e6fc-4662-9dd4-2a44c8d3e8ca)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
