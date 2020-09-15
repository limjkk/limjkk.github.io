---
title : "Canny Edge Detection"
date: 2018-06-30-18:00
categories:
- Opencv

tags:
- Opencv
---

---
# 소스코드

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
'''
Canny Edge Detection
경계값을 MinVal,MaxVal 두개로 잡는다.


'''
cam = cv2.VideoCapture(0) # 0번 웹캠을 사용
while True:
    ret , frame = cam.read()  # 캠의 데이터를 받는다
    frame = cv2.cvtColor(frame,cv2.COLOR_RGB2GRAY) # 캠의 데이터를 흑백으로 변경한다.
    edge1 = cv2.Canny(frame,100,200) # 캠의 데이터를 Canny 함수를 통해 변경
# Canny(이미지 나 영상객체,임계값1,임계값2)
    cv2.imshow('original',frame) # 영상 출력
    cv2.imshow('Canny Edge Dection',edge1) # Canny Edge Dection 함수로 변경한 영상 출력
    k = cv2.waitKey(1) & 0xFF
    if k == 27:
        break
cv2.destroyAllWindows()

```
---

# 실행결과
![이미지](/images/opencv/cannyedge/1.PNG)
---
