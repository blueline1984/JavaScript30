# JavaScript30

## 01 Drum Kit 22.06.21

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

::before 에 대해서

inherit에 대해

CSS 태그 및 속성
`*` 태그
overflow

vh? em?

cubic-bezier?

background-image:url

p:nth-child(2)

flex: 1;
