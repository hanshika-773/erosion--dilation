# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>Create a blank black image using NumPy.


### Step2:
<br>Add large text (e.g., “YASH”) on the image using cv2.putText().

### Step3:
<br>Define a kernel for morphological operations.

### Step4:
<br>Apply erosion to shrink the text.

### Step5:
<br>Apply dilation to expand the text and display all images.

 
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = np.zeros((800, 800, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hanshi', (200, 400), font, 5, (255, 255, 255), 10, cv2.LINE_AA)

kernel = np.ones((5, 5), np.uint8)

eroded = cv2.erode(image, kernel, iterations=1)
dilated = cv2.dilate(image, kernel, iterations=1)

plt.figure(figsize=(12, 6))

plt.subplot(1, 3, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(cv2.cvtColor(eroded, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(cv2.cvtColor(dilated, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')

plt.tight_layout()
plt.show()

```
## Output:

### Display the input Image

<img width="208" height="236" alt="Screenshot 2025-11-17 114725" src="https://github.com/user-attachments/assets/1da10e87-ed72-473b-8848-9b21b89a2863" />



### Display the Eroded Image

<img width="208" height="238" alt="Screenshot 2025-11-17 114738" src="https://github.com/user-attachments/assets/5197cc72-36a7-47be-8de8-6dafad84400a" />



### Display the Dilated Image

<img width="207" height="238" alt="Screenshot 2025-11-17 114801" src="https://github.com/user-attachments/assets/75774679-42a5-4575-bf20-29732d47e594" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
