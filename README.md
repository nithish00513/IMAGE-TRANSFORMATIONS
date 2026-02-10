# IMAGE-TRANSFORMATIONS
## name:nithish kumar s
## reg:212224230190


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import all the necessary modules

### Step2:
<br>Choose an image and save it as filename.jpg

### Step3:
<br>Use imread to read the image

### Step4:
<br>Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
<br>Use cv2.warpPerspective(image,M,(cols*2,rows*2)) to scale the image
### Step6:
Use cv2.warpPerspective(image,M,(int(cols*1.5),int(rows*1.5))) for x and y axis to shear the image

### Step7:
<br>Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image
### Step8:
<br>Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image
### Step9:
<br>Crop the image to remove unwanted areas from an image
### Step10:

<br>Use cv2.imshow to show the image
### Step11:
<br>End the program
## Program:

## Developed By: A joans jay authers
# Register Number:212221240019
i)Image Translation
```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("dip.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

```


ii) Image Scaling
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```


iii)Image shearing
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

iv)Image Reflection
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```


v)Image Rotation
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
```


vi)Image Cropping
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Cropping:")
plt.imshow(translated_image)
plt.show()
```




## Output:
 i)Image Translation

<img width="804" height="515" alt="image" src="https://github.com/user-attachments/assets/e8039252-dd87-46d4-8b81-ca802940d4aa" />




 ii) Image reflected
 <img width="657" height="455" alt="image" src="https://github.com/user-attachments/assets/81406914-08fa-442f-9109-691231a98154" />







 iii)Image shearing

<img width="1296" height="489" alt="image" src="https://github.com/user-attachments/assets/99b7189a-28c1-4f0b-b0ca-0f4f34f4c832" />











 v)Image Rotation

<img width="677" height="490" alt="image" src="https://github.com/user-attachments/assets/656c6bf1-3890-48cb-834c-3a73d92998cb" />






vi)Image Cropping
<img width="696" height="515" alt="image" src="https://github.com/user-attachments/assets/282d9c34-eb04-4473-ae81-9b5685bc44be" />








## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
