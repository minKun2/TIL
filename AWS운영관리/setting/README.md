![aws로고](https://user-images.githubusercontent.com/80079066/120594527-04c5e900-c47c-11eb-807b-64d8831f2bc7.png)

# AWS 운영 관리
⚠️ **주의사항** ⚠️
 - 오늘 다루어볼 주제는 직접 AWS를 설계 한 사람이 아닌 사람으로써, 다른분으로부터 인수인계를 받아 오로지 제가 알고 있는 부분만 다루어질 부분이기 때문에 많이 부족할 수 있는 점 가만하여 봐주시길 바랍니다! 추가적으로 구축 설계 혹은 deep한 운영 관리에 추가할 사항이 있다면 점차 보완해 나갈 예정입니다! 🙇

---------------------------------------------------------------
---------------------------------------------------------------

## 프로젝트의 AWS 구성

---------------------------------------------------------------
---------------------------------------------------------------

## 운영서버 및 개발서버 배포 방법

---------------------------------------------------------------

### 필요 파일
   #### Putty + Puttygen
   ![putty로고](https://user-images.githubusercontent.com/80079066/120595259-093ed180-c47d-11eb-9811-5a866e53742e.png)
   [Putty 다운로드](https://www.putty.org/)
   
   #### ftp (전 fileZilla를 사용하였습니다)
   ![filezilla](https://user-images.githubusercontent.com/80079066/120595254-08a63b00-c47d-11eb-9c62-2adafe80236e.png)
   
   [FileZilla 다운로드](https://filezilla-project.org/)
   
   #### intelliJ / VScode 같은 툴 
   ![인텔리제이](https://user-images.githubusercontent.com/80079066/120595260-09d76800-c47d-11eb-97a5-7f0f83d01ecd.png)
   
   [인텔리제이 다운로드](https://www.jetbrains.com/ko-kr/idea/download/#section=windows)
   
   (전 intellij 구매해서 사용하고 있습니다 - 대학교를 다니는 학생분들은 학교에 따라 무료 혹은 저렴하게 이용하실 수 있으니 homepage 참고 부탁드립니다! ps.나도 학생할래.. 😢 )

--------------------------------------------------------------------

### pem파일 -> ppk파일로 변환하기
   
   #### Puttygen 접속 왼쪽 위 [Conversions] 클릭
   
![ppk 변환 1](https://user-images.githubusercontent.com/80079066/120597228-c5999700-c47f-11eb-8e01-89ab6a11ffec.png)

   #### [Import Key] 클릭
   
![ppk 변환 2](https://user-images.githubusercontent.com/80079066/120597232-c6cac400-c47f-11eb-99fc-faec688ec5f3.png)

   #### (파일명).pem 파일 선택

![ppk 변환 3](https://user-images.githubusercontent.com/80079066/120597234-c6cac400-c47f-11eb-8596-cb61b7c7d3f1.png)

   #### 아래와 같은 화면으로 바뀌면 아무것도 건드리지 않은 상태에서 [Save private key] 클릭

![ppk 변환 4](https://user-images.githubusercontent.com/80079066/120597236-c7635a80-c47f-11eb-8497-6f93e8b0a07e.png)

   #### 클릭하면 파일명만 지어주면 끝!!! 🎬
   
![ppk 변환 5](https://user-images.githubusercontent.com/80079066/120597239-c7635a80-c47f-11eb-8ddc-d87d4b51d288.png)

-----------------------------------------------------------
------------------------------------------------------------
### Putty에 서버 등록하기
- 이번 프로젝트는 운영서버가 2개(A,B) 개발 서버가 1개 이기 때문에 3개의 서버를 등록해주겠습니다!

  #### Putty 접속 후 [HostName(or IP address] 칸에 서버 IP 입력 [Port]칸에 포트 번호 입력
  #### Connection Type = SSH 선택 (기본값이라 안건드려도 됩니다.
  #### [Saved Sessions] 아래에 서버 이름 입력(헷갈리지 않도록만 입력하면 됩니다!)후 [Save]
   - 저의 경우 아래와 같이 저장하여 사용하였습니다. 
     - [운영서버 A] "(앱 or 프로젝트 이름)_op_A"
     - [운영서버 B] "(앱 or 프로젝트 이름)_op_B"
     - [개발서버] "(앱 or 프로젝트 이름)_dev"
  
  [사진]
  
  #### [Save] 후 좌측에 [Connection] -> [SSH] -> [Auth] 클릭
  
  [사진]
  
  #### 맨 하단에 [Private key for authentication]에서 아까 만든 .ppk 파일 찾아서 업로딩!
  
  [사진]
  
  #### 그 후 [Open] 클릭 
  
  [사진]
  
  #### 이 과정을 총 세번 (운영서버 2개 / 개발서버 1개) 진행 해 줍니다! * 개발 서버 .ppk 파일은 따로 위에서 만들어줘야 합니다! 운영서버 .ppk 같이 안씀! *
 








