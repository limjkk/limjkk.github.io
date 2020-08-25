---
title : "이미지 블렌딩"
date: 2020-04-07-18:00
categories:
- Opencv

tags:
- Opencv
---

---
# 소스코드

```
# 이미지 블렌딩

import numpy as np
import cv2

# cv2.addWeighted()함수는 새로운 이미지로 블렌딩하는 함수.

def onMouse(x):
    pass
def imgBlending(imgfile,imgfile2):
    img1 = cv2.imread(imgfile)
    img2 = cv2.imread(imgfile2)
    cv2.namedWindow('imgPane')
    cv2.createTrackbar("Mixing","ImgPane",0,100,onMouse)
    mix = cv2.getTrackbarPos("MIXING","ImgPane")
    while True:
        img = cv2.addWeighted(img1,float(100-mix)/100,img2,float(mix)/100,0)
        cv2.imshow('ImgPane',img)
        k = cv2.waitKey(1) & 0xFF
        if k == 27:
            break
        mix - cv2.getTrackbarPos("MIXING","ImgPane")
    cv2.destroyAllWindows()
imgBlending("Image/img1.jpg","Image/img2.jpg")


```
---

# IMG1
![이미지](/images/opencv/imageblending/img1.jpg)
---

# IMG2
![이미지](/images/opencv/imageblending/img2.jpg)
---

# Added Image
![이미지](/images/opencv/imageblending/Added Image.PNG)
---
