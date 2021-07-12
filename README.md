# Face-detection-using-opencv
## Steps
### First of all make sure you have OpenCV installed. You can install it using pip:

`pip install opencv-python`

### You need to download the trained classifier XML file (haarcascade_frontalface_default.xml), which is available in OpenCv’s

https://github.com/adarsh1021/facedetection/blob/master/haarcascade_frontalface_default.xml
### To detect faces in images:
 ````
 ```
 import cv2

# Load the cascade

face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')

# Read the input image

img = cv2.imread('test.jpg')

# Convert into grayscale

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Detect faces

faces = face_cascade.detectMultiScale(gray, 1.1, 4)

# Draw rectangle around the faces

for (x, y, w, h) in faces:

  cv2.rectangle(img, (x, y), (x+w, y+h), (255, 0, 0), 2)
    
# Display the output


cv2.imshow('img', img)

cv2.waitKey() 
```
````







Results:
![2021-07-10 (2)](https://user-images.githubusercontent.com/85651071/125176745-a4466c00-e1de-11eb-90cb-4bf886e9e4e5.png)



