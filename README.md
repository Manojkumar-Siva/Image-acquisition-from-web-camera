# Image-Acquisition-from-Web-Camera
# Aim:
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.<br/>
i) Write the frame as JPG. <br/>
ii) Display the video. <br/>
iii) Display the video by resizing the window.<br/>
iv) Rotate and display the video.

# Software Used: 
 Anaconda - Python 3.7
# Algorithm:
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

# Program:
``` Python
### Developed By:
### Register No:

## i) Write the frame as JPG file
import cv2
vidcap=cv2.VideoCapture(0)

while True:
    ref,frame=vidcap.read()
    cv2.imwrite("Newvid.jpg",frame)
    if cv2.waitKey(1)==ord('p'):
        break
vidcap.release()
cv2.destroyAllWindows()



## ii) Display the video
import cv2
import numpy as np

cap=cv2.VideoCapture(0)

while True:
    ref,frame =cap.read()
    cv2.imshow('frame',frame)
    if cv2.waitKey(1)==ord('p'):
        break
cap.release
cv2.destroyAllWindows()



## iii) Display the video by resizing the window
import cv2
import numpy as np

cap=cv2.VideoCapture(0)

while True:
    ref,frame1=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image = np.zeros(frame1.shape,np.uint8)
    smaller_frame=cv2.resize(frame1,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    
    cv2.imshow('frame',image)
    if cv2.waitKey(1)==ord('l'):
        break
cap.release()
cv2.destroyAllWindows()




## iv) Rotate and display the video
import cv2
import numpy as np

cap=cv2.VideoCapture(0)

while True:
    ref,frame1=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    
    image = np.zeros(frame1.shape,np.uint8)
    smaller_frame=cv2.resize(frame1,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)

    
    cv2.imshow('frame',image)
    if cv2.waitKey(1)==ord('l'):
        break
cap.release()
cv2.destroyAllWindows()
```
# Output:

### i) Write the frame as JPG image
</br>

![](./ot1.jpeg)

### ii) Display the video
</br>

![](./ot2.jpeg)


### iii) Display the video by resizing the window
</br>

![](./ot3.jpeg)

### iv) Rotate and display the video
</br>

![](./ot4.jpeg)
# Result:
Thus the image is accessed from webcamera and displayed using openCV.
