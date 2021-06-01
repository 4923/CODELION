## Javascript로 만드는 '로또 번호 추첨기'

> Goal: 새로고침 할 때마다 번호가 랜덤하게 출력되는 프로그램

### Done! [🎲 Your lottery number generator](https://github.com/4923/Web/blob/master/Front-end/JavaScript/project_01/lotto-generator.html)

![lotto generator final](https://user-images.githubusercontent.com/60145951/152658035-b51fdc65-070d-425c-b16b-b9e2b75fc09e.png)

<br>

```python
# 동일한 코드를 파이썬으로 짠다면
import random

def rotto_generator() -> list:
    rotto_numbers = [random.randint(1, 46) for _ in range(6)]
    return rotto_numbers

def main():
    # 새로고침 할 때마다 다른 숫자를 출력하는 효과를 내려면
    # rotto_generator() 함수를 새로고침 할 때마다 호출하면 된다
    return

if __name__ == "__main__":
    main()
```

익숙한 파이썬 문법을 결과물로 떠올려두고 JS 문법에 대응시켜가며 배워보자.

## breakdown steps
로또번호 추첨기의 주요 기능은 아래와 같다.
|기능|Py|JS|
|:-|:-|:-|
|1부터 45까지의 자연수가 6개| [ ___(1, 45) for _ in range(6)| for (var i=0; i<6; i++){ ___ }; |
|무작위하게| random.randint | parseInt(Math.random()*45 +1) |
|새로고침 할 때마다 출력| 함수화, return | X |
|중복이 아닐 때 (조건) | if lotto_list.find(target) != -1 : | if (lottoArray.indexOf(lottoNumber != -1)){ ___ }

## projects 1: contents
- [JS의 난수 생성 방법](https://github.com/4923/Web/blob/master/Front-end/JavaScript/project_01/04_lottery-random.md)
    - `Math.random();` => 0이상 1 미만의 난수 생성
    - `parseInt();` => 실수형을 정수형으로
- [JS의 배열](https://github.com/4923/Web/blob/master/Front-end/JavaScript/project_01/05_lottery-array.md)
    - python의 dequeue와 같다.
    - `.push()`, `.pop()`: 배열의 끝에 밀어넣고, 추출하는 작업
    - `.unshift()`, `.shift()`: 배열의 앞에 밀어넣고, 추출하는 작업 (`.appendleft`, `.popleft`)
- [JS의 반복문](https://github.com/4923/Web/blob/master/Front-end/JavaScript/project_01/06_lottery-loop.md)
    - C의 조건과 같다.
    - `for (var i=0; i<6; i++){ ___ };`
- [JS의 조건문](https://github.com/4923/Web/blob/master/Front-end/JavaScript/project_01/07_lottery-condition.md)
    - C의 사용방법과 같다.
    - `if (condition1) { run if condition1 is true }`