# 공유니폼 (GongUniform)

> 선수 추천과 IoT 자판기를 결합한 야구 유니폼 대여 서비스

**캡스톤디자인 팀 프로젝트**  
**개발 기간:** 2023.09 ~ 2024.06

## 📌 Project Overview

공유니폼은 높은 야구 유니폼 가격과 다양한 선수·디자인 선택으로 인한 고민을 줄이기 위해
기획한 야구 유니폼 대여 서비스입니다.

Android 앱에서 선수와 유니폼을 선택하고 대여 과정을 진행할 수 있도록 구성했으며,
Spring Boot와 MySQL을 이용해 회원·유니폼·주문 데이터를 관리했습니다.

또한 사용자 취향과 선수 경기 기록을 활용한 추천 알고리즘을 구현하고,
Raspberry Pi와 모터를 이용해 유니폼을 배출하는 IoT 자판기를 제작했습니다.

## 🛠 Tech Stack

**Android**
- Java
- XML
- Google Maps API
- ZXing

**Backend**
- Spring Boot
- MySQL
- REST API

**Recommendation**
- Python
- pandas
- NumPy
- scikit-learn

**IoT**
- Raspberry Pi
- Python
- RPi.GPIO

**Infrastructure**
- AWS

## 🔍 Main Features

- 선수·유니폼·사이즈를 선택하는 **유니폼 대여 흐름 구성**
- 대여 정보 확인을 위한 **QR 화면**
- Google Maps API를 이용한 **대여 자판기 및 반납 위치 지도**
- 주문 내역을 확인할 수 있는 **마이페이지**
- 사용자 설문 응답을 활용한 **선수 추천**
- 사용자 간 유사도를 활용한 **유니폼 추천**
- 선수 경기 기록을 활용한 **선수 추천 모델**
- Spring Boot / MySQL 기반 **회원·유니폼·주문 데이터 관리**
- Raspberry Pi와 모터를 이용한 **유니폼 자판기 구현**

## 👤 My Contribution

**Role: Backend / Recommendation / IoT**

### Android
- 선수·유니폼·사이즈 선택을 위한 대여 화면 및 화면 전환 구현
- 대여 과정에 필요한 QR, 지도, 마이페이지 등 서비스 화면 구성

### Backend
- Spring Boot와 MySQL을 이용한 서버 및 데이터베이스 구성
- 회원, 유니폼, 주문 데이터를 관리하기 위한 API 구현
- 앱에서 사용할 데이터를 조회·저장할 수 있도록 Backend 구조 설계

### Recommendation
- 사용자 설문 응답을 활용한 선수 추천 알고리즘 구현
- 사용자 간 유사도를 활용한 유니폼 추천 알고리즘 구현
- 선수 경기 기록 데이터를 전처리하고 회귀 모델을 학습해 선수 추천 모델 구현
- OPS, wOBA, 장타율, 출루율, 안타 등 주요 feature를 활용해 모델 성능 평가

### IoT
- Raspberry Pi와 모터를 이용한 유니폼 배출 장치 제작
- RPi.GPIO를 이용한 모터 제어 코드 구현 및 배출 동작 테스트
