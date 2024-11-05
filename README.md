# Image_Acqusition-_using_Web_Camera
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
### step1:Initialize Video Capture: Import OpenCV and create a VideoCapture object (cv2.VideoCapture(0)).
### step2:Capture a Single Frame: Read a frame and save it as a JPEG file using cv2.imwrite() if the frame is successfully captured.
### step3:Display Video in Real-Time: Enter a loop to continuously capture and display frames using cv2.imshow() until a key press (e.g., 'q') is detected.
### step4:Resize the Video Frames: Capture frames, resize them with cv2.resize(), and display the resized frames until a key press is detected.
### step5:Rotate and Display the Video: Capture frames, rotate them with cv2.rotate(), and display the rotated frames until a key press is detected.

## Program:

### Developed By: SARAVANA KUMAR M
### Register No: 212222230133

## i) Write the frame as JPG file
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while (True):
    ret, frame = videoCaptureObject.read()
    cv2.imwrite("trial.jpeg", frame)
    result = False
videoCaptureObject.release()
cv2.destroyAllWindows()

```
## ii) Display the video
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while True:
    ret, frame = videoCaptureObject.read()
    if not ret:
        break
    cv2.imshow("Video", frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()

```

## iii) Display the video by resizing the window

```
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    if not ret:
        break
    smaller_frame = cv2.resize(frame, (0, 0), fx=0.5, fy=0.5)
    cv2.imshow('myimage', smaller_frame)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```

## iv) Rotate and display the video
```
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video', rotated_frame)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```

## Output

### i) Write the frame as JPG image
</br>

![trial](https://github.com/user-attachments/assets/e9986506-2755-4808-8b20-f528a5ba3ea2)

</br>


### ii) Display the video
</br>
![Screenshot 2024-11-05 092320](https://github.com/user-attachments/assets/420b8b72-7bdc-4906-8b2a-740d7440d802)

</br>


### iii) Display the video by resizing the window
</br>

![Screenshot 2024-11-05 092358](https://github.com/user-attachments/assets/b68d024a-3f51-44c6-950f-12d9c4bc1b00)
</br>



### iv) Rotate and display the video
</br>

![Screenshot 2024-11-05 092521](https://github.com/user-attachments/assets/99f14e1d-8752-4aed-a1fa-7c5f586edb4f)

</br>

## Result:
Thus the image is accessed from webcamera and displayed using openCV.
