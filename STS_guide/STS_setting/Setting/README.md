# STS 프로젝트 세팅하기
## (1) 이미 프로젝트가 저장이 되어 있는 경우의 세팅
- STS 접속 후 [File]->[import]클릭

![파일있음1](https://user-images.githubusercontent.com/80079066/118419372-bc29d400-b6f6-11eb-8582-b197ac830fa8.png)

- [Maven] -> [Existing Maven Projects] 클릭

![파일있음2](https://user-images.githubusercontent.com/80079066/118424780-cb168380-b702-11eb-8a8c-257058da3915.png)

- [Browser] -> (해당 프로젝트가 있는 폴더 선택) -> [폴더 선택]

![파일있음3](https://user-images.githubusercontent.com/80079066/118424762-c520a280-b702-11eb-9e13-6c7da0686b54.png)

- [/pom.xml ~~ 프로젝트 파일 체크 확인] -> [Finsh]

![파일있음4](https://user-images.githubusercontent.com/80079066/118424784-cfdb3780-b702-11eb-8d30-5b84b026bb2a.png)

## (2) GIT에서 직접 프로젝트를 받는 경우

- github나 gitlab에서 직접 프로젝트를 받아 오는 경우 일단 gitlab or github 접속 후 해당 프로젝트 레포지토리로 이동
- 프로젝트 레포지토리에서 [clone] -> [HTTP]URL 복사

![git으로 세팅 1](https://user-images.githubusercontent.com/80079066/118426178-b38cca00-b705-11eb-940e-66bf199f7a25.png)

- [File] -> [import] -> [Git] -> [Projects from Git(with smart import)] 클릭

![git으로 세팅](https://user-images.githubusercontent.com/80079066/118426185-b687ba80-b705-11eb-8bf5-e5282250bd0e.png)

- [URL]칸에 아까 복사한 HTTP클론 URL 복사 -> 자동으로 HOST/Repository path 입력됨.

![git으로 세팅2](https://user-images.githubusercontent.com/80079066/118426193-b982ab00-b705-11eb-8f7a-b43ea4d37811.png)

- User ID / PW 입력 (gitlab의 경우)

![git으로 세팅3](https://user-images.githubusercontent.com/80079066/118426200-bedff580-b705-11eb-8758-67233c65fd09.png)

- 프로젝트 적용 확인 후 Finsih 클릭

### <span colior = "red" >주의 사항</span> 

git으로 클론을 받아 프로젝트를 진행할 경우 Lombok,JDK를 먼저 설정하지 말고 프로젝트를 먼저 클론 받은 후 STS를 종료 / Lombok과 JDK를 설정 후 다시 접속하여 아래의 공통 세팅을 진행하는 것이 좋습니다.(저장할 폴더에 아무것도 없어야 저장이 되기 때문에)


## (3) 공통 세팅 순서 
