# OPENING--AND-CLOSING
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


#### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

#### Create the Text using cv2.putText
``` Python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Edible',(5,70), font,2,(255),5,cv2.LINE_AA)
```
#### Create the structuring element
```py
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


#### Use Opening operation
```py

image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```


#### Use Closing Operation
```py


image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")


```
## Output:

### Display the input Image
![image](https://github.com/shalini-venkatesan/OPENING--AND-CLOSING/assets/118720291/a4312b70-ac33-4dc9-b107-11fa23e07f35)


### Display the result of Opening
![image](https://github.com/shalini-venkatesan/OPENING--AND-CLOSING/assets/118720291/13150aa2-b922-4e79-8df9-5c8d432c2a40)


### Display the result of Closing
![image](https://github.com/shalini-venkatesan/OPENING--AND-CLOSING/assets/118720291/5d9e259f-a703-44bc-8886-2b9cea085d25)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
