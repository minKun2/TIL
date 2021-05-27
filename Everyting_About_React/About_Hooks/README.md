![리액트 Hooks](https://user-images.githubusercontent.com/80079066/118940470-b567bf00-b98b-11eb-80db-8bbf331a05dd.jpeg)

# React Hooks 이란? :interrobang:
> 훅(Hooks)은 함수형 component에서도 class형 컴포넌트의 기능 또는 여러 component에서 사용할 수 없던 다양한 기능을 사용할 수 있기 해주는 기능입니다.

### Hooks 의 장점 :+1:
> 1. 작성할 코드가 줄어들어 가독성이 좋아진다.
> 2. 정적 타입 언어로 타입 정의가 쉽다.
> 3. 재사용이 가능한 로직을 쉽게 만들 수 있다.

### Hooks의 종류와 사용 방법
> 1. useState
> 2. useEffect
> 3. useRef
> 4. useMemo

#### 1. useState 란? :interrobang:
 - 가장 기본적인 Hook 함수형 component에서 가변적인 상태를 지니고 있게 해준다. 상태를 관리해줘야 할 일이 생긴다면 useState를 사용하면 됩니다.
#### useState 사용 방법
##### useState 이용
 - Count.js 파일을 src에 만들어줍니다.
 
 ```js
 import React, { useState } from 'react'; // useState 선언
 
 const Count = () => {
  const [value, setValue] = useState(0);
  return (
   <div>
    <p>
     카운터 값 : <b>{value}</b> 
    </p>
    <button onClick={() => setValue(value + 1)}> 1 증가 </button> // 버튼을 누를 때마다 useState(0)의 값이 1씩 증가
    <button onClick={() => setValue(value - 1)}> 1 감소 </button> // 버튼을 누를 때마다 useState(0)의 값이 1씩 감소
   </div>
  );
 };
 
 export defualt Count;
 ```
 
 - App.js

```js
import React from 'react';

const App = () => {
 return <Count />;
};

export defualt App;
```

 - 위의 코드를 입력해보세요. 그리고 cmd 창에서 `yarn start`를 입력하여 실행시켜 줍니다.
 
 ![리액트 useState 결과값](https://user-images.githubusercontent.com/80079066/118945892-db439280-b990-11eb-9d67-7f3e54a70f39.png)

 - 숫자가 증가하거나 감소하면 성공!:clap:

##### useState 여러번 이용해 보기!

- 이번엔 src 안에 Info.js를 만들어 봅시다. 만든 후 아래와 같이 입력해 봅시다.

```js
import React, { useState } from "react";

const Info = () => {
  const [name, setName] = useState("");       // 이름을 입력 받을 useState
  const [adress, setAdress] = useState("");   // 주소를 입력 받을 useState
  const [phoneNm, setPhoneNm] = useState(""); // 전화번호를 입력 받을 useState

  const onChangeName = (e) => {
    setName(e.target.value);                  // 입력할 때 마다 name 값을 변경
  };
  const onChangeadress = (e) => {
    setAdress(e.target.value);                // 입력할 때 마다 adress 값을 변경
  };
  const onChangePhoneNm = (e) => {
    setPhoneNm(e.target.value);               // 입력할 때 마다 phoneNm 값을 변경
  };

  return (
    <div>
      <div>
        <input
          value={name}
          placeholder="성함을 입력해주세요."   //*placeholder : 입력하기 전 음영으로 안내문구 띄우기
          onChange={onChangeName}
        />
        <input
          value={adress}
          placeholder="주소를 입력해주세요."
          onChange={onChangeadress}
        />
        <input
          value={phoneNm}
          placeholder="핸드폰 번호를 입력해주세요."
          onChange={onChangePhoneNm}
        />
      </div>
      <div>
        <div>
          <b>성함 :</b>
          {name}
        </div>
        <div>
          <b>주소 :</b> {adress}
        </div>
        <div>
          <b>핸드폰 번호 :</b> {phoneNm}
        </div>
      </div>
    </div>
  );
};

export default Info;
```

- 아래과 같이 뜨게 된다면 성공!:clap:

![usestate 중복으로 사용하기](https://user-images.githubusercontent.com/80079066/118953669-01b8fc00-b998-11eb-89a8-aa2e7b23f5e5.png)

-----------------------------------------------------------

-----------------------------------------------------------

#### 2. useEffect 란? :interrobang:
 - 페이지가 렌더링한 후 useEffect는 무조건 한번 실행합니다.
 - useEffect에 배열로 지정한 useState 값이 변경이 되면 실행하는 훅입니다.

<b>* useEffect는 렌더링, 변수 값 or 오브젝트가 달라지게 되면, 알아채고 업데이트하는 함수입니다. </b>

#### useEffect 사용법
1. 
> ```javascript
> useEffect (()=>{});
> ```
👉 기본 형태지만, 거의 사용하지 않습니다! Dependency가 없어서 렌더링 할 때 한번, 값이 바뀔때 마다 발생하여 불필요한 실행이 많아짐.
 
2.
> ```javascript
> useEffect (() => {},[])
> ```
👉 렌더링 후 한번만 실행하고 싶을 때, 콜백함수 뒤에 배열을 나타내는 대괄호를 작성합니다. 대괄호 안에 Dependency를 지정합니다.
대괄호 안에 아무런 값이 없으면 렌더링 후 단 한번만 실행되고 다시 실행되지 않습니다.

3.
> ```javascript
> const [naem, setName] = useState();
> useEffect (() => {},[name])
> ```
👉 렌더링 후 배열 안의 변수 값이 변할 때마다 실행합니다. Dependency에 지정된 변수값이 변할 때만 실행합니다.

 
