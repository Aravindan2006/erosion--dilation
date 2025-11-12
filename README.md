# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
Create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image

 
## Program:

``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
def load_image():
    blank_image = np.zeros((600,600))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_image,text='ARAVIND',org=(600,800),fontFace=font,fontScale = 5,color=(255,255,255),thickness=15,lineType=cv2.LINE_AA)
    return blank_image
def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
img=load_image()
display_img(img)
kernel=np.ones((5,5),dtype=np.uint8)
erosion = cv2.erode(img,kernel,iterations = 2)
display_img(erosion)
dilution=cv2.dilate(img,kernel,iterations=2)
display_img(dilution)

```
## Output:

### Display the input Image
<img width="677" height="463" alt="image" src="https://github.com/user-attachments/assets/40cded65-c123-4a0d-9243-2a84687bef4a" />


### Display the Eroded Image
<img width="643" height="462" alt="image" src="https://github.com/user-attachments/assets/4c8f1fc9-3834-4ff2-a09a-05595cdb52b6" />


### Display the Dilated Image
<img width="627" height="467" alt="image" src="https://github.com/user-attachments/assets/72b26570-0fff-4017-a91b-6f8368f93449" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
