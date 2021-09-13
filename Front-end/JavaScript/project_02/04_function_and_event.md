## 드디어!
> 함수와 이벤트를 이용하면 실시간 반영이 가능하다!

### 함수
```js
function foo() { }
```

- 글자가 입력될 때 마다 총 글자수를 입력해야 하므로
- 글자를 입력할 때 함수를 호출해보도록 하자

```js
function counter() {
    var content = document.getElementById('jasoseol').value;
    document.getElementById('count').innerHTML = '(' + content.length + '/200)';
};
counter();
```

### 이벤트?
- 키보드를 누르면 일어나는 일에 대해 알아보자.
    1. 마우스 클릭 또는 키보드로 입력
    2. 값이 변화
    3. 페이지 로딩
    4. 이하 브라우저에서 작업

- 이렇게 사용자와의 상호작용을 **이벤트**라고 말하며, 
    - e.g.) `onkeydown` : 키보드가 눌릴 때
- 이벤트가 발생할 때 일어나게 하는 작업 등을 **이벤트 핸들링**이라고 말한다.
    - 이벤트 핸들링은 문자열이다. 여기서는 함수를 입력하자.

```js
// 틀 
<textarea event-example='event-handling'></textarea>
```

### 실시간 반영!
> js가 실시간으로 사용자와 상호작용 할 수 있다는건 이런 '이벤트' 개념 덕분이다.
![onkeydown-event](https://user-images.githubusercontent.com/60145951/152693299-58cfa364-be95-4196-9cc2-52fd2f22b56c.png)
브라우저 텍스트 입력 상자에 한 줄을 추가해봤다.