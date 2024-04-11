# EX 01 COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image

```python
    import cv2
    image=cv2.imread('leann.jpg',1)
    image=cv2.resize(image,(350,350))
    cv2.imshow('leann',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/b58a37d6-394f-4c70-8cb0-6728a303c5be)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/3a295951-b16c-40ce-b28e-17d298db776f)

### ii)Write the image

```python
    import cv2
    image=cv2.imread('leann.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/830612e6-cc8d-414d-89c7-47d39b393354)

### iii)Shape of the Image

```python
    import cv2
    image=cv2.imread('leann.jpg',1)
    print(image.shape)
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/722e4690-858e-4dc3-b4a8-a8e63dbf28a1)

### iv)Access rows and columns

```python
import random
    import cv2
    image=cv2.imread('leann.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/6017b4df-8b4c-45b0-b2cc-e89c747089f2)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/d88010e9-6c92-42f9-b88c-c7c3c37c2b07)


### v)Cut and paste portion of image

```python
  import cv2
  image=cv2.imread('leann.jpg',1)
  image=cv2.resize(image,(300,300))
  tag =image[150:200,110:160]
  image[110:160,150:200] = tag
  cv2.imshow('image1',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/86d8e04c-824e-42d8-83b9-5cb3524c375c)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/dc06e3f5-a8d3-4ea6-8d5d-1129843a0d46)


### vi) BGR and RGB to HSV and GRAY

```python
import cv2
img = cv2.imread('leann.jpg',1)
img = cv2.resize(img,(200,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/4d0d1f92-c7ca-4ce0-96f1-01f875461504)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/9777c928-03c2-4dbf-b6a6-af241a687275)

### vii) HSV to RGB and BGR

```python
import cv2
img = cv2.imread('leann.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/c33ff51b-495d-4d4b-8cac-f9f02d0740b8)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/a515cb34-389a-4508-811f-ce7b4a10bc9f)

### viii) RGB and BGR to YCrCb

```python
import cv2
img = cv2.imread('leann.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/6e0291ea-548f-4f5b-8bbe-aa99f21c8cae)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/93cf18ae-1315-4ebe-970a-2ac12f871630)



### ix) Split and merge RGB Image
```python
import cv2
img = cv2.imread('leann.jpg',1)
img = cv2.resize(img,(200,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/aa0b6730-0e6a-4b10-a7c0-eb6323955c85)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/b3d37cd7-ffde-4b01-8514-4f911c071a62)

### x) Split and merge HSV Image
```python
import cv2
img = cv2.imread("leann.jpg",1)
img = cv2.resize(img,(200,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/54797a72-6a3f-43e4-a5a6-26283f90d4b2)

![image](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/75b4ba0e-f372-47ff-bdad-22204f591b48)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







