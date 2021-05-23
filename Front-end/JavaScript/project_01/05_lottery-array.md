## JS의 배열 (Array)
> 하나의 변수 안에 여러 개의 값을 넣는다.

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
- 배열의 끝에서 일어나는 일들
    1. 추가
        - `.push()` : python의 `.append()`
        - 마지막 값 추가
        - python의 list 처럼 자료형이 달라도 입력할 수 있다.
            ![push diffrent data type](https://user-images.githubusercontent.com/60145951/152653861-bdd16786-38d7-43a1-a67d-d1f1681809aa.png)
    2. 삭제
        - `.pop()`
- 배열의 앞에서 일어나는 일들

3. 기타
- 요소 전체 출력
alert(lotto);
- 길이
alert(lotto.length);
- trailing 쉼표로 끝날 수 있다.

### 참고
- [코어 자바스크립트 / 자료구조와 자료형](https://ko.javascript.info/array)