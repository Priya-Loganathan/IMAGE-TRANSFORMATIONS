# IMAGE-TRANSFORMATIONS

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective().

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:
Shear the image in both the rows and columns.

### Step5:
Find the reflection of the image.

## Program:
```
Developed By: DELLI PRIYA L
Register Number: 212222230029
```
### i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("/content/BIRD.webp")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
### ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
### iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/BIRD.webp")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
### iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
### v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/color.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
### vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("/content/BIRD.webp")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
```

## Output:
### i)Image Translation
![image](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/aeb8ea07-40ce-471e-80cd-3f2f5661ec92)

### ii) Image Scaling
![image](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/5d27edd0-9ace-46bf-8980-511f4957418e)

### iii)Image shearing
![image](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/cb96604d-e74d-4676-955e-be80d2e7d263)
![image](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/86ca4a6a-306a-404b-9cda-8dd2c59154bc)

### iv)Image Reflection
![image](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/71121449-6d8f-4630-9b36-ff3e312869b4)+
![328086101-80fbda47-c800-4f04-95a9-c47efe823333](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/2a95f84a-efb4-4c01-ae0d-fe8d872f06f2)

### v)Image Rotation
![328086203-172d6638-e301-4f72-9054-302ad5689fcb](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/5999b640-e733-4a21-a479-3cbd9961267c)
![328086203-172d6638-e301-4f72-9054-302ad5689fcb-1](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/3b833b4d-cc2b-42fd-8f37-096ba68b55e8)
![328086217-ebdfff3a-5b17-4ce3-bb0e-4c0d961a262f](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/e8916d9b-aa7f-426d-972b-33f0461effc6)

### vi)Image Cropping
![328086239-db45cdf5-1b63-42fd-8ef5-33cfb2c458ff](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/117a1d94-8dc0-4735-a0e4-86f5b972146d)
![328086239-db45cdf5-1b63-42fd-8ef5-33cfb2c458ff-1](https://github.com/Priya-Loganathan/IMAGE-TRANSFORMATIONS/assets/121166075/3275b4b5-3f0f-485a-be20-e4705ea200d4)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
