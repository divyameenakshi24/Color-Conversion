# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>
Import cv2 and save and image as filename.jpg

### Step2:
<br>
Use imread(filename, flags) to read the file.

### Step3:
<br>
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another

### Step4:
<br>
Split and merge the image using cv2.split and cv2.merge commands

### Step5:
<br>
End the program and close the output image windows.

## Program:
```python
# Developed By:A.Divya Meenakshi
# Register Number:212220230014
# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('cat.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('cat.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows(




# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('cat.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()



# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('cat.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image

import cv2
image = cv2.imread('cat.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
### i) BGR and RGB to HSV and GRAY
![3 1](https://user-images.githubusercontent.com/75235402/162799412-75552f42-c205-46c4-9c15-d7a76b79b64e.JPG)
![3 2](https://user-images.githubusercontent.com/75235402/162799422-18bd95c9-8882-4183-9a69-5a883ed6bce8.JPG)
![3 3](https://user-images.githubusercontent.com/75235402/162799749-ca290b23-e8b3-44a4-8ed0-8778a77182d8.JPG)


### ii) HSV to RGB and BGR
![3 5](https://user-images.githubusercontent.com/75235402/162799879-4fcf4707-d80e-43e7-a2f0-4121bad51f2e.JPG)
![3 6](https://user-images.githubusercontent.com/75235402/162799887-642cc672-fcda-4adb-a6dc-fc8469e2719e.JPG)


### iii) RGB and BGR to YCrCb
![3 8](https://user-images.githubusercontent.com/75235402/162800108-1e0caa3c-68cb-4556-ba95-784464d6b0a4.JPG)
![3 9](https://user-images.githubusercontent.com/75235402/162800112-08b56205-e5d9-4169-8a92-21ca87ee59f2.JPG)




### iv) Split and merge RGB Image
![3 10](https://user-images.githubusercontent.com/75235402/162800532-78985c39-713f-48cf-945c-c9b8f571439d.JPG)
![3 11](https://user-images.githubusercontent.com/75235402/162800597-4d038e0e-3449-498b-b66e-5880f3a9a2b7.JPG)
![3 12](https://user-images.githubusercontent.com/75235402/162800649-e89bcb80-252a-44f1-845a-8aac085a8e9a.JPG)
![3 13](https://user-images.githubusercontent.com/75235402/162800701-9df5d7c2-1f3e-4f52-933c-501a63aa5ed9.JPG)



### v) Split and merge HSV Image
![3 14](https://user-images.githubusercontent.com/75235402/162800726-70fc4290-092d-4b7a-8add-e1a137ead882.JPG)
![3 15](https://user-images.githubusercontent.com/75235402/162800755-b4596fad-741a-4452-832c-09d6884140f2.JPG)
![3 16](https://user-images.githubusercontent.com/75235402/162800774-97728d47-0788-4455-8f32-f50a37ccb9d6.JPG)
![3 17](https://user-images.githubusercontent.com/75235402/162800786-a8b6e389-b1a6-42e0-9098-beca01a92b7a.JPG)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
