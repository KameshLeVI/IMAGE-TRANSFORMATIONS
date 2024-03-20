# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
### Step2:
Load the image file in the program.
### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
### Step4:
Display the modified image output.
### Step5:
End the program.

## Program:
```python
Developed By: Kamesh D
Register Number: 212222240043
```
i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("solo.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,20],
               [0,1,10],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("solo.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows, cols, dims = input_image.shape
M = np.float32([[1.5,0,0],
               [0,1.8,0],
               [0,0,1]])
scaled_image = cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```


iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("solo.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0],
                 [0.5,1,0],
                 [0,0,1]])
shared_image_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
shared_image_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(shared_image_xaxis)
plt.show()
plt.axis('off')
plt.imshow(shared_image_yaxis)
plt.show()
```
iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sololevel.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x = cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflect_y = cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()
```

v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sololevel.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("sololevel.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.imshow(input_image)
plt.show()
cropped_img=input_image[50:200 ,50:500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### Original Image
![solo](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/f6e89b9c-5810-4afb-a001-10412e23865c)

![sololevel](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/5442361b-1ee6-4ac9-b701-a861df018d5e)

### i)Image Translation
![Screenshot 2024-03-20 103326](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/6d40eb69-05e5-4b2e-96ff-0445300d9b2b)

### ii) Image Scaling
![Screenshot 2024-03-20 103402](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/4e78a526-e261-4933-a431-1d4ea054f575)

### iii)Image shearing
![Screenshot 2024-03-20 103526](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/222d4445-0995-4fa0-91fe-51d5f5e612db)

### iv)Image Reflection
![Screenshot 2024-03-20 103609](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/7454f121-7576-4dc4-a7e3-0276557980c0)

### v)Image Rotation
![Screenshot 2024-03-20 103655](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/6024c5dc-8d9c-46eb-b16a-b4127482e985)


### vi)Image Cropping
 ![Screenshot 2024-03-20 103800](https://github.com/KameshLeVI/IMAGE-TRANSFORMATIONS/assets/120780633/80963d2e-c376-45d7-9554-4c0796e228c8)

## Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
