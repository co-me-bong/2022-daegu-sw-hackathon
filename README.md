# 실시간 객체 인식을 통한 도로 위 포트홀 문제 해결 시스템

## 0. 팀명: 코메봉

- 신찬규 (팀장) : 2020111854
- 이지성: 2022112038
- 이현우: 2022113203
- 장민기: 2020114267

## 1. 제출 세션 및 주제

- 자유 세션 - 대구 지역 구성원의 삶을 윤택하게 하는 SW 개발
- 운전자의 안전을 위한 웅덩이 탐지 댕댕이, **웅댕이 🐶**: 운전자의 안전을 위한 포트홀 탐지 운전 보조 어플리케이션

## 2. 프로젝트 한 줄 설명

실시간 객체 인식을 통한 도로 위 포트홀 문제 해결 시스템

## 3. 프로젝트 설명

### 3-1. 프로젝트 개요

"포트홀"이란 지반의 침하로 생기는 싱크홀과 달리 아스팔트 도로면에 생기는 땅꺼짐 현상을 말한다. 대구의 많은 도로에 포트홀이 생기지만, 빠른 조치가 힘들기 때문에 생긴 상태로 남겨진 포트홀이 많다. 최근 차량 통행이 많은 국채보상로에 포트홀이 생겼으나, 빠른 조치가 되지않아 운전자들의 안전이 위협됐던 일이 있다. 또한, 이번 8월에 발생한 서울의 폭우로 인해 굉장히 많은 포트홀이 생성되었는데, 그러한 포트홀들 때문에 서울 노량진에서는 버스의 차제가 옆으로 기울어 전복될 수 있는 상황도 겪었으며, 충북 청주 중부고속도로 하행선에서는 포트홀로 인해 차량 20여대의 타이어가 터지거나 하부가 파손되기도 하는 등 포트홀이 도로에서 예상치 못한 곳에서 나올 수 있으며 자칫 전복사고로도 이어질 수 있는 위험한 현상인 것을 알 수 있다. 해당 프로젝트에서는 그러한 포트홀을 탐지하는 어플리케이션을 제작하고, 향후 포트홀로 발생할 수 있는 도로 위 사고를 막고자 한다.

### 3-2. 향후 연구 방향

현재는 해당 기술의 가장 빠른 배포를 위해 iOS 어플리케이션으로 제작 했으나 향후 더 많은 데이터셋을 학습 시켜 더 정확한 결과를 도출 할 수 있도록 하며, 대부분의 자동차에 설치된 블랙박스에 해당 기술을 접목 시킬 예정이다.

### 3-3. 시행 착오

YOLO v5m 모델의 학습을 완료했으며, iOS 어플리케이션 또한 제작 완료 했으나 iOS와 YOLO v5m을 연결하는 과정에서 모델이 제대로 로딩되지 않는 버그가 발생했습니다. 시연 영상은 이 프로젝트에 대한 개요 설명과, 포트홀이 있는 유튜브 영상을 처리한 결과임을 양해 부탁드립니다.

<div></div>
참고 문헌

- [윤관식, 「방치된 포트홀에 뿔난 시민」, 경북일보, 2018.07.10](http://kyongbuk.co.kr/news/articleView.html?idxno=1031628)
- [경찰청, 「도로 위의 지뢰 ‘포트홀’ 대처법은?」, 대한민국 정책브리핑, 2022.08.12](https://www.korea.kr/news/visualNewsView.do?newsId=148904684)
- [곽민구, 「‘도로 위 지뢰’ 포트홀 사고 잇따라…발생 원인과 대처 방법은?」, 인터넷신문위원회, 2022.08.15](https://www.thedailypost.kr/news/articleView.html?idxno=88643)

## 4. 프로젝트에 활용된 기술

### **4-1. 인공지능**

- YOLO v5m 모델을 이용한 실시간 객체 인식 기술 사용
- YOLO는 You Only Look Once의 줄임말로, 현재 객체 인식에 가장 많이 사용되는 모델

**4-1-1. 학습 데이터**

- 도로의 포트홀을 탐지하기 위해 아래의 데이터를 이용함.
  - [https://public.roboflow.com/object-detection/pothole](https://public.roboflow.com/object-detection/pothole)
  - `pothole`
    <p align="center">
        <img src="https://user-images.githubusercontent.com/52674782/192130988-9cdfb14d-4838-41b4-a83f-d406c56b5b48.png">
    </p>

**4-1-2. 학습 결과**

<p align="center">
    <img src="https://user-images.githubusercontent.com/52674782/192130579-76c2b70c-2338-4365-b5ab-a2d938cfb177.png" width="45%">
    <img src="https://user-images.githubusercontent.com/52674782/192130580-f5513601-27fe-455d-9b31-f08133bd4dcc.png" width="45%">
</p>

<p align="center">
    <img src="https://user-images.githubusercontent.com/52674782/192130582-5818f4da-ca2f-48d2-b550-33007948b4f6.png" width="45%">
    <img src="https://user-images.githubusercontent.com/52674782/192130583-56dfd587-52ed-4aa2-bec3-72372b641175.png" width="45%">
</p>

<p align="center">
    <img src="https://user-images.githubusercontent.com/52674782/192130584-34e45d95-d73b-4907-858a-cc5f3be400ab.png" width="45%">
    <img src="https://user-images.githubusercontent.com/52674782/192130585-d7aa9859-b723-4090-a663-00170d7c8b79.png" width="45%">
</p>

<p align="center">
    <img src="https://user-images.githubusercontent.com/52674782/192130480-a1af6972-1995-43cc-943f-179e2ea2026b.jpg">
</p>

### **4-2. iOS 어플리케이션**

- Swift를 이용해 iOS 어플리케이션 제작
- Xcode Storyboard를 이용해 UI/UX 제작
- LibTorch-Lite를 이용해 어플리케이션과 YOLO v5m 모델 연결

<p align="center">
    <img src="https://user-images.githubusercontent.com/52674782/192131042-ac3c305a-c1e4-4e87-89b4-ff3885e4906f.png" width="45%">
    <img src="https://user-images.githubusercontent.com/52674782/192131044-9b94403d-fdce-4a8b-a0c4-b28d6c9bb6ba.png" width="45%">
</p>

## 5. 시연 영상

<a href="https://www.youtube.com/watch?v=fPe1LlsrCaI">유튜브 시연 영상</a>

- 00:00 코드 시연
- 00:05 영상 시작
- 00:09 포트홀 출몰 (인식 완료)
