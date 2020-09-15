---
title: 서로 다른 두 프레임 홍채 패턴 비교
date: 2020-07-01-18:00
categories:
- Opencv

tags:
- Opencv
---

# [결과]비교 이미지
![이미지](/images/opencv/Skew Deviation/1.png)
---

서로다른 두 프레임의 홍채를 촬영, 홍채 패턴을 분석하기 위해 Linear Polar를 사용하여
두 프레임의 홍채를 일직선으로 Polar시킨다. 이후 SIFT를 사용하여 두 홍채의 패턴을 비교한다.

---

# 서로 다른 두 프레임의 동공사진

![alt-text-1](/images/opencv/Skew Deviation/before.jpg "before") | ![alt-text-2](/images/opencv/Skew Deviation/after.jpg "after")

# Hough Circle 함수를 적용해 동공검출


![alt-text-1](/images/opencv/Skew Deviation/bfcimg.jpg "before") | ![alt-text-2](/images/opencv/Skew Deviation/afcimg.jpg "after")

# Linear Polar를 적용 시킨 이미지


![alt-text-1](/images/opencv/Skew Deviation/nzero.jpg "before") | ![alt-text-2](/images/opencv/Skew Deviation/none.jpg "after")


# SIFT 적용


![alt](/images/opencv/Skew Deviation/Compare.png)


<span style="font-family: '함초롬바탕';"> 흔히 사용되는 홍채인식 방법을 사용하여 Skew Deviation을 검출 하는 방법을 구현하였다.
정상적으로 기능이 작동하지만 서로 다른 두프레임의 밝기 차이가 심한경우 검출률이 낮은 한계점을 보였다.
해당 문제를 해결하기 위해서는 추가적인 전처리 과정이 필요하다.</span>
