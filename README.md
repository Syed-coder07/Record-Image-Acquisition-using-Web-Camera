## Record-Image-Acquisition-using-Web-Camera-Completion-requirements

## Aim:

* To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

* Write the frame as a JPG file
* Display the video
* Display the video by resizing the window
* Rotate and display the video
* Software Used:
* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
  
## Algorithm:

Step 1:
Import the required libraries and initialize the webcam using cv2.VideoCapture().

Step 2:
Capture frames continuously from the webcam.

Step 3:
Save a frame as a JPG image using cv2.imwrite().

Step 4:
Display the live video stream using cv2.imshow().

Step 5:
Resize the frame and rotate it using OpenCV functions, then display the processed frames.

Program:
Developed By : SYED SHAMSHEER ALI .B

Register No : 212225220114

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
```

```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
cv2.imwrite("Syed1.jpg", frame)
cap.release()
```

```
captured_image = cv2.imread('Syed1.jpg')
```

```

plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```

```

cap = cv2.VideoCapture(0)
for i in range(50):
ret, frame = cap.read()
if not ret:
break
frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
clear_output(wait=True)
plt.imshow(frame_rgb)
plt.axis('off')
plt.show()
time.sleep(0.05)
cap.release()
```

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
for i in range(50):
ret, frame = cap.read()
if not ret:
break
resized_frame = cv2.resize(frame, (100, 150)) # Resize to 320x240
frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
clear_output(wait=True)
plt.imshow(frame_rgb)
plt.axis('off')
plt.show()
time.sleep(0.05)
cap.release()
```

```

cap = cv2.VideoCapture(0)
for i in range(50):
ret, frame = cap.read()
if not ret:
break
rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
clear_output(wait=True)
plt.imshow(frame_rgb)
plt.axis('off')
plt.show()
time.sleep(0.05)
cap.release()
```

## Output:

## Captured Frame:

<img width="620" height="511" alt="image" src="https://github.com/user-attachments/assets/c189fd4e-170d-4872-8dff-0abb77c68ef7" />


<img width="622" height="477" alt="image" src="https://github.com/user-attachments/assets/48a43956-8fd4-4aab-a50a-0a7d1e57f74a" />


<img width="437" height="493" alt="image" src="https://github.com/user-attachments/assets/d500ce9b-24e5-4a28-877f-d35d8f7dab52" />

## Rotate The Diaplay and Viddeo

<img width="447" height="506" alt="image" src="https://github.com/user-attachments/assets/31f7da8c-c086-41ab-9424-bff41e4318d8" />


## Result:

Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
