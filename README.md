# Exp-10--Record-IMPLEMENTATION-OF-OPENING-AND-CLOSING

### NAME: BAVYA SRI B
### REG NO: 212224230034

## Aim

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

- Morphological Opening
- Morphological Closing

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create or load an input image containing foreground objects.

### Step 3:

Display the original image.

### Step 4:

Create a structuring element (kernel) of suitable size.

### Step 5: Opening Operation

- Apply the Opening operation using the structuring element.
- Opening consists of Erosion followed by Dilation.
- Remove small foreground noises while preserving the shape of larger objects.
- Display the opened image.

### Step 6: Closing Operation

- Apply the Closing operation using the structuring element.
- Closing consists of Dilation followed by Erosion.
- Fill small holes and gaps within foreground objects.
- Display the closed image.

### Step 7:

Compare the original, opened, and closed images.

## Program

#### Developed By

**Name:** BAVYA SRI B

**Register No:** 212224230034

```PYTHON

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Open and Close', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Input Image with Text")
plt.axis('off')
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  
plt.title("Opening Operation")
plt.axis('off')
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  
plt.title("Closing Operation")
plt.axis('off')

```

## Output

### Original Image

<img width="667" height="535" alt="image" src="https://github.com/user-attachments/assets/b03e6e37-b284-4305-ab09-e9340fca3e7f" />


### Opening Operation

<img width="682" height="532" alt="image" src="https://github.com/user-attachments/assets/3cd630e0-9c26-47ee-bc28-e67908d6e984" />


### Closing Operation

<img width="671" height="541" alt="image" src="https://github.com/user-attachments/assets/d5127d5e-7a20-49d5-966e-85f959147cda" />


## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV. 
