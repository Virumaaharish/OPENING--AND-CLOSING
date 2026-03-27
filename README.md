# OPENING--AND-CLOSING
# NAME : VIRUMAA HARISH M
# REF NO : 212223230246
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

``` Python
# NAME :
# REF NO :

# Import libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read image in grayscale
image = cv2.imread("rose.png", 0)

# Create structuring element (kernel)
kernel = np.ones((5,5), np.uint8)

# ---------------- OPENING ----------------
opening = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# ---------------- CLOSING ----------------
closing = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

# ---------------- DISPLAY OUTPUT ----------------
titles = ["Original Image", "Opening", "Closing"]
images = [image, opening, closing]

plt.figure(figsize=(10,5))

for i in range(3):
    plt.subplot(1,3,i+1)
    plt.imshow(images[i], cmap='gray')
    plt.title(titles[i])
    plt.axis("off")

plt.tight_layout()
plt.show()
```
## Output:

### Display the input Image
<br>
<br>
<br>
<img width="249" height="363" alt="image" src="https://github.com/user-attachments/assets/0f935866-b00c-46b6-98b1-a1ea08a0f003" />

<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<img width="248" height="363" alt="image" src="https://github.com/user-attachments/assets/fdc45b9b-d297-4ae2-911e-a892f7fa2fb7" />


<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<img width="253" height="361" alt="image" src="https://github.com/user-attachments/assets/3d03d9a0-a719-4f83-a059-61ac417cb54d" />


<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
