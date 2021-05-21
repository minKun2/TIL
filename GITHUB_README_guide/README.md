# github readme 작성 가이드

> 깃허브는 마크다운 문법으로 text를 작성할 수 있습니다.

## 📓 마크 다운 이란?

> 일반 텍스트 문서의 양식을 편집하는 문법으로 텍스트에 태그를 이용해 글자에 속성을 주거나, 이미지를 삽입하고 조작하는 일이 가능합니다.

## 📓 마크 다운의 장점

> 1. 문법이 간단해서 읽고 쓰는게 간편함.
>
> 2. 글을 빠르게 작성 가능
>
> 3. 개발자에게 필요한 소스코드 블록 사용가능

## 1. 글씨 크기 변경하여 사용하기


# 제일 큰 텍스트 (제목)

==== 사용하기! (제목)
===================

쓰는 방법 :

```
# 제일 큰 텍스트 (제목) // 1번째 방법
==== 사용하기! (제목) // 2번째 방법
============
```


-----------------------------------------------


## 두번째로 큰 텍스트 (부제목)

부제목 ---- 사용하기! (부제목)
---------------------

쓰는 방법 : 

```
## 두번째로 큰 텍스트 (부제목) // 1번째 방법
부제목 --- 사용하기! (부제목) // 2번째 방법
-------------------
```

-----------------------------------------------

### 세번째로 큰 텍스트

쓰는 방법 : ` ### 세번째로 큰 텍스트`

-----------------------------------------------

#### 네번째로 큰 텍스트

쓰는 방법 : `#### 네번째로 큰 텍스트`

-----------------------------------------------

##### 다섯번째로 큰 텍스트

쓰는 방법  : `###### 다섯번째로 큰 텍스트

-----------------------------------------------

## 2.  GitHub 이모지 사용하기

> emoji 모음 링크 [이모지](https://gist.github.com/rxaviers/7360908)

-----------------------------------------------

## 3. GitHub Stats 사용하기

>
>  `[![Anurag's github stats](https://github-readme-stats.vercel.app/api?username=username)](https://github.com/anuraghazra/github-readme-stats)`
>
> 위에서 username을 수정해서 사용해주면 아래의 모습이 나옵니다.

  [![Anurag's github stats](https://github-readme-stats.vercel.app/api?username=minKun2)](https://github.com/anuraghazra/github-readme-stats)

-----------------------------------------------

## 4. 이미지 삽입하기 🖼️

> 삽입 방법
>
> [Issues] 클릭 후 [new Issues] 
>
> 삽입할 이미지 드래그 앤 드롭 후 변경된 URL 복사

![깃허브 이미지올리기](https://user-images.githubusercontent.com/80079066/119087762-9b3ce800-ba42-11eb-98cc-c0229a1b5530.png)

> 복사 후 README.md에 붙혀넣기!하면 끝이 납니다! 👍

⬇️⬇️⬇️⬇️ 붙혀넣기 한 깃허브 이미지 ⬇️⬇️⬇️⬇️

![깃헙이미지](https://user-images.githubusercontent.com/80079066/119087760-9aa45180-ba42-11eb-9204-a7aed9b6fcac.png)

> 사이즈를 변경하여 이미지 삽입하기
>
> 똑같은 경로로 이미지를 삽입하되 README.md에서 요러케 바꾸어줍니다.
>
> 명령어 1 : `<img src ="https://user-images.githubusercontent.com/80079066/119087760-9aa45180-ba42-11eb-9204-a7aed9b6fcac.png" width="600px" height="600px">`
>
> 명령어 2 : `<img src ="https://user-images.githubusercontent.com/80079066/119087760-9aa45180-ba42-11eb-9204-a7aed9b6fcac.png" width="50%" height="50%">`

⬇️⬇️⬇️⬇️ 명령어 1번 이미지 ⬇️⬇️⬇️⬇️

<img src ="https://user-images.githubusercontent.com/80079066/119087760-9aa45180-ba42-11eb-9204-a7aed9b6fcac.png" width="600px" height="600px">

> px로 직접 크기를 지정해 줍니다.

⬇️⬇️⬇️⬇️ 명령어 2번 이미지 ⬇️⬇️⬇️⬇️

<img src ="https://user-images.githubusercontent.com/80079066/119087760-9aa45180-ba42-11eb-9204-a7aed9b6fcac.png" width="50%" height="50%">

> %로 원래크기의 ~%의 크기로 축소/확대 해줍니다.
