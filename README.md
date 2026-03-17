# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale

### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.
### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.
### Step5:
Display and compare the original, eroded, and dilated images.

 
## Program:
```
 Developed by : D.Raju
 Register number:212224240128
```

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```



# Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

#  Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```


# Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```



```
 kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
# Apply erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
# Apply dilation (expanding effect)
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
# Display the dilated image
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
```
```
## Output:

### Display the input Image
<img width="521" height="518" alt="image" src="https://github.com/user-attachments/assets/e4fd4326-3fe6-4a2a-ae09-d7c79f5a6b3a" />


### Display the Eroded Image
<img width="488" height="522" alt="image" src="https://github.com/user-attachments/assets/e21608cb-a05d-47e6-a103-315a8957bab1" />


### Display the Dilated Image

<img width="507" height="502" alt="image" src="https://github.com/user-attachments/assets/e6092ef9-b4f6-4c11-87c3-4303aab6922f" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
