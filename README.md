# COLOR_CONVERSIONS_OF-IMAGE
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
### Developed By:S.THIRISHA
### Register Number: 212222230160


## Output:

### i) Read and display the image

```python
    import cv2
    image=cv2.imread('dog.png',1)
    image=cv2.resize(image,(300,300))
    cv2.imshow('3SHA',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/bfccb508-249d-4773-89ec-9bb38b4d075a)

![Screenshot 2024-02-15 093755](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/572e8778-7c2a-4f0f-9ac5-71a9bb784ff2)


### ii)Write the image

```python
    import cv2
    image=cv2.imread('dog.png',0)
    cv2.imwrite('demos.jpg',image)
```
![Screenshot 2024-02-15 094552](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/a75a5993-67c1-42ab-aaf8-d69793e13184)


### iii)Shape of the Image

```python
    import cv2
    image=cv2.imread('dop.jpg',1)
    print(image.shape)
```
![Screenshot 2024-02-15 094559](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/a44da894-ea18-41ef-a7e8-83d17ccaf6c1)


### iv)Access rows and columns

```python
import random
    import cv2
    image=cv2.imread('dog.png',1)
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
![304987272-657e161c-be5b-44d5-8b9e-000a9f5e0b1c](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/d7071db1-6172-4de2-869c-7e51853a7cce)

![Screenshot 2024-02-15 094522](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/3e572071-8c1b-4b53-9761-8b8222fb8beb)



### v)Cut and paste portion of image

```python
  import cv2
  image=cv2.imread('dog.jpg',1)
  image=cv2.resize(image,(300,300))
  tag =image[150:200,110:160]
  image[110:160,150:200] = tag
  cv2.imshow('image1',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
```
![304988239-7ffe4b36-c8d7-4902-a3a1-e9720647682e](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/6268ac79-0a4d-4ce6-9496-8b60f709c2d7)

![Screenshot 2024-02-15 094741](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/8a9ce0f0-22fa-439f-9715-d96f7ccb5ad7)


### vi) BGR and RGB to HSV and GRAY

```python
import cv2
img = cv2.imread('dog.jpg',1)
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

![304988508-a3006cdb-b35a-419c-8f88-a986de2072c4](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/22fd881d-afb8-4141-8db1-a345a7be69b3)

![Screenshot 2024-02-15 094913](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/217c908a-9522-46df-944b-66a9be169d48)


### vii) HSV to RGB and BGR

```python
import cv2
img = cv2.imread('dog.jpg')
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
![304988706-88206ce0-702d-4986-aa3c-ad55dc8fc5b5](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/31f19aa7-2005-4e7a-b4c0-c58ba31779ca)


![Screenshot 2024-02-15 095002](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/5907ef97-23fa-4c4f-89e1-c5ba2b83158a)



### viii) RGB and BGR to YCrCb

```python
import cv2
img = cv2.imread('dog.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![Screenshot 2024-02-15 131312](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/57380cdc-e99a-480f-82a9-5fa8600afc0a)

![image](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/569b54c7-b673-4250-a168-01462a3bbe74)


### ix) Split and merge RGB Image
```python
import cv2
img = cv2.imread('dog.jpg',1)
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
![Screenshot 2024-02-15 131359](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/90f840e4-7d15-435a-8e06-17513b052240)

![image](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/0fc7d567-dc30-4128-bca3-2d5bf919f7b0)


### x) Split and merge HSV Image
```python
import cv2
img = cv2.imread("dog.jpg",1)
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
![Screenshot 2024-02-15 131434](https://github.com/Leann4468/COLOR_CONVERSIONS_OF-IMAGE/assets/121165979/257b3f94-b302-4733-a559-ffb17387b339)

![image](https://github.com/Thirisha-s/COLOR_CONVERSIONS_OF-IMAGE/assets/120380280/5324ef18-5e75-4bfb-ac8e-1dae42b76e28)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.
