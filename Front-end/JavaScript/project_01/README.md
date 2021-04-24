## Javascript로 만드는 '로또 번호 추첨기'

> Goal: 새로고침 할 때마다 번호가 랜덤하게 출력되는 프로그램

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