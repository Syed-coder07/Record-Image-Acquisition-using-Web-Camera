## Record-Image-Acquisition-using-Web-Camera

## Developed by : Syed Shamsheer Ali B

## Register Number : 212225220114

## Aim:

To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:
1. Write the frame as a JPG file
2. Display the video
3. Display the video by resizing the window
4. Rotate and display the video

## Software Used:

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

## Program:

Developed by: Syed Shamsheer Ali .B
Register Number: 212225220114

EXP.NO: 02 Record-Image Acquisition using Web Camera

1-Capture the image

>```
>import cv2
>import matplotlib.pyplot as plt
>from IPython.display import clear_output
>import time
>```

>```
>cap = cv2.VideoCapture(0)
>ret, frame = cap.read()
>if ret:
   > cv2.imwrite("Syed1.jpg", frame)
>cap.release()
>```

>```
>captured_image = cv2.imread('Syed1.jpg')
>```

>```
>plt.imshow(captured_image[:,:,::-1])
>plt.title('Captured Frame')
>plt.axis('off')
>plt.show()
>```

2-Display the video

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

3- Display the video by resizing the window

    cap = cv2.VideoCapture(0)
    for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
    cap.release()

4- Rotate and display the video

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

Output:

1-Capture the image

<img width="616" height="512" alt="image" src="https://github.com/user-attachments/assets/de92cadc-b85d-41d6-a82e-a191d54d5732" />

2-Display the video

<img width="624" height="477" alt="image" src="https://github.com/user-attachments/assets/da9e733a-79e1-4d55-8d5e-051e42d16c88" />

3- Display the video by resizing the window

<img width="306" height="461" alt="image" src="https://github.com/user-attachments/assets/baa75b27-59d4-4ad1-80fe-63f174cd45a5" />

4- Rotate and display the video

<img width="350" height="470" alt="image" src="https://github.com/user-attachments/assets/3464ad1b-7d0d-4115-bf2b-a6b1c37d3a9d" />

Result:

Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.



