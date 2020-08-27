---
title : "서로 다른 두 프레임 홍채 패턴 비교"
date: 2020-07-01-18:00
categories:
- Opencv

tags:
- Skew Deviation
---

---

# 비교 이미지
![이미지](/images/opencv/Skew Deviation/1.png)
---

서로다른 두 프레임의 홍채를 촬영, 홍채 패턴을 분석하기 위해 Linear Polar를 사용하여
두 프레임의 홍채를 일직선으로 Polar시킨다. 이후 SIFT를 사용하여 두 홍채의 패턴을 비교한다.

---
