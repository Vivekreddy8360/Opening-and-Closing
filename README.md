# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
1. Import the required packages.

### Step2:
2. Create the input image.
### Step3:
3. Create the structuring element.

### Step4:
4. Apply opening operation.
### Step5:
5. Apply closing operation.
 
## Program:

# Import necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
im=cv2.putText(img1,' SANATH ',(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Input Image",im)
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
cv2.imshow("Opening Image",image1)
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
cv2.imshow("Closing Image",image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Display the input Image
![hk1](https://user-images.githubusercontent.com/94525701/174123976-e71c68a3-06aa-4e40-92fd-59041afd8120.jpeg)


### Display the result of Opening
![hk2](https://user-images.githubusercontent.com/94525701/174123995-3be9b2cc-deb6-49e1-9290-8395e320c298.jpeg)


### Display the result of Closing
![hk3](https://user-images.githubusercontent.com/94525701/174124028-18343cc8-c35c-49c2-b9b7-c47d88b6a4af.jpeg)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
