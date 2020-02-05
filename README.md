# todolist-springboot2
스프링부트2를 이용하여 todo-list 웹을 제작

실행환경
---
~~~
Gradle: 4.10.2 
~~~

Gradle Downgrade 방법
---

IntelliJ의 경우 Gradle의 default 버전이 5버전이기 때문에, 'gradle-wrapper.properties' 파일에서 버전 확인 요망<br> 
gradlew 파일 마우스 우클릭 -> Open in Terminal 클릭 -> 터미널에 아래의 명령어 입력후 실행 
~~~
./gradlew wrapper --gradle-version 4.10.2
~~~



의존성 추가
--- 
~~~
    compile('org.springframework.boot:spring-boot-starter-web')
    compile('org.projectlombok:lombok')
    compile('org.springframework.boot:spring-boot-starter-data-jpa')
    compile('org.springframework.boot:spring-boot-starter-mustache')
    compile('com.h2database:h2')

    compile('org.springframework.boot:spring-boot-starter-oauth2-client')
    compile('org.springframework.session:spring-session-jdbc')

    compile("org.mariadb.jdbc:mariadb-java-client")

    testCompile('org.springframework.boot:spring-boot-starter-test')
    testCompile("org.springframework.security:spring-security-test")
    implementation 'org.springframework.boot:spring-boot-starter-security'
~~~




## 버그들
1. gradle 버전이 5 버전일 경우 ROMBOK 라이브러리를 찾지 못하는 오류가 발생합니다<br>
-> gradle을 다운그레이드 함으로서 오류를 방지합니다.
