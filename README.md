# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and any one channel of the color image.
<br>

### Step3:
Display the histograms.
<br>

### Step4:
Equalize the color image.
<br>

### Step5:
Display the equalized grayscale image.
<br>

## Program:
```python
# Developed By: JEEVAGOWTHAM S
# Register Number: 212222230053

import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('gray.jpg')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('color.jpg')
plt.imshow(Color_image)
plt.show()


# Write your code to find the histogram of gray scale image and color image channels.
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("gray_scale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image

hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("color_scale value")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 

equ=cv2.equalizeHist(cv2.imread('color.jpg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()






```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2023-09-08 134422](https://github.com/JeevaGowtham-S/HISTOGRAM/assets/118042624/3079563c-2d49-4028-b3da-eba052f6f8c8)

![Screenshot 2023-09-08 134158](https://github.com/JeevaGowtham-S/HISTOGRAM/assets/118042624/ffb60fb0-af0d-4492-b23b-e6204e1ca6f1)


<br>
<br>
<br>
<br>

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2023-09-08 134738](https://github.com/JeevaGowtham-S/HISTOGRAM/assets/118042624/e0b45a17-1675-4b32-bb90-2547f6179b78)
![Screenshot 2023-09-08 134728](https://github.com/JeevaGowtham-S/HISTOGRAM/assets/118042624/29ca0fd0-bc37-4e7c-a727-f4b75aa10174)

<br>
<br>
<br>
<br>

### Histogram Equalization of Grayscale Image
![Screenshot 2023-09-08 135737](https://github.com/JeevaGowtham-S/HISTOGRAM/assets/118042624/dac46b93-0c30-4d1f-8c40-4a26ce487eeb)



<br>
<br>
<br>
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
