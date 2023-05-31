# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the text image using cv2.putText.

### Step 3:
Then create the structuring image for dilation/erosion.

### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step 5:
Plot the images using plt.imshow.
 
## Program:

```
Developed by : Parshwanath M
Register Number : 212221230073
```

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
img=cv2.cvtColor(text_image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"PARSH",(5,70),font,2,(0,0,255),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(img,kernel)
cv2.imshow("Eroded Image",image_erode)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate the image
image_dilate = cv2.dilate(img,kernel)
cv2.imshow("Dilated Image",image_dilate)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image
![#1](https://github.com/parsh2004/Implementation-of-Erosion-and-Dilation/assets/95388047/7d74bcdd-04d5-41a5-8511-9bbb9bedf402)

### Display the Eroded Image
![#2](https://github.com/parsh2004/Implementation-of-Erosion-and-Dilation/assets/95388047/3a336b4b-bbcc-4ac2-9d4f-06076930f60e)

### Display the Dilated Image
![#3](https://github.com/parsh2004/Implementation-of-Erosion-and-Dilation/assets/95388047/1efb741f-f462-41f3-baa2-14fb9aef18ce)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
