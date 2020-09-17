---
title: 마이크로프로세서 기말 프로젝트
date: 2019-12-30-18:00
categories:
- Microprocessor

tags:
- Microprocessor
- Arduino
---

---
# 슬라이드1
![이미지](/images/microprocessor/1.JPG)
---
# 슬라이드2
![이미지](/images/microprocessor/2.JPG)
---
# 슬라이드3
![이미지](/images/microprocessor/3.JPG)
---
# 슬라이드4
![이미지](/images/microprocessor/4.JPG)
---
# 슬라이드5
![이미지](/images/microprocessor/5.JPG)
---
# 슬라이드6
![이미지](/images/microprocessor/6.JPG)
---
# 슬라이드7
![이미지](/images/microprocessor/7.JPG)
---
# 슬라이드8
![이미지](/images/microprocessor/8.JPG)
---
# 슬라이드9
![이미지](/images/microprocessor/9.JPG)
---
# 슬라이드10
![이미지](/images/microprocessor/10.JPG)
---
# 슬라이드11
![이미지](/images/microprocessor/11.JPG)
---
# 슬라이드12
![이미지](/images/microprocessor/12.JPG)
---
# 슬라이드13
![이미지](/images/microprocessor/13.JPG)
---
# 슬라이드14
![이미지](/images/microprocessor/14.JPG)
---
# 슬라이드15
![이미지](/images/microprocessor/15.JPG)
---
# 슬라이드16
![이미지](/images/microprocessor/16.JPG)
---
# 슬라이드17
![이미지](/images/microprocessor/17.JPG)
---
# 슬라이드18
![이미지](/images/microprocessor/18.JPG)
---
# 슬라이드19
![이미지](/images/microprocessor/19.JPG)
---
# 슬라이드20
![이미지](/images/microprocessor/20.JPG)
---
# 슬라이드21
![이미지](/images/microprocessor/21.JPG)
---
# 슬라이드22
![이미지](/images/microprocessor/22.JPG)
---
# 슬라이드23
![이미지](/images/microprocessor/23.JPG)
---
# 슬라이드24
![이미지](/images/microprocessor/24.JPG)
---
# 슬라이드25
![이미지](/images/microprocessor/25.JPG)
---
# 슬라이드26
![이미지](/images/microprocessor/26.JPG)
---
# 슬라이드27
![이미지](/images/microprocessor/27.JPG)
---
# 슬라이드28
![이미지](/images/microprocessor/28.JPG)
---
# 슬라이드29
![이미지](/images/microprocessor/29.JPG)
---
# 슬라이드30
![이미지](/images/microprocessor/30.JPG)
---
# 슬라이드31
![이미지](/images/microprocessor/31.JPG)
---
# 슬라이드32
![이미지](/images/microprocessor/32.JPG)
---
# 슬라이드33
![이미지](/images/microprocessor/33.JPG)
---
# 슬라이드34
![이미지](/images/microprocessor/34.JPG)
---

---
# 자동제어 (풍속)
<iframe width="1280" height="721" src="https://www.youtube.com/embed/YWd-LDVEwOw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---

# 자동제어 (온도)
<iframe width="1280" height="721" src="https://www.youtube.com/embed/CyCPhvwOQ-k" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---

# 자동제어 (광량)
<iframe width="1280" height="721" src="https://www.youtube.com/embed/Wki6MNqOFZ8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---

# 수동제어 (제어 올림)
<iframe width="1280" height="721" src="https://www.youtube.com/embed/mL3tyXFHYHw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---

# 수동제어 (제어 내림)
<iframe width="1280" height="721" src="https://www.youtube.com/embed/tuOFsle_7kI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---

# 물분사
<iframe width="1280" height="721" src="https://www.youtube.com/embed/aZ3qnMpKUDc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---


<div class="share-button">
  <span>다운로드</span>
  <a href="https://drive.google.com/file/d/1nr3PdIogaGr5HWGEOqTo_zxa7Rexrg1Y/view?usp=sharing" >다운로드 시작</a>
</div>
---

<style>
.share-button {
  widith: 280px;
  height: 80px;
  background: #dfe6e9;
  border-radius: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0 50px;
  overflow: hidden;
  position: relative;
  cursor: pointer;
  transition: .3s linear;
}
.share-button:hover{
  transform: scale(1.1);
}
.share-button span{
  position: absolute;
  width: 100%;
  height: 100%;
  background: #2d3436;
  color: #f1f1f1;
  text-align: center;
  line-height: 80px;
  z-index: 999;
  transition: .6s linear;
  border-radius: 40px;

}
.share-button:hover span{
  transform: translateX(-100%);
  transition-delay: .3s;
}
.share-button a {
  flex: 1;
  font-size: 26px;
  margin-right: 20px;
  color: #2d3436;
  text-align: center;
  transform: translateX(-100%);
  opacity: 0;
  transition: .3s linear;
}
.share-button:hover a {
  opacity: 1;
  transform: translateX(0);
}
.share-button a:nth-of-type(1){
  transition-delay: 1s;
}
.share-button a:nth-of-type(2){
  transition-delay: .8s;
}
.share-button a:nth-of-type(3){
  transition-delay: .6s;
}
.share-button a:nth-of-type(4){
  transition-delay: .4s;
}
</style>
