## JS의 배열 (Array)
> 순서가 있는 collection을 저장할 때 사용한다.

```js
/* 선언 */
var array = new Array();    // 또는
var array2 = [];    // 이렇게 빈 배열을 선언하지만 필수는 아니다.

/* EXAMPLE */
var lotto = [1, 2, 3, 4, 5];    // python의 list처럼 대괄호를 사용한다.
document.write(lotto[1]);    // index는 0부터 시작하므로 1이 아닌 2다.
```

### 배열 조작
> Python의 Deque와 유사하다.

> python의 list 처럼 요소의 자료형에 구애받지 않는다.
![push diffrent data type](https://user-images.githubusercontent.com/60145951/152653861-bdd16786-38d7-43a1-a67d-d1f1681809aa.png)

- 배열의 끝에서 일어나는 일들
    1. 추가
        - 마지막 값 추가
        - `.push()` : python의 `.append()`
    2. 삭제
        - 마지막 값 추출: 마지막 값을 제거하고 그 값을 반환한다.
        - `.pop()` : python의 `.pop()`
- 배열의 앞에서 일어나는 일들: 비교적 느리다.
    1. 추가
        - 첫번째 위치에 값을 추가
        - `.unshift` : python으로 구현한 dequeue의 `.appendleft()`
        - 여러개를 한번에 추가할 수 있다.
    2. 삭제
        - 첫 값 추출: 첫번째 값을 제거하고 그 값을 반환한다.
        - `.shift()` : python으로 구현한 dequeue의 `.popleft()`
        - 여러개를 한번에 삭제할 수 있다.

- 기타
    - 요소 전체 출력: `alert(lotto);`
        |code|alert array|
        |:-:|:-:|
        |![alert code](https://user-images.githubusercontent.com/60145951/152656050-05092c3c-d7d3-46e7-802f-d7dad8b07dbb.png)|![alert array](https://user-images.githubusercontent.com/60145951/152656015-d2a628ed-4d23-4746-bd3b-f0324e13059c.png)|
    - 길이: `alert(lotto.length);`
    - trailing: array의 마지막 요소는 쉼표로 끝날 수 있다.

### 참고
- [코어 자바스크립트 / 자료구조와 자료형](https://ko.javascript.info/array)