# IMAGE TRANSFORMATIONS


## Aim:
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image.

### Step5:
Reflect of the image.

### Step6:
Rotate the image.

## Program:
```
Developed By: JANANI.S
Register Number: 212222230049
```
```python
i) Original Image
# To show the original image and to find the shape of the image
import cv2
import numpy as np
img = cv2.imread('peacock.jpg',-1)
re=cv2.resize(img,(400,300))
original = cv2.cvtColor(re , cv2.COLOR_BGR2RGB)
cv2.imshow('input',original)
cv2.waitKey(0)
cv2.destroyAllWindows()
original.shape
row, col, dim =original.shape

ii)Image Translation
translation = np.float32([[1,0,100],[0,1,150],[0,0,1]])
translated_image = cv2.warpPerspective(original,translation,(col,row))
cv2.imshow('translated_image',translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii)Image shearing
shear_x = np.float32([[1,0.7,0],[0,1,0],[0,0,1]])
shear_y = np.float32([[1,0,0],[0.3,1,0],[0,0,1]])
sheared_x= cv2.warpPerspective(original,shear_x,(col,row))
sheared_y = cv2.warpPerspective(original,shear_y,(col,row))
cv2.imshow('shear_x',sheared_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('shear_y',sheared_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

iv)Image Reflection
ref_x = np.float32([[1,0,0],[0,-1,row],[0,0,1]])
ref_y = np.float32([[-1,0,col],[0,1,0],[0,0,1]])
reflect_x= cv2.warpPerspective(original,ref_x,(col,row))
reflect_y = cv2.warpPerspective(original,ref_y,(col,row))
cv2.imshow('reflected_x',reflect_x)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imshow('reflected_y',reflect_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

v)Image Rotation
angle = np.radians(15)
mat_rotate = np.float32([[np.cos(angle),-
(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotate_img =cv2.warpPerspective(original,mat_rotate,(col,row))
cv2.imshow('rotated',rotate_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

vi)Image Cropping
cropped_img=img[10:500,25:600] 
cv2.imshow('after_cropping',cropped_img);
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Original image

![Screenshot 2024-05-10 153220990](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/ecb36946-3b26-4ab9-bdef-a04641567735)

### i)Image Translation

![tis](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/54e7dfc4-909d-4fa0-a8fa-8736b16139aa)

### ii)Image shearing

![SHEARX](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/e493a792-14e2-4240-90c1-54acfc0f8b4f)

![Screenshot 2024-05-10 182017](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/0347ff55-0b6e-463c-a3fb-aed2a20c2960)

### iii)Image Reflection

![REFLECTEDX](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/aaac7cf0-9fb8-4e47-960f-60368bdf5854)

![REFLECTEDY](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/4745f772-d680-48d1-a1ac-4e3ee162934a)

### iv)Image Rotation

![ROTATED](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/d2c82128-f7da-4775-a1d4-fc43f6e16eb9)


### v)Image Cropping

![CROP](https://github.com/JananiSoundararajan/IMAGE-TRANSFORMATIONS/assets/119477549/926a5307-4bda-444c-8643-41d6a0433bd0)


Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
