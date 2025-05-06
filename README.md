# EXP-10 OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation


 
## Program:
```

# Developed By: MONISH N
# Register No: 212223240097

import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"HAREESH R",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:
 
### Display the input Image
![Screenshot 2025-05-06 180749](https://github.com/user-attachments/assets/8b6dc36f-b6ee-4805-95ef-660a10623fa5)

### Display the result of Opening
![Screenshot 2025-05-06 180800](https://github.com/user-attachments/assets/7d8ab2d0-e1ef-461e-b767-7b8250f41bce)

### Display the result of Closing
![Screenshot 2025-05-06 180810](https://github.com/user-attachments/assets/afab4a16-34ce-4da2-b088-54ffa8de8eff)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
