![리액트 Hooks](https://user-images.githubusercontent.com/80079066/118940470-b567bf00-b98b-11eb-80db-8bbf331a05dd.jpeg)

# React Hooks 이란? :interrobang:
- 훅(Hooks)은 함수형 component에서도 class형 컴포넌트의 기능 또는 여러 component에서 사용할 수 없던 다양한 기능을 사용할 수 있기 해주는 기능이다.

### Hooks 의 장점 :+1:
 1. 작성할 코드가 줄어들어 가독성이 좋아진다.
 2. 정적 타입 언어로 타입 정의가 쉽다.
 3. 재사용이 가능한 로직을 쉽게 만들 수 있다.

### Hooks의 종류와 사용 방법
#### 1. useState 란? :interrobang:
 - 가장 기본적인 Hook 함수형 component에서 가변적인 상태를 지니고 있게 해준다. 상태를 관리해줘야 할 일이 생긴다면 useState를 사용하면 된다.
#### 1-1. useState 사용 방법
 - Count.js 파일을 src에 만든다.
 
 ```
 import React, { useState } from 'react'; // useState 선언
 
 const Count = () => {
  const [value, setValue] = useState(0);
  return (
   <div>
    <p>
     카운터 값 : <b>{value}</b> 
    </p>
    <button onClick={() => setValue(value + 1)}> 1 증가 </button>
    <button onClick={() => setValue(value - 1)}> 1 감소 </button>
   </div>
  );
 };
 
 export defualt Count;
 ```
 
 
