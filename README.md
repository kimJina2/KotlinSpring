<!-- PROJECT SHIELDS -->
# BE5_FinalPJ
### 🏆 프로젝트 소개
기본적인 CRUD프레임워크 기능과 DB의 select/insert/update/delete의 베이직한 기능을 Kotlin으로 작업하였으며,
도서관리에서 사용되는 사용자기능,책대출/반납에 관한 프로젝트입니다.
>**개발기간 : 2023.09.30 ~ 2023.10.04**

<!-- PROJECT IMG -->
### ✅ 산출물
> 
| 메인 | 
| :------------: |
| ![image](https://github.com/kimJina2/KotlinSpring/assets/147501094/9c2f69d0-5d3a-48d1-bd02-de212259f91b) | 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PROJECT IDE -->
## 🛠 프로젝트 스택
* 개발환경 : JAVA 11
* IDE: IntelliJ
* Build: Gradle
* Framework: Spring-Boot 2.6.8
* Database: MYSQL
* 사용기술
  - SpringBoot
  - Spring Web
  - Kotlin
  - JUnit
  - Spring Data JPA

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PROJECT TABLE -->
## ⚖ 테이블 설계
**1. 책**
```
CREATE TABLE book
(
    id         BIGINT PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(50),
    type       VARCHAR(255),
);
```
**2. 유저**
```
CREATE TABLE user
(
    id         BIGINT PRIMARY KEY AUTO_INCREMENT,
    age        INT,
    name       VARCHAR(255)
);
```
**3. 관리**
```
CREATE TABLE user_history
(
    id          INT PRIMARY KEY AUTO_INCREMENT,
    book_name   VARCHAR(255),
    status      INT,
    user_id     BIGINT

);
ALTER TABLE user_history
(
    add
    FOREIGN KEY (user_id)
);
```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PROJECT API -->
## 📌 API 명세서
- 사용자조회/수정/삭제<br>
POST /user <br>
PUT /user <br>
DELETE /user
- 도서 등록/대출/반납<br>
POST /book <br>
POST /book/loan <br>
PUT /book/return

<p align="right">(<a href="#readme-top">back to top</a>)</p>


