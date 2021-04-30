STS(Spring Tool Suits) 가이드북 제작 개요( STS GuidebooK Production Overview )
===========
제작 목적( Purpose of production )
-----------
- 프로젝트에서 사용하는 API서버를 STS을 사용하여 제작하게 됨.<p> The API server used in the project is produced using STS.
- Error 사항 soultion을 저장하여 빠르게 해결, 업무효율성을 높이기 위함.<p> Save error problems to quickly fix them and increase work efficiency.
- STS 툴에 대한 이해도를 높이기 위함. <p>To improve understanding of STS tools.

필요 파일 설치 및 경로 ( Install required files & Installation path )
-----------
- STS 설치 <p> : 홈페이지에서 운영체제에 맞게 설치 ( URL : <https://spring.io/tools> )
- LomBok 설치 <p> : 홈페이지에서 설치 ( URL : <https://projectlombok.org/download> )
  - LomBok 설치 이유 <p> : java와 같은 언어를 이용해 개발을 하다보면 기계적으로 작성해야하는 코드들이 있는데, 이 코드들을 자동화 하여 코드를 짧게 다이어트 하도록 하는 java 필수 라이브러리이다. <p> 
    - LomBok의 장점 
      - 1 어노테이션 기반의 코드 자동 생성을 위한 생산성 향상
        - 어노테이션이란?<p> : 본래 주석이란 듯으로, 인터페이슬르 기반으로 한 문법. 주석과는 역할이 다르지만 주석처럼 코드에 달아 클래스에 특별한 의미를 부여하거나 기능을 주입할 수 있음. 해석되는 시점 또한 정할 수 있음.
          - 어노테이션의 종류
            - 1). `built-in-annotation` : 어노테이션에 대한 정보를 나타내기 위한 어노테이션 
              - 1)-1. @Override        : 메서드 앞에서만 붙이며, 현재 메서드가 슈퍼클래스의 메소드를 오버라이드한 메소드임을 컴파일러에게 명시 ( 오타 잡아줌 )
              - 1)-2. @Deprecated      : 차후 버전에 지원되지 않을 수 있기 때문에 더 이상 사용되지 말아야할 메소드를 명시
              - 1)-3. @SupressWarning  : 프로그래머의 의도를 컴파일러에게 전달하여 경고 제거
              - 1)-4. @Functionallnterface : 컴파일러에게 다음의 인터페이스는 함수형 인터페이스라는 것을 알림. 오버라이딩 어노테이션과 같은 이유로 사용
