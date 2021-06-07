# API Server & BO(BackOffice) AWS 배포

## API Server 배포하기

### 

  #### 1️⃣ Intellij에서 BizApi Pull 받기!
  
    - [Project] -> [Get from VCS] 클릭
    
  [사진1]
 
    - [URL] => Git에서 HTTP 주소 복사
    - [Durectory] => 프로젝트를 Clone할 디렉토리 설정 (아무것도 없이 비워져 있어야 함)
 
  [사진2]
   
    - 맨 오늘쪽에 [Maven] -> [프로젝트 상위 폴더] -> [Lifecycle] -> [package]에 올려두고 refresh 클릭
    
  #### 2️⃣ BizApi를 run build! 
    
  [사진3] 

    - [File] -> [Projcet Structure] 클릭
    
  [사진4]
  
    - [Artifacts] -> [+] -> [Jar] -> [From modules with dependencies]클릭 
  
  [사진5]
  
    - [Main Class]의 폴더 버튼 클릭 후 운영서버가 될 클래스 선택 ( 제 프로젝트는 가운데에 있어서 가운데를 선택했습니다 )
    
  [사진6]
  
    - 다시 맨 오늘쪽에 [Maven] -> [프로젝트 상위 폴더] -> [Lifecycle] -> [package]에 올려두고 ▶️ [Run Maven Build] 클릭하면 스냅샷 생성
    
  [사진7]
  
  #### 3️⃣ 스냅샷 교체 (운영서버 교체 배포)
  
  
  [putty. filezila]
  
    - Putty와 fileZila를 띄워줍니다.
      - Putty 운영서버_A 클릭 후 open
      - filezila 운영서버_A 클릭 후 open
        [api폴더] -> [스냅샷 확인]
  
  [사진 8]
  
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
      
    
