# Amo

> 기후·자연재해 데이터를 기반으로 다양한 분석 기능을 제공하는 웹 서비스

**빅데이터응용 팀 프로젝트**  
**개발 기간:** 2025.09 ~ 2025.12

## 📌 Project Overview

기후 및 자연재해 관련 데이터를 데이터베이스에 구축하고,  
사용자가 웹 환경에서 데이터를 조회·분석할 수 있도록 구현한 프로젝트입니다.

자연재해, 기온, 해수면 온도 이상, CO₂ 농도 등의 데이터를 활용하여  
Aggregation, Roll-Up, Ranking, Windowing 분석 기능을 제공하며,  
로그인 기반의 데이터 조회 및 관리 기능을 구현했습니다.

## 🛠 Tech Stack

**Frontend**
- JavaScript
- HTML / CSS
- Chart.js

**Backend**
- PHP

**Database**
- MySQL

**Data Processing**
- Python
- pandas

## 🔍 Main Features

- 자연재해 데이터 **Aggregation 분석**
- 계층형 데이터 **Roll-Up 분석**
- 국가·재해 유형별 **Ranking 분석**
- 기온·해수면 온도·CO₂ 데이터 **Windowing / 이동평균 분석**
- 데이터 조회 및 **CRUD**
- 로그인 및 세션 기반 사용자 인증
- 분석 결과 웹 시각화

## 👤 My Contribution

**Role: Backend Developer & Team Leader**

### Data Engineering
- 기후·재난 데이터 전처리 및 MySQL 적재
- 대량 데이터 초기 적재를 위한 Bulk Insert SQL 작성
- 데이터베이스 초기화 및 삭제 스크립트 작성

### Backend API
- 국가별 피해 규모를 기준으로 상위 10개 결과를 조회하는 **Ranking API 구현**
- 기온, 해수면 온도 이상(SST), CO₂ 데이터를 대상으로 기간별 값과 이동평균을 계산하는 **Windowing API 구현**
- 데이터 조회·생성·수정·삭제를 위한 **CRUD API 구현**
- 로그인 여부를 검사하여 데이터 관리 기능 접근을 제한하는 **인증 처리 구현**

### Team Leader
- 백엔드 및 데이터 처리 작업을 담당하며 팀 프로젝트 개발 진행 관리

## 🔧 Problem Solving

> 작성 예정

## 🔗 Repository

[Original Team Repository](https://github.com/ssundori/BigDataApplication_Amo)
