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

## 그런데 `ES6`은 뭐지?
> 파이썬이 익숙하니 비교해보자

|JS|Py|description|
|:-|:-|:-|
|const name=value;| <s>CONSTANT?</s> |상수. const는 객체와 함께 사용할 때를 제외하고는 변경 불가능하다. 반면 파이썬에는 값을 고정하는 변수가 없다. 명시적으로 대문자로 변수이름을 짓거나 `typing`의 `Final`을 사용하는 방식을 취한다.
|let name=value;| no need |파이썬의 모든 변수는 가변적이므로 let이 필요하지 않다.
|Template Literals: ` ${variable}`|f-string: f"{변수}"|기능에 차이는 없다.
|const myFunc = (name) => return `이름은 ${name}다.`|X|return을 생략할 수도 있다. 파이썬3의 화살표 문법은 `->` 를 사용하며 반환값의 형태를 임시로 지정한다.|

그 외의 문법들은 사용하며 익숙해지자.
- [출처: [JavaScript] 자주 사용하는 ES6 문법 정리](https://velog.io/@kimhscom/JavaScript-%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-ES6-%EB%AC%B8%EB%B2%95-%EC%A0%95%EB%A6%AC#default-parameters%EA%B8%B0%EB%B3%B8-%EB%A7%A4%EA%B0%9C-%EB%B3%80%EC%88%98)