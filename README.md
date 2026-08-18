# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
<br>Load the necessary packages.

### Step2:
<br>Read the Image and convert to grayscale.



### Step3:
<br>Use Global thresholding to segment the image.



### Step4:
<br>Use Adaptive thresholding to segment the image.



### Step5:
<br>Use Otsu's method to segment the image and display the results.



## Program
Developed by 
 - NAME : HEMAVARATHAN S
 - REG NO : 212225240050

python
# Load the necessary packages
```
**import numpy as np
import matplotlib.pyplot as plt
import cv2**
```


# Read the Image and convert to grayscale
```

image = cv2.imread("spidy.png",1)
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray = cv2.imread("spidy.png",0)
```

# Use Global thresholding to segment the image
```
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)
```

# Use Adaptive thresholding to segment the image


```
thresh_img7=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)
```

# Use Otsu's method to segment the image 
```
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)
```

# Display the results


```
### Original Image

```
plt.axis("off")
plt.title("Original Image")
plt.imshow(image)
```
<img width="545" height="537" alt="image" src="https://github.com/user-attachments/assets/1b8be6a5-dbd9-4627-a86f-e698a003e241" />

### Global Thresholding
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```

### Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```

### Optimum Global Thesholding using Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
## Output
```
<img width="545" height="537" alt="image" src="https://github.com/user-attachments/assets/1b8be6a5-dbd9-4627-a86f-e698a003e241" />
<img width="427" height="385" alt="image" src="https://github.com/user-attachments/assets/c6ce6777-eb58-4f12-9dbe-405728cec21d" />
<img width="367" height="366" alt="image" src="https://github.com/user-attachments/assets/12ad27b8-3b4b-48fa-a6f1-05da51a49d1f" />
<img width="352" height="370" alt="image" src="https://github.com/user-attachments/assets/fb56ec74-0eab-48c9-a403-d2d10dc115c0" />
<img width="361" height="367" alt="image" src="https://github.com/user-attachments/assets/47e99684-40a0-4bd3-86de-a859793177d1" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
