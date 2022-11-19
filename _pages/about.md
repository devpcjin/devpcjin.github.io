---
permalink: /about/
title: "About me"
toc: true
toc_sticky: true
toc_label: "About me"
---

# 박철진 (Park Cheoljin)

## 👉 Contact

📞 **Phone.**        010-4517-1765

📧 **Email.**          sgn03077@gmail.com

🔗 **Github.**       [https://github.com/devpcjin](https://github.com/devpcjin)

🔗 **Blog.**           [https://velog.io/@pc_jin](https://velog.io/@pc_jin)

## 👨‍💻 Introduce

- 안녕하세요! **어제보단 오늘, 오늘보단 내일 더 성장**하는 개발자 박철진입니다.
- 단순 코드작성이 아닌 객체지향 설계 원칙을 바탕으로 코드의 효율성과 재사용성을 위해 꾸준히 학습하려고 노력하고 있습니다.
- 목표한 것을 이루기 위해 포기하지 않고 끝까지 최선을 다합니다. 중도 포기하지 않고 목표지점까지 부지런하게 나아갑니다.
- 빠른 실행력을 바탕으로 생각에서 그치지 않고 바로 실행으로 옮깁니다.
- 협업에서 소통의 가치를 중요하게 생각합니다. 주변 사람들과 소통을 통해 정보를 나누고, 더 나은 의견이 있다면 열린 자세로 수용할 준비가 되어있습니다.

## 🔧 Stacks


**Back-End**

- Java 11 / Spring Boot / Spring Data JPA / Gradle
- AWS (EC2, S3, RDS, Code Deloy, SecretsManager 등)

**Database**

- MySQL

**Collaboration & Tools**

- IntelliJ, VS Code
- Git, Github

## 🌱 Projects
### 1. [Crackers](https://github.com/devpcjin/Crackers-JavaSpring)
<details>
<summary></summary>
<div markdown="1">
- 기간 : 2022.06.24 ~ 2022.07.29

**🧑🏼 PROJECT 소개**

> 맛집을 검색해서 저장 및 공유하고 댓글로 소통하는 커뮤니티
> 

**🛠️ 주요기능 및 주요업무**

- 프로젝트 팀장
- 기여한 기능 : 커뮤니티, 맛집 저장 기능 / 배포 인프라 구축
    - 각 Entity 사이의 연관관계 메서드 구현
    - 커뮤니티 페이지 CRUD 구현
        - DTO를 활용하여 유지 보수성 증가
        - @ManyToOne 지연 로딩 사용
        - @Transactional 사용
        - 테이블 사이의 연관관계 복잡성을 해결하기 위해 Entity를 나눠서 관리
    - Github Action과 AWS Code Deploy를 활용한 배포자동화
        - Github Action을 통해 빌드 파일 AWS S3에 업로드
        - Code Deploy를 활용하여 AWS EC2 서버에 배포
        - nginx를 사용하여 포트 포워딩 및 서버 설정
    - 협업
        - Github Project 사용
        - Github Issue 사용
        - 팀 프로젝트 Git branch 전략 제안
        

⚠️ **문제 해결 경험**

- Entity사이의 ManyToMany 관계 해결을 위해 Entity 분리
    - 맛집 Entity와 사용자 Entity로 Community를 표현하기 위해 초기 설계를 ManyToMany로 했지만, 연관관계의 복잡성을 해결하기 위해 맛집 Entity를 Community Entity와 Place Entity로 나눠서 관리
    - 데이터베이스 관점이 아닌 객체 관점에서 유연하게 entity 설계 및 구현
- 회원가입시 중복 검사를 프론트에서 진행하여 보안 문제 발생
    - 프론트엔드에서 관리자 도구로 자바 스크립트를 수정하여 중복 검사를 무시하고 회원가입이 가능해서 보안 문제 발생
    - 정규식을 활용하여 프론트/서버에서 이중으로 중복 검사를 실행해서 보안 문제 해결
- API, DB 정보, OAuth 토큰 등 보안암호 노출 문제 발생
    - AWS Secrets Manager를 활용하여 보안 암호 관리
        
        

🌱 **스킬 및 사용툴**

- Backend : `Java11` `Spring Boot 2.6.9` `Gradle 7.4.1` `Spring Data JPA` `Spring Security` `Thymeleaf`
- Frontend : `JavaScript` `JQuery` `HTML/CSS` `Bootstrap` `Bulma`
- Database : `AWS RDS` `MySQL 8.0.28`
- Infra : `AWS EC2` `AWS S3` `AWS SecretManager` `AWS CodeDeploy`
- CI/CD : `Github Action`
</div>
</details>


---

### 2. [자율주행 RC 카](https://github.com/devpcjin/Capstone-Design-Graduation-Project)
<details>
<summary></summary>
<div markdown="1">

- 기간 : 2019.11.01 ~ 2020.06.30

**🧑🏼 PROJECT 소개**

> 차선을 인식한 자율 주행 및 사물인식을 통한 제어가 가능한 자율주행 RC카
> 

**🛠️ 주요기능 및 주요업무**

- 프로젝트 팀장
- 기여한 기능 : GPS 정보 수집 / 웹서버 구축
    - GPS 정보 수집 및 수집한 데이터 처리
        - `NMEA 0183` 프로토콜을 활용하여 GPS 정보 수집
        - Serial 통신(GPIO 핀)을 활용하여 데이터 전송
        - GPS 정보를 Parsing하여 원하는 데이터 추출하여 사용
    - Google Map API를 활용하여 웹 서버에 차량의 현재위치 표현
        - UDP 통신을 통한 실시간 차량의 현재 위치 표현
        - 비동기 방식 통신을 통해 지도상에 차량의 이동경로 표현
    - 프로젝트 설명을 위한 웹 페이지 구축

⚠️ **문제 해결 경험**

- 주변 조도 값에 따라 차선인식에 영향을 주는 문제 발생
    - 명암 대비로 차선을 구분하고 인식하는 조도, 구름의 양 등 주변 환경에 따라 차선인식 불량이 발생
    - 조도센서를 추가하여 차량 주변의 조도 값에 따라 HSV 값을 조절하여 차선 인식불량 문제 해결
- 웹 서버로 차량의 현재 위치를 표현 할 때 차량의 위치가 변할 때 마다 페이지가 새로고침되는 문제 발생
    - 비동기식 통신 방식을 선택하여 필요한 부분만 불러와 해당 문제를 해결
    

🌱 **스킬 및 사용툴**

- 사용 기자재 : `NVIDIA Jetson AGX Xavier` `Raspberry Pi 4` `GPS module (EM-406A)`
    
    `Python 3.6.9` `C++` 
    
- 사용 소프트웨어
    - Backend : `Python 3.6.9` `C++` `PHP` `Tensorflow Lite` `OpenCV 4.3(Jetson) / OpenCV 4.5 (Rassberry Pi)` `ROS melodic` `Jetpack 4.3`
    - Frontend : `HTML/CSS` `Bootstrap`

</div>
</details>

## 📃 Papers

**Implementation of Dynamic HSV Adjusting Method for Lane Detection**

- 2022 24th ICACT

## 🎖️ Awards

**2021 캡스톤 디자인 졸업작품전 대상**

- *수상 기관 : 충북대학교 정보통신공학부*

## 📚 Education

**스파르타 내일배움 캠프 클라우드 엔지니어 트랙 3기 수료 (2022.04 ~ 2022.08)**

- Java
- Spring Boot
    - Spring MVC 패턴
    - Spring Data JPA 기초
- AWS Cloud
    - AWS EC2
    - AWS S3
    - AWS ElasticBeanstalk

**Bachelor's Degree in Telecommunication Engineering (2016.03 ~ 2022.02)**

*2022, Chungbuk National University, Cheong-Ju, Republic of Korea.*