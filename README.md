# Image-Acquisition-from-Web-Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7

## Algorithm

### Step 1:
Use VideoCapture(0) to access web camera

### Step 2:
Use imread to read the video or image

### Step 3:
Use imwrite to save the image

### Step 4:
Use imshow to show the video

### Step 5:
End the program and close the output video windows by pressing 'q'

## Program:
``` 
### Developed By:Suji.G
### Register No:212222230152

## i) Write the frame as JPG file

import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('212222230152_suji', frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()
### Developed By:
### Register No:




## ii) Display the video

import cv2
import numpy as np

cap = cv2.VideoCapture(0)

while True:
    ret,frame1= cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    
    image = np.zeros(frame1.shape, np.uint8)
    smaller_frame = cv2.resize(frame1, (0,0), fx=0.5, fy=0.5)
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[:height//2, width//2:] = smaller_frame
    image[height//2:, width//2:] = smaller_frame
    cv2.imshow('212222230152_suji',image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


## iii) Display the video by resizing the window

import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8)
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
    image[:height//2, :width//2] = smaller_frame
    image[height//2:, :width//2] = smaller_frame
    image[:height//2, width//2:] = smaller_frame
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('212222230152_suji', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()




## iv) Rotate and display the video


import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8)
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180
    image[height//2:, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180
    image[:height//2, width//2:] = smaller_frame
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('212222230152_suji', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()



```
## Output

### i) Write the frame as JPG image


![Screenshot from 2023-03-23 08-36-29](https://user-images.githubusercontent.com/119559822/227097733-da43f8f3-cbc2-4c01-b0cf-bc035ddefebf.png)

### ii) Display the video


![Screenshot from 2023-03-23 08-59-51](https://user-images.githubusercontent.com/119559822/227097742-7d791c8a-a9c0-4c28-97c1-8fce08b4eae5.png)

### iii) Display the video by resizing the window

![Screenshot from 2023-03-23 09-04-15](https://user-images.githubusercontent.com/119559822/227097749-18a10634-658a-49bb-b586-0641e5a272fb.png)



### iv) Rotate and display the video



![Screenshot from 2023-03-23 09-11-43](https://user-images.githubusercontent.com/119559822/227097760-e1bd5b0c-38b4-45d3-b320-72758231062c.png)



## Result:
Thus the image is accessed from webcamera and displayed using openCV.
