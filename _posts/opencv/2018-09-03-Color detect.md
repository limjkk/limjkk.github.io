---
title : "카메라를 이용한 색 검출"
date: 2020-04-07-18:00
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

cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    hsv = cv2.cvtColor(frame,cv2.COLOR_BGR2HSV)
    # 웹캠에서 전송되는 비디오 프레임을 HSV 색공간으로 변경.
    # HSV ( 색상(Hue), 채도(Saturation), 명도(Value)의 좌표를 써서 특정한 색을 지정한다. )
    lower_blue = np.array([110,100,100])
    upper_blue = np.array([130,255,255])
    lower_green = np.array([45,100,100])
    upper_green = np.array([80,255,255])
    lower_red = np.array([-10,100,0])
    upper_red = np.array([10,255,255])
     # HSV 이미지에서 각 색깔별로 추출하기 위한 임계값.
    mask_blue = cv2.inRange(hsv,lower_blue,upper_blue)
    mask_green = cv2.inRange(hsv,lower_green,upper_green)
    mask_red = cv2.inRange(hsv,lower_red,upper_red)

    # mask와 원본 이미지를 비트 연산함
    res1 = cv2.bitwise_and(frame,frame,mask=mask_blue)
    res2 = cv2.bitwise_and(frame,frame,mask=mask_green)
    res3 = cv2.bitwise_and(frame,frame,mask=mask_red)

    cv2.imshow("Original",frame)
    cv2.imshow("Blue",res1)
    cv2.imshow("Green",res2)
    cv2.imshow("Red",res3)
    k = cv2.waitKey(1) & 0xFF

    if k == 27:
        break
cv2.destroyAllWindows()


```
---

# 경계값
![이미지](/images/opencv/colordetect/1.png)
---

# HSV
![이미지](/images/opencv/colordetect/2.png)
---

# 실행결과
![이미지](/images/opencv/colordetect/3.png)
---
