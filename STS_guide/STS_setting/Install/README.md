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

#### lombok 설치
sts 설치가 끝나면 바로 닫아주시고, lombok을 설치해 보겠습니다.

lombok을 설치하는 이유는 아래에 링크를 통해 확인하시면 됩니다.
[lombok설치 이유]()

![lombok저장](https://user-images.githubusercontent.com/80079066/116949671-ebcfe980-acbd-11eb-9e5e-f1fca65eb9f8.PNG)

위 사진처럼 다운로드 받은 lombok.jar 파일을 아까 압축을 해제한 STS폴더로 복사하여 가져옵니다.
그리고 클릭을 하면 아래와 같은 화면이 나옵니다.

![lombok설치1](https://user-images.githubusercontent.com/80079066/116949903-7c0e2e80-acbe-11eb-8c2e-750384e8f8ff.PNG)

`Specify location`버튼을 클릭하여 lombok을 설치할 STS.exe 파일을 선택해 줍니다.

![lombok설치2](https://user-images.githubusercontent.com/80079066/116949893-74e72080-acbe-11eb-936a-397b196173c2.PNG)

`Install/Update`버튼을 클릭하여 설치해주면 lombok설치가 끝이 납니다.

여기서 주의해야할 점은 반드시 STS의 압축을 해제한 폴더 안에 가져와야합니다. 그렇지 않으면 lombok파일이 제대로 설치되지 않거나 STS를 실행했을 때, 오류가 날 수 있습니다.

