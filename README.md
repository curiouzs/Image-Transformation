# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By: LOKESH KRISHNAA M
Register Number: 212220230030


i)Image Translation

import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv 

#plotting of an image 
image = cv.imread("tata.jpg")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(image)
plt.show()

#translation of an image 
rows,cols,dim = image.shape
M = np.float32([[1,0,100], [0,1,50],[0,0,1]])

translated_image= cv.warpPerspective(image, M, (cols, rows))

plt.axis("off")
plt.imshow(translated_image)
plt.show()

ii) Image Scaling

#SCALING 
rows,cols,dim = image.shape

M_scale = np.float32([[2,0,0], [0,1.6,0],[0,0,1]])

scale_image= cv.warpPerspective(image, M_scale, (cols, rows))


plt.axis("off")
plt.imshow(scale_image)
plt.show()

iii)Image shearing

#shearing image 
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])


shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))


plt.axis("off")
plt.imshow(shear_imagex)
#plt.imshow(shear_imagey)
plt.show()


plt.axis("off")
#plt.imshow(shear_imagex)
plt.imshow(shear_imagey)
plt.show()


iv)Image Reflection

#reflect an image 
M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))


plt.axis("off")
plt.imshow(ref_imagex)
plt.show()


plt.axis("off")
plt.imshow(ref_imagey)
plt.show()


v)Image Rotation




vi)Image Cropping





```
## Output:
### i)Image Translation


### ii) Image Scaling


### iii)Image shearing



### iv)Image Reflection



### v)Image Rotation




### vi)Image Cropping





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
