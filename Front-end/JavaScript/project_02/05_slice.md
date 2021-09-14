### 최대 글자를 넘으면 자르는 기능 구현: `substring`

문자열 자료형도 array처럼 0부터 시작하는 index가 있다. (띄어쓰기 포함)  
substring을 이용하면 문자열을 slicing 할 수 있다.  

자소서 글자수 세기 프로그램을 완성하기 위해 200글자가 넘어갈 경우 더 이상 입력되지 않도록 하는 기능을 구현한다.
- 입력은 되지만 (이벤트는 생성되지만) 문자열 자료형에 반영되지는 않는 형태다.
- 따라서 substring을 한 후 원래 문자열에 재할당 해야한다!

![text-slicing](https://user-images.githubusercontent.com/60145951/152693596-ca0a0a64-423b-4b62-96e4-ad9cd265cdbc.png)

완성!