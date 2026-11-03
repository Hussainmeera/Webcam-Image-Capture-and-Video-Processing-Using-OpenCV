# EXP-2-Record-Image-Acquisition-using-Web-Camera
## Aim
To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

Write the frame as a JPG file
Display the video
Display the video by resizing the window
Rotate and display the video
## 🛠️ Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
## ⚙️ Algorithm
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

## 💻 Program
# Developed By:
## Name: MEERA HUSSAIN A
## Register No: 212224230155
```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
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
## Output
i) Write the frame as JPG image
Captured image is saved as captured_image.jpg

<img width="1027" height="407" alt="image" src="https://github.com/user-attachments/assets/f4bbd4ca-7e7e-46b6-b327-12342514e024" />



ii) Display the video
Live webcam video is displayed

<img width="1146" height="393" alt="image" src="https://github.com/user-attachments/assets/12c108e5-32c6-4291-9d2b-658be511705c" />


iii) Display the video by resizing the window
Video is shown in resized resolution (640 × 480)

<img width="1070" height="398" alt="image" src="https://github.com/user-attachments/assets/7252d788-6c20-4dd7-b79d-fd1a41fb76e6" />



iv) Rotate and display the video
Video is displayed after rotation (90° clockwise)

<img width="1097" height="406" alt="image" src="https://github.com/user-attachments/assets/db1dc59f-3f12-4140-b16c-6e3a0284ae6a" />



## Result
Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.
