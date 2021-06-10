# API Server & BO(BackOffice) AWS 배포

## API Server 배포하기


  ### 1️⃣ Intellij에서 BizApi Pull 받기!
  
    - [Project] -> [Get from VCS] 클릭
    
![사진1](https://user-images.githubusercontent.com/80079066/121302598-e73dc700-c934-11eb-8754-8f381eab981c.png)
 
    - [URL] => Git에서 HTTP 주소 복사
    - [Durectory] => 프로젝트를 Clone할 디렉토리 설정 (아무것도 없이 비워져 있어야 함)
 
![사진2](https://user-images.githubusercontent.com/80079066/121302599-e7d65d80-c934-11eb-9d7c-1ceb592cb73d.png)
   
    - 맨 오늘쪽에 [Maven] -> [프로젝트 상위 폴더] -> [Lifecycle] -> [package]에 올려두고 refresh 클릭
    
  ### 2️⃣ BizApi를 run build! 
    
![사진 3](https://user-images.githubusercontent.com/80079066/121302595-e73dc700-c934-11eb-89ad-5e8b3c408d39.png)

    - [File] -> [Projcet Structure] 클릭
    
![사진4](https://user-images.githubusercontent.com/80079066/121302601-e7d65d80-c934-11eb-8b7c-69cd694a561e.png)
  
    - [Artifacts] -> [+] -> [Jar] -> [From modules with dependencies]클릭 
  
![사진5](https://user-images.githubusercontent.com/80079066/121302591-e5740380-c934-11eb-8f36-a2aac2fad623.png)
  
    - [Main Class]의 폴더 버튼 클릭 후 운영서버가 될 클래스 선택 ( 제 프로젝트는 가운데에 있어서 가운데를 선택했습니다 )
    
![사진6](https://user-images.githubusercontent.com/80079066/121302592-e6a53080-c934-11eb-8595-0c3654d2d2b5.png)

    - 다시 맨 오늘쪽에 [Maven] -> [프로젝트 상위 폴더] -> [Lifecycle] -> [package]에 올려두고 ▶️ [Run Maven Build] 클릭하면 스냅샷 생성
    
![사진7](https://user-images.githubusercontent.com/80079066/121302593-e6a53080-c934-11eb-8e67-8a8db78d6282.png)
  
  ### 3️⃣ 스냅샷 교체 (운영서버 교체 배포)
  
  
![putty filezila](https://user-images.githubusercontent.com/80079066/121303038-882c8200-c935-11eb-9025-32f723f28cbb.png)
  
    - Putty와 fileZila를 띄워줍니다.
      - Putty 운영서버_A 클릭 후 open
      - filezila 운영서버_A 클릭 후 open
        [api폴더] -> [스냅샷 확인]
    
    - Putty 창에서 다음과 같이 명령어 입력
    
      💻 login as : [ID 입력]
      
      💻 ls       : 현재 있는 폴더의 폴더 및 파일 확인
      
      💻 cd [폴더명] : 폴더로 이동
      
      💻 ps -efc | grep java : java가 포함된 파일 나열
        ➡️ 현재 돌아가고 있는 서버들이 나옴 
            ➡️ 현재 프로젝트에는 Api, 검색엔진, 리뷰엔진이 돌아가고 있음 ( 프로젝트마다 엔진 갯수와 구성이 다름 )
            
      💻 kill -9 [서버의 넘버 입력] : 운영을 종료할 서버의 넘버를 입력  
        ➡️ 제가 바꿀 서버는 bizApi서버이니 해당 서버의 넘버를 입력하여 종료시켜줌
        
      💻 ps -efc | grep java : 서버가 죽었는지 확인
      
      💻 ls : 현재 스냅샷 확인
      
      fileZila에서 스냅샷 삭제 후

      💻 ls : 스냅샷 삭제 확인

      fileZila에 아까 위에서 빌드한 스냅샷 복사 붙혀넣기

      💻 ls : 복사한 스냅샷 확인
      
      💻 nohup java -jar [스냅샷파일] --spring.profiles.acitve=prd & : 붙혀놓은 스냅샷으로 API 서버 재가동
        ➡️ 운영 서버 A,B는 'prd' / 개발 서버는 'dev' 입력!
        
      💻 ps -efc | grep java : 서버 가동 확인
      
## BackOffice 배포하기

### Git 에서 클론 받기 
➡️ Api Server clone 받는 것과 동일하게 프로젝트 클론 받습니다.

### build 하기
➡️ intellij 내에서 Terminal open

      명령어
      1. yarn add node-sass@[버전]
      2. yarn run build
      
   끝! 👏 쉽죠?

### AWS Server에 배포

➡️ 로그인

![AWS 로그인](https://user-images.githubusercontent.com/80079066/121450824-6be12180-c9d7-11eb-988c-b26fc8151539.png)

➡️ S3 스토리지 이동 및 배포할 객체 선택

![AWS S3 이동](https://user-images.githubusercontent.com/80079066/121450822-6aaff480-c9d7-11eb-8c57-c39a80b26fdd.png)

➡️ 객체 선택 후 [업로드] 선택 후 프로젝트 폴더 [project folder] -> [build]

![build](https://user-images.githubusercontent.com/80079066/121450826-6c79b800-c9d7-11eb-807c-acf769e34ade.png)

➡️ [build]에 있던 파일을 붙여넣기 후 업로드 클릭 기다리면... 성공! 👏

![업로드 서옥ㅇ](https://user-images.githubusercontent.com/80079066/121450829-6c79b800-c9d7-11eb-8622-dc27eeef2882.png)





