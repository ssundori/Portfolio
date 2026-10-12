# 공유니폼 (GongUniform)

> 선수 추천과 IoT 자판기를 결합한 야구 유니폼 대여 서비스

**캡스톤디자인 팀 프로젝트**

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
- Raspberry Pi와 모터를 이용한 **유니폼 자판 구현**
