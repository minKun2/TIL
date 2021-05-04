# STS 설치 방법
## (1) STS 설치
### 압축 풀기 


#### cmd창(ConEmu)열어서 압축 풀기
![jar파일 압축 풀기](https://user-images.githubusercontent.com/80079066/116949136-53853500-acbc-11eb-8a17-f75b3f59e7de.PNG)
- jar 파일은 이런식으로 압축을 풀지 않고 일반적인 압축 해제로 풀게 되면 오류가 발생할 수 있으니 꼭!!! cmd 창의 명령어로 압축해제
- 압축해제 명령어 : jar -xvf [파일명].jar

#### workspace 생성
![workspace생성](https://user-images.githubusercontent.com/80079066/116949244-a101a200-acbc-11eb-8d06-2bd6247b81e6.PNG)

#### workspace 지정
![workspace지정](https://user-images.githubusercontent.com/80079066/116949381-f473f000-acbc-11eb-8cf5-31b17e9a644e.PNG)
- 압축을 해제한 폴더에 workspace를 같이 만들어 주고, sts의 workspace도 해당 폴더에서 런치할수 있도록 했습니다. 다른 곳에 만들어서 실행하니
해결되지 않는 오류가 발생하는 경우가 생겨 같이 만들어주고 꼭 workspace 지정 후 해당 폴더에 `.metadata`라는 파일이 잘 생성이 되었는지 확인해 줍시다.

