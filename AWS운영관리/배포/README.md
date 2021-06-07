# API Server 배포하기

### Git에서 Pull 받기 (소스트리 이용가능)

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
     
      
    
