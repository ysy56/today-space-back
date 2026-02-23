# 🏠 오늘의 공간 (Today's Space)
> **인테리어 이커머스 및 공간 정보 큐레이션 서비스** > *과거 팀 프로젝트를 기반으로, 9개월간의 **측량/GIS 실무 경험**을 녹여내어 **위치 기반 서비스(LBS)**로 고도화 중인 백엔드 리팩토링 저장소입니다.*

## 📝 Project Overview
* **프로젝트 성격**: 인테리어 상품 판매 및 사용자 위치 기반 쇼룸 안내 플랫폼
* **주요 기능**: 상품 조회 및 결제, Redis 활용 인기 상품 랭킹, 위치 기반 근처 시공 업체 찾기
* **개발 인원**: 1인 (Back-end Refactoring)
* **진행 기간**: 2024.07 - 2024.08 (초기 개발) / **2026.02 - 진행 중 (리팩토링)**

## 🛠 Tech Stack (Refactored)
* **Language/Framework**: Java 17, Spring Boot 3.x
* **Database**: **PostgreSQL (PostGIS)**, MongoDB, Redis
* **Infrastructure**: Docker, Jenkins, AWS(S3, EC2), **Cloudtype (배포)**
* **GIS Tool**: QGIS (데이터 정제 및 가공)

## 🚀 Refactoring & Deep Dive (2026.02 ~)
*과거의 기술적 부채를 해결하고, 실무에서 얻은 데이터 전문성을 결합하고 있습니다.*

### 1. GIS 실무 지식의 결합 (**QGIS ↔ PostGIS**)
* **Problem**: 초기 설계 시 위경도 좌표를 단순 텍스트로 저장하여 정밀한 거리 계산 및 공간 검색에 한계가 있었음.
* **Improvement**: 9개월간의 측량 데이터 구축 경험을 바탕으로 **PostGIS** 도입.
* **Focus**: 공간 인덱싱을 활용하여 '사용자 반경 내 쇼룸/시공업체 탐색' 기능의 **쿼리 성능 최적화**.

### 2. 백엔드 아키텍처 및 보안 고도화
* **Security**: 소스코드 내 노출된 민감 정보(API Key, DB PW)를 **환경 변수**로 분리하여 보안 취약점 해결.
* **Modernization**: Java 17 및 Spring Boot 3.x 마이그레이션으로 최신 환경 대응.
* **Infrastructure**: 유지 비용 최적화를 위해 기존 인프라를 **Cloudtype**으로 이전 및 자동화.

## 🏗 System Architecture


### 1. 설계 문서
* [초기 설계 문서(ERD/API)]([https://github.com/today-space/today-space-back](https://github.com/today-space/today-space-back?tab=readme-ov-file#-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%EB%82%B4%EC%9A%A9))
* [리팩토링 설계 문서(PostGIS 반영)](준비 중)

## 💡 Retrospective: 왜 리팩토링인가?
> "측량 현장에서 QGIS로 데이터를 구축하며 데이터의 정확성이 서비스에 미치는 영향을 몸소 배웠습니다. 과거의 '오늘의 공간'은 단순히 기능을 구현하는 데 급급했지만, 이제는 **현장의 데이터 감각**을 **백엔드 기술**과 결합하여 더 가치 있는 서비스를 만들 수 있음을 증명하고자 합니다."

## 🔗 관련 문서 및 링크
* **[Live Demo]** (준비 중)
* **[Troubleshooting Blog]** (링크 예정)
