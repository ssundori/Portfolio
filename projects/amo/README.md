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

### 1. 여러 쿼리 처리 중 데이터 불일치 방지

데이터 생성·수정·삭제 과정에서는 실제 데이터 변경과 사용자 작업 로그 저장이 함께 수행됩니다.

두 작업 중 하나만 성공할 경우 실제 데이터와 로그의 상태가 달라질 수 있어,
관련 쿼리를 하나의 작업 단위로 처리하도록 **Transaction**을 적용했습니다.

- 데이터 변경 쿼리와 사용자 작업 로그 저장을 하나의 Transaction으로 처리
- 모든 쿼리가 성공하면 `commit`
- 처리 중 오류가 발생하면 `rollback`

이를 통해 일부 쿼리만 반영되는 상황을 방지하고 데이터의 일관성을 유지했습니다.


### 2. 대량 데이터 조회 범위 제한

약 3만 건의 기후·재난 데이터를 조회하는 과정에서
전체 데이터를 한 번에 반환하지 않고 필요한 범위만 조회하도록 **Pagination**을 적용했습니다.

- `page`, `page_size` 기반 조회
- `LIMIT`, `OFFSET`을 사용해 필요한 데이터만 DB에서 조회
- 전체 데이터 수와 현재 페이지 정보를 함께 응답

이를 통해 데이터 관리 화면에서 필요한 범위의 데이터만 전달하도록 구성했습니다.


### 3. Frontend-Backend 간 요청값 기준 통일

프론트엔드 연동 과정에서 선택하지 않은 필터 값이
`""`, `undefined`, `"null"` 등 서로 다른 형태로 전달되면서
백엔드의 조건 처리 결과가 달라지는 문제가 발생했습니다.

백엔드에서는 미선택 값을 `NULL` 기준으로 정규화하고,
프론트엔드에서는 연도와 ID 값을 숫자형으로 전달하도록 요청 형식을 맞췄습니다.

또한 Ranking 결과에서 동일한 재난 유형을 세부적으로 구분하기 어려운 문제는
응답 기준을 `disaster_type`에서 `disaster_subtype`으로 변경해 개선했습니다.

이를 통해 Frontend와 Backend가 동일한 입력·응답 기준으로 동작하도록 정리했습니다.

## 🏗 System Architecture

```text
Climate / Disaster Dataset
        ↓
Python / pandas
Data Preprocessing
        ↓
MySQL Database
        ↓
PHP REST API
├── Aggregation
├── Roll-Up
├── Ranking
├── Windowing
└── CRUD
        ↓
JavaScript Frontend
        ↓
Dashboard / Analysis Results
```text

## 🔗 Repository

[Original Team Repository](https://github.com/ssundori/BigDataApplication_Amo)
