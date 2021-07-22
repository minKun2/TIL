# STS 설치 방법
## (1) STS 설치
### 압축 풀기 


#### cmd창(ConEmu)열어서 압축 풀기
![jar파일 압축 풀기](https://user-images.githubusercontent.com/80079066/116949136-53853500-acbc-11eb-8a17-f75b3f59e7de.PNG)
- jar 파일은 이런식으로 압축을 풀지 않고 일반적인 압축 해제로 풀게 되면 오류가 발생할 수 있으니 꼭!!! cmd 창의 명령어로 압축해제
- 압축해제 명령어 : jar -xvf [파일명].jar

- 압축해제 완료 상태 폴더
![sts파일압축해제완료](https://user-images.githubusercontent.com/80079066/116949924-8a5c4a80-acbe-11eb-92fb-30e42685a084.PNG)


#### workspace 생성
![workspace생성](https://user-images.githubusercontent.com/80079066/116949244-a101a200-acbc-11eb-8d06-2bd6247b81e6.PNG)

#### workspace 지정
![workspace지정](https://user-images.githubusercontent.com/80079066/116949381-f473f000-acbc-11eb-8cf5-31b17e9a644e.PNG)
- 압축을 해제한 폴더에 workspace를 같이 만들어 주고, sts의 workspace도 해당 폴더에서 런치할수 있도록 했습니다. 다른 곳에 만들어서 실행하니
해결되지 않는 오류가 발생하는 경우가 생겨 같이 만들어주고 꼭 workspace 지정 후 해당 폴더에 `.metadata`라는 파일이 잘 생성이 되었는지 확인해 줍시다.

## (2) lombok 설치
sts 설치가 끝나면 바로 닫아주시고, lombok을 설치해 보겠습니다.

lombok을 설치하는 이유는 아래에 링크를 통해 확인하시면 됩니다.

[lombok설치 이유](https://mangkyu.tistory.com/78)

![lombok저장](https://user-images.githubusercontent.com/80079066/116949671-ebcfe980-acbd-11eb-9e5e-f1fca65eb9f8.PNG)

위 사진처럼 다운로드 받은 lombok.jar 파일을 아까 압축을 해제한 STS폴더로 복사하여 가져옵니다.
그리고 클릭을 하면 아래와 같은 화면이 나옵니다.

![lombok설치1](https://user-images.githubusercontent.com/80079066/116949903-7c0e2e80-acbe-11eb-8c2e-750384e8f8ff.PNG)

`Specify location`버튼을 클릭하여 lombok을 설치할 STS.exe 파일을 선택해 줍니다.

![lombok설치2](https://user-images.githubusercontent.com/80079066/116949893-74e72080-acbe-11eb-936a-397b196173c2.PNG)

`Install/Update`버튼을 클릭하여 설치해주면 lombok설치가 끝이 납니다.

여기서 주의해야할 점은 반드시 STS의 압축을 해제한 폴더 안에 가져와야합니다. 그렇지 않으면 lombok파일이 제대로 설치되지 않거나 STS를 실행했을 때, 오류가 날 수 있습니다.

## (3) JDK 설치 

jdk를 설치를 하셨으면, 아마 C:\Program Files\Java 위치에 폴더가 이렇게 생성됩니다.

![jdk설정1](https://user-images.githubusercontent.com/80079066/116951407-b679ca80-acc2-11eb-91ef-114b28b2e348.PNG)

#### jdk 환경변수 설정
- jdk는 환경변수 설정이 필요합니다. 다음은 환경변수 설정 과정입니다.
 
[jdk 환경변수 설정 이유](https://shinjekim.github.io/java/2020/01/03/%EC%9E%90%EB%B0%94-%ED%99%98%EA%B2%BD%EB%B3%80%EC%88%98-%EC%84%A4%EC%A0%95%EC%9D%B4-%ED%95%84%EC%9A%94%ED%95%9C-%EC%9D%B4%EC%9C%A0/)

- 내PC에서 마우스 우클릭 후 속성 or 제어판 -> 고급 시스템 설정 -> 고급 -> 환경변수 
![jdk설정2](https://user-images.githubusercontent.com/80079066/116951411-b8dc2480-acc2-11eb-927a-1addc2df5fda.PNG)

- 새로만들기 클릭 -> 변수 이름( 대부분 JAVA_HOME으로 설정 )과 변수 값 설정 ( 변수 값은 JDK가 설치된 경로를 입력 ) 
![jdk설정3](https://user-images.githubusercontent.com/80079066/116951416-baa5e800-acc2-11eb-9fb7-b80aad837edf.PNG)

- 환경변수를 만든 후 PATH 변수에도 추가 시켜주어야 합니다. PATH 클릭 -> 편집 -> 새로만들기 -> %JAVA_HOME%\bin 추가 
![jdk설정4](https://user-images.githubusercontent.com/80079066/116951420-bbd71500-acc2-11eb-8d87-a872e9ee7d58.PNG)

- 이렇게 되면 JDK 환경 변수 설정이 완료되었습니다. 그럼 잘 적용이 되었는지 확인해보겠습니다. cmd 창을 열고 'java -version'을 입력합니다.

![jdk설정마무리](https://user-images.githubusercontent.com/80079066/116951424-bed20580-acc2-11eb-98af-e02ce5648f7a.PNG)

- 위 사진처럼 JDK버전이 정상적으로 확인되면 JDK 설치가 완료 된 것입니다.

## (4) STS에서 JDK 설정
- 이클립스(STS)는 기본적으로 JDK가 아닌 JRE를 이용해 실행되기 때문에 프로젝트 진행 시 Lombok 라이브러리 등의 사용에 지장이 있을 수 있습니다. 이러한 문제를 미리 막기 위해서 디폴트로 사용할 자바 실행 환경을 JDK로 설정해 줍니다. 

이클립스(STS)에 설정하는 방법은 두가지가 있습니다. 

### 첫번째 STS 안에서 직접 설정

- STS 실행 -> [Window] -> [Preferences] -> [Java] -> [Installed JREs]

![image](https://user-images.githubusercontent.com/80079066/117406962-d4586100-af48-11eb-9491-7bd82e2e2877.png)

[Add] -> [Standard VM] -> [Next]

![STS JDK 설정 1](https://user-images.githubusercontent.com/80079066/117592727-b0796300-b174-11eb-9629-4395674a9fdd.PNG)

[Directory] -> (JDK가 있는 폴더로 가서 폴더를 클릭 후) [폴더 선택]

![STS JDK 설정 2](https://user-images.githubusercontent.com/80079066/117592730-b111f980-b174-11eb-8327-ec9ab9ee05d4.PNG)

아래와 같이 뜨게 되면 정상적으로 적용 된 것 [Finish] 클릭

![STS JDK 설정 3](https://user-images.githubusercontent.com/80079066/117592733-b2432680-b174-11eb-95a5-e03f0ee80470.PNG)

이렇게 하면 STS의 기본 설치가 끝이 났습니다.
