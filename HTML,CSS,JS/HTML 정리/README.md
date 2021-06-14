[HTML로고]

# HTML이란?

▶️ 제목, 문단, 표, 이미지, 동영상 등의 구조를 정의 하는 언어를 말합니다


## HTML 사용법


### HTML 기본 문법

```html

<div>안녕하세요<div>


<!--- 쉽게 말하면 --->
 
<TAG></TAG>
<TAG>CONTENT</TAG>
<태그>[내용]<태그>

<!---for example--->
 <h1>안녕하세요. 주니어 개발자 김민재입니다.</h1> // h1 : 대주제
 
 <p>안녕하세요! 미래의 풀스택!앱개발자가 될 주니어개발자 김민재입니다!</p> // p : 문단
  
```

▶️ 위의 예제를 나타내보면!!? :

[예제1]

#### 태그는 열리고 닫히는 태그가 하나의 세트를 이룹니다.

### HTML 속성과 값을 입력하는 문법

```html

<!---쉽게 말해 요렇게 써요--->
<TAG 속성="값"></TAG>

<---for example--->
 
<img src="https://heropcode.github.io/GitHub-Responsive/img/logo.svg" alt="GitHub Logo" /> //img는 빈 태그로 따로 닫는 태그가 아닌 맨끝에 /로 닫아준다!

```

▶️ 위의 예제는 ?!

[예시2]

귀여운 GitHub 로고가 나오게됩니다! 👏

### HTML의 문서의 범위

[예시3]

#### HTML의 전체 범위

▶️ <html>은 이 문서의 전체를 말합니다! 
   웹 브라우저가 해석해야할 HTML 문서가 어디서부터 어디까지 인지 알려주는 태그입니다!

▶️ 사용법

```html
<html></html>
```

#### HTML의 정보 범위

▶️ <head>는 웹 브라우저가 해석해야할 문서의 정보 범위를 지정합니다!
   웹 페이지 제목<title>, 웹 페이지 문자 인코딩 방식<meta charset>, 연결할 외부 파일 위치<link rel="" href=""> 등 화면을 구성하기 위한 기본 설정등을 정의합니다!
 
#### HTML의 구조 범위
 
▶️ <body>는 해석해야할 문서의 구조 범위를 지정합니다!
   사용자가 웹 화면을 통해 볼 수 있는 내용의 레이아웃 등을 정의합니다!(로고, 푸터, 버튼, 입력창 등등)
 
#### HTML의 버전 지정

▶️ <!DOCTYPE html>는 일명 DTD로 마크업 언어에서 문서의 형식을 정의합니다!
   총 버전은 현재까지 5가지의 버전이 있으며(1,2,3,4, XTML, 5) 현재는 5를 제일 많이 쓰고 기본값 또한 5로 되어 있습니다. XTML같은 경우 유지 보수 시 볼 수 있습니다.

#### HTML 제목 지정

▶️ 각 브라우저의 사이트 탭의 이름으로 표시됩니다!
 
▶️ 사용법

 ```html
 <html>
  <head>
   <title>GitHub</title>
  </head>
 </html>
````
[타이틀 예시]
 
#### HTML 웹 페이지 정보 입력

▶️ <meta ...>는 웹 페이지에 관한 정보(문자 인코딩 방식, 제작자, 내용 등)을 검색엔진 혹은 브라우저에 제공합니다! (meta 태그는 빈태그!)

▶️ 사용법

```html
<html>
  <head>
    <meta charset="UTF-8" />
    <!--문자 인코딩 방식 설정 (필수로 해주는 것이 좋음)-->
    <meta name="author" content="김민재" />
    <!--제작자-->
    <meta name="discription" content="연습하는 사이트~!" />
    <!--사이트 설명-->
    <title>Github(연습사이트)</title>
  </head>
</html>
```
 
#### HTML에서 외부문서 가져오기

▶️ HTML에서 외부 문서를 가져올 때 사용합니다!

▶️ 사용법
```html
 <html>
  <head>
    <meta charset="UTF-8" />
    <!--문자 인코딩 방식 설정 (필수로 해주는 것이 좋음)-->
    <meta name="author" content="김민재" />
    <!--제작자-->
    <meta name="discription" content="연습하는 사이트~!" />
    <!--사이트 설명-->
    <title>Github(연습사이트)</title>
    <link rel="stylesheet" href="./main.css" />
  </head>
  <body>
    <div class="box"></div>
  </body>
</html>
```

    - link
    - rel = 관계를 나타내줌 (stylesheet, icon 등)
    - href = 위치 지정

 


