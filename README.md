# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required libraries and image for transformation.
### Step2:
Perform operations on the image like translaton, rotation and other.
### Step3:
Use the warpPerspective(image , matrix, (rows, columns)) function.
### Step4:
Plot the Image and Transformed Image on the graph using matplotlib for identifying changes.
### Step5:
Diifferent operations has been performed on the image.

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
angle=np.radians(10)
matrix=np.float32([[np.cos(angle),-np.sin(angle),0],
                                [np.sin(angle),np.cos(angle),0],
                                [0,0,1]])
Rotated_image=cv.warpPerspective(image,matrix,(cols,rows))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
# cropping 
crop_img = image[600:750, 400:500]
plt.axis("off")
plt.imshow(crop_img)
plt.show()
```

## Output:
### i)Image Translation

<img src ="https://user-images.githubusercontent.com/75234646/165653509-6b829a40-7a7c-4df0-9626-3233dcf66fa5.png" width ="65%" height="50%">
### ii) Image Scaling
<img src ="https://user-images.githubusercontent.com/75234646/165653522-98a8f535-bdbc-49ed-b76b-f2aba5aba1b7.png" width ="65%" height="50%">
### iii)Image shearing
<img src ="https://user-images.githubusercontent.com/75234646/165653487-2c118e4e-74d0-44d2-91f3-ebda4a919dd1.png" width ="65%" height="50%">
### iv)Image Reflection
<img src ="https://user-images.githubusercontent.com/75234646/165653555-c90c67c7-1e3e-4f6c-b950-f9fa404e6054.png" width ="65%" height="50%">
### v)Image Rotation
<img src ="https://user-images.githubusercontent.com/75234646/165653973-b50356da-e7e6-4510-bd3e-67ff25b85fb2.png" width ="65%" height="50%">
### vi)Image Cropping
<img src ="https://user-images.githubusercontent.com/75234646/165653542-487117bd-9774-46ff-82a4-e14dc1c91211.png" width="65%" height="50%">

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
