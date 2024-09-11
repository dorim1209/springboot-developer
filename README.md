# 스프링 부트 3 백엔드 개발자 되기: 자바 편

이 저장소는 [스프링 부트 3 백엔드 개발자 되기: 자바 편](https://product.kyobobook.co.kr/detail/S000212798297) 실습 내용을
포함하고 있습니다.

![image](https://contents.kyobobook.co.kr/sih/fit-in/458x0/pdt/9791191905717.jpg)

## 주요 기능
- 스프링 부트 3 기반 백엔드 프로젝트
- REST API 구현 (CRUD)
- Gradle을 사용한 빌드 구성
- H2 데이터베이스 연동

## 요구 사항
- Java 17 이상
- Gradle 7 이상

## 시작하기

1. 리포지토리 클론:
   ```bash
   git clone git@github.com:dorim1209/springboot-developer.git
   ```
2. 프로젝트 빌드:
   ```bash
   ./gradlew build
   ```
3. 애플리케이션 실행:
   ```bash
   ./gradlew bootRun
   ```
4. 접속
    ```bash
   http://localhost:8080/articles
   ```
<!-- 작성중 -->

## 데이터베이스 설정

<img width="1432" alt="스크린샷 2024-09-11 15 52 58" src="https://github.com/user-attachments/assets/ad95e352-2979-4462-b07f-79f1a33497b5">

- 기본적으로 H2 데이터베이스가 메모리 모드로 설정되어 있습니다.
- H2 콘솔에 접속하려면 다음 URL을 사용하세요:
  ```bash
  http://localhost:8080/h2-console
   ```
- `application.properties`에서 데이터베이스 설정을 확인하고 변경할 수 있습니다:
    ```properties
    spring.datasource.url=jdbc:h2:mem:testdb
    spring.datasource.username=sa 
    spring.h2.console.enabled=true
    ```

## 테스트 실행 방법
1. 테스트 실행:
   ```bash
   ./gradlew test
   ```
2. 테스트 결과 확인:
   - build/reports/tests/test/index.html 파일을 열어 HTML 형식의 테스트 결과를 확인할 수 있습니다.