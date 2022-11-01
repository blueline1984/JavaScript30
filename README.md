# JavaScript30

## Completed List

- [01 Drum Kit](#01-drum-kit) 22.06.21
- [02 JS and CSS Clock](#02-js-and-css-clock) 22.06.22
- [03 CSS Variables](#03-css-variables) 22.06.23
- [04 Array Cardio Day 1](#04-array-cardio-day-1)
- [05 Flex Panel Gallery](#05-flex-panel-gallery) 22.08.06
- [07 Array Cardio Day 2](#06-array-cardio-day-2) 22.10.28
- [08 Fun with HTML5 Canvas](#07-fun-with-html5-canvas) 22.10.31


## 01 Drum Kit

<img width="1894" alt="Drum kit backgroud" src="https://user-images.githubusercontent.com/97525377/174822161-a0b70c4d-8b48-4420-9464-26a9c2396422.png">

### What I Learned

```
1. HTML data attribute
2. <audio> tag
3. document.addEventListener("eventType", callback);
4. transitionend event
5. document.querySelector("a[target]");
6. element.classList
```

## 02 JS and CSS Clock 22.06.22

## 03 CSS Variables 22.06.23

![CSS Variables](https://user-images.githubusercontent.com/97525377/175243447-7dda0f1f-cfb5-4590-a045-2c45bbb36fa2.gif)

### What I Learned

```
1. how to use css variables with JS
2. input tag range type
3. this in script function
```

## 04 Array Cardio Day 1

### What I Learned

Array Method

```
1. Array.prototype.filter
- 각 요소들을 순회하며 true를 반환하면 요소를 유지하고, false를 반환하면 버린다
- 유지된 요소들을 새로운 배열에 담아 반환한다(기존 배열 변화 x)

2. Array.prototype.map
- 각 요소들을 순회하며 각각의 요소들에 주어진 함수를 실행한 결과를 모아 반환한다
- 새로운 배열에 담아 반환한다(기존 배열 변화 x)

3. Array.prototype.sort
- 배열의 요소들을 정렬한 후 그 배열을 반환한다
- 기존 배열을 변경하여 반환한다(기존 배열 변화에 유의!)
- compareFunction(optional)이 주어지지 않는 경우, 요소를 문자열로 변환하여 유니 코드 코드 포인트 순서로 문자열 비교하여 정렬한다
- compareFunction(optional)이 주어지는 경우, 해당 함수의 반환값에 따라 정렬한다
- compareFunction(a, b) 함수가 -1 반환할 경우, a를 b보다 a가 b보다 먼저 정렬되고,
1을 반환할 경우, b가 a보다 먼저 정렬된다(0일 경우, 변경하지 않고 다른 요소로 넘어간다)

4. Array.prototype.reduce
- 배열의 각 요소에 대해 reducer 함수를 실행하고, 하나의 결과값을 반환한다(누적값)
- reducer 함수의 경우 4개의 인자를 갖는다
  - accumulator(누적값)
    reducer 함수가 처음 호출되면 initialValue를 제공한 경우에는 initialValue를 값으로 한다
  - currentValue(현재값)
  - currentIndex(현재 인덱스)
  - array(원본 배열)
- initialValue
  reducer 함수 최초 호출시 첫번째 인수에 제공하는 값
```

## 05 Flex Panel Gallery

### 1. CSS 가상요소와 가상클래스

- CSS 가상 요소는 선택자로 선택한 요소의 뒤에 붙여 표기하는 미리 약속된 키워드를 일컫는다.

- 콜론(:) 2개를 연달아 붙이는 것으로 가상요소를 나타낸다. ex) `::before`

- 가상 클래스는 콜론(:) 1개로 나타낸다. ex) `*:before`

- `::before`, `::after` 가상 요소는 HTML 태그, JavaScript 없이도 HTML 페이지 안에 콘텐츠, 또는 디자인 요소를 추가할 수 있는 특별한 기능을 한다.
  - `::before`
    요소 내용 앞쪽에 새로운 내용 추가
  - `::after`
    요소 내용 끝에 새로운 내용 추가

### 2. CSS inherit

- 해당 요소의 부모 요소의 속성 값을 상속받아 사용한다.

```
html {
  box-sizing: border-box;
  background: #ffc600;
  font-family: "helvetica neue";
  font-size: 20px;
  font-weight: 200;
}

*,
*:before,
*:after {
  box-sizing: inherit; //box-sizing: border-box
}

//부모의 box-sizing 속성 값을 상속
```

### 3. `*` 선택자 (전체 선택자)

- 모든 형태의 요소를 선택한다.

- 브라우저에 부하를 줄 수 있기때문에 사용에 유의한다.

### 4. overflow 속성

- overflow 속성은 요소의 content가 해당 영역에 들어가기에 큰 경우, 해당 content를 자르거나 scrollbar를 추가하여 처리할 수 있다.

- height(높이 속성값)을 갖고 있는 블럭 요소에만 적용 가능하다.

- `visible`, `hidden`, `scorll`, `auto` 등의 속성을 갖는다.

### 5. CSS Units - Relative Lengths

- CSS 길이 속성에 사용한다. `width, margin, padding, font-size` 등.

- em, rem

  - em: 해당 요소의 크기를 해당 요소의 부모 요소를 기준으로 정한다.
  - rem: 해당 요소의 크기를 최상단의 root 요소를 기준으로 정한다.

  ```
  //em
  div {
    font-size: 30px;
  }

  span {
    font-size: 0.5em;
  }

  //...

  <div>The font-size of the div element is set to 30px.
    <span>The span element inside the div element has a font-size of 0.5em, which equals to 0.5x30 = 15px</span>.
  </div>


  //rem
  html {
    font-size:16px;
  }

  div {
    font-size: 3rem;
  }

  //...

  <div>The font-size of this div element is 3rem.</div>
  ```

- vh, vw
  - viewport height, viewport width를 의미한다. (viewport: 웹페이지가 사용자에게 보여지는 영역)
  - 브라우저 화면 전체의 높이, 너비를 100vh, 100vw로 한다.
  - 이와 마찬가지로 살펴보면, 50vw는 전체 화면 너비의 50%, 1vh는 전체화면 높이의 1% 이다.
  - viewport의 크기가 변하면 그에 따라 요소의 길이가 변한다.(반응형)

### 6. A:nth-child(N)

- 부모 요소안의 <A> 태그의 N번째 요소를 가리킨다.

- 예제의 경우는 p:nth-child(2) 이므로 클래스가 panel인 태그 즉, <div> 태그의 자식요소 중 <p>태그의 2번째 요소를 가리킨다.

### 7. classList

- classList 속성은 해당 요소의 CSS class name을 배열에 담아(유사배열객체) 반환하고 DOMTokenList를 반환한다.
  <img width="487" alt="스크린샷 2022-08-06 오후 11 05 22" src="https://user-images.githubusercontent.com/97525377/183252536-c8b736c0-b74f-4044-88fd-d7a52c3fff13.png">

### 8. HTML DOMTokenList

<img width="629" alt="스크린샷 2022-08-06 오후 11 00 47" src="https://user-images.githubusercontent.com/97525377/183252168-b9d6c94a-e670-4e4e-886e-f1bf46142252.png">
  출처: https://www.w3schools.com/jsref/dom_obj_html_domtokenlist.asp

### 9. addEventListne에서의 this

- event.currentTarget(해당 이벤트가 발생한 요소)을 가리킨다.

```
 <div class="panels">
    <div class="panel panel1">
      <p>Hey</p>
      <p>Let's</p>
      <p>Dance</p>
    </div>
    <div class="panel panel2">
      <p>Give</p>
      <p>Take</p>
      <p>Receive</p>
    </div>
    <div class="panel panel3">
      <p>Experience</p>
      <p>It</p>
      <p>Today</p>
    </div>
    <div class="panel panel4">
      <p>Give</p>
      <p>All</p>
      <p>You can</p>
    </div>
    <div class="panel panel5">
      <p>Life</p>
      <p>In</p>
      <p>Motion</p>
    </div>
</div>

<script>
function openToggle() {
  this.classList.toggle("open"); // this는 각각의 <div class="panel"> 태그를 가리킴
}

panels.forEach((panel) => panel.addEventListener("click", openToggle));
</script>
```

## 06 Type Ahead 22.08.10

css
inset
nth-child(even)
transform: perspective, rotateX..translateY(2px) scale(1.001);


## 07 Array Cardio Day 2 22.10.28
- `Array.prototype.some()`
  배열 안의 어떤 요소라도(하나라도) 주어진 판별 함수를 통과하는지 확인하고 통과하는 요소가 하나라도 있다면 true, 하나도 없다면 false를 반환합니다.

- `Array.prototype.every()`
  배열 안의 모든 요소가 주어진 판별 함수를 통과하는지 확인하고 통과할 경우 true, 그렇지 않을 경우에는 false를 반환합니다.

- `Array.prototype.find()`
  주어진 판별 함수를 통과하는 배열의 첫 번째 요소의 값을 반환합니다. 통과하는 요소가 하나도 없다면 undefined를 반환합니다.
  
- `Array.prototype.findIndex()`
  주어진 판별 함수를 만족하는 배열의 첫 번째 요소의 인덱스를 반환합니다. 만족하는 요소가 하나도 없다면 -1을 반환합니다.


## 08 Fun with HTML5 Canvas

### What I Learned
- `coordinates`
  1. clientX, clientY
  스크롤 여부와 관계없이 사용자에게 보여지는 브라우저 페이지를 기준으로 좌표를 표시합니다. 스크롤 여부와 관계가 없다는 말은 사용자가 현재 보는 화면이 페이지 상단이 되고 그 지점의 X, Y 좌표를 0으로 설정한다는 뜻입니다.
  `clientX`: 브라우저 페이지 상단을 0을 기준으로 X 좌표를 반환합니다.
  `clientY`: 브라우저 페이지 상단을 0을 기준으로 Y 좌표를 반환합니다.

  2. pageX, pageY
  `clientX, clientY`와는 달리, 현재 사용자에게 보여지는 브라우저 페이지가 기준이 아닌 해당 문서(document)를 기준으로 X, Y 좌표를 반환합니다. 즉, 스크롤이 발생할지라도 좌표 기준은 해당 문서의 상단으로 변하지 않습니다.

  3. offsetX, offsetY
  특정 요소(element)를 기준으로 특정 지점의 좌표를 반환합니다.

  4. screenX, screenY
  모니터를 기준으로 X, Y 좌표를 반환합니다.

- `canvas`
  1. `querySelector`를 이용하여 canvas 요소의 `getContext()` 메서드를 이용합니다. `getContext()` 메서드는 캔버스의 드로잉 컨텍스트 객체를 반환합니다.
  ```
  const canvas = document.querySelector("#draw");
  const ctx = canvas.getContext("2d");
  ```
  2. ctx를 이용하여 다양한 설정이 가능합니다.
  3. `globalCompositeOperation` 프로퍼티를 이용하여 겹치는 부분에 대한 설정이 가능합니다.
  4. 파라미터로 `2d`, `webgl`, `webgl2`, `bitmaprenderer`를 받습니다.
