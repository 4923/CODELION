## js에서는 변수를 `var name = value;` 로 표현한다.

### ES6: 최신 JS 문법 에서는...
```js
// 변수 선언
let name = value;
const name = value;
```

데이터의 특징, 자료형에 따라 변수가 달라지는데  
js의 기본 자료형은 아래와 같다.

1. 문자열: String
    - Python과 마찬가지로 큰따옴표와 작은따옴표 모두 사용할 수 있다.
2. 숫자: int, float
    - integer: 정수형
    - float: 실수형
3. 참 또는 거짓을 표현하는 boolean: bool
    - true, false

자료형은 데이터 앞에 `typeof`를 입력하여 파악한다.
```js
var name = "문자"
document.write(name)    // 문자
document.write(typeof name)    // string
```
![variable in js](https://user-images.githubusercontent.com/60145951/152651450-e3750aba-dc2c-4386-a43f-55b983169ec9.png)

