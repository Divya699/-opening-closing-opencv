# Ex 10 Opening and Closing Operations Using OpenCV
## Aim
To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

## The program performs the following operations:

Morphological Opening

Morphological Closing

## Software Used

Anaconda – Python 3.7

Jupyter Notebook / VS Code

OpenCV (cv2)

NumPy

Matplotlib

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

Apply the Opening operation using the structuring element.

Opening consists of Erosion followed by Dilation.

Remove small foreground noises while preserving the shape of larger objects.

Display the opened image

### Step 6: Closing Operation

Apply the Closing operation using the structuring element.

Closing consists of Dilation followed by Erosion.

Fill small holes and gaps within foreground objects.

Display the closed image.

### Step 7:

Compare the original, opened, and closed images.

## Program

### Developed By : DIVYA PRIYA S

### Register No: 212225240037

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'DIVYA PRIYA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
```
```
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
```
```
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')
```
```
# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
```
```
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Closing Operation")
plt.axis('off')
```
# OUTPUT

<img width="478" height="812" alt="image" src="https://github.com/user-attachments/assets/00811d5e-482b-43b2-b983-544a918da03e" />

## ORIGINAL IMAGE

<img width="731" height="579" alt="image" src="https://github.com/user-attachments/assets/132c40d9-6494-494c-8beb-1412208b9ac6" />

## OPENING OPERATION

<img width="735" height="582" alt="image" src="https://github.com/user-attachments/assets/917771d8-1884-4eb5-bd6b-3d6006a99c45" />

## CLOSING OPERATION

<img width="719" height="495" alt="image" src="https://github.com/user-attachments/assets/bc872509-8d36-4e65-a8b6-49a022519efb" />


# RESULT

Thus, the morphological operations Opening and Closing are successfully implemented using OpenCV.
