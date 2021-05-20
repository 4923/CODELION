## JS의 난수
1. `var num = Math.random();` => 0이상 1미만의 난수 생성 (float)
- 새로고침 할 때마다 JS가 실행되는 것이므로 매번 새 난수를 출력하는 조건은 신경 쓸 필요 없다.
    ![Math.random between 0 to 1](https://user-images.githubusercontent.com/60145951/152653091-554b4c86-c375-49b9-bffc-cc525f90d3e3.png)
2. 45를 곱한다.
    - `num * 45` 를 한다면? 0이상 45미만의 실수가 된다.
        ![multiple 45](https://user-images.githubusercontent.com/60145951/152653196-b8bb7ec6-42ee-4d27-bd29-d64fac408408.png)
3. 로또 번호에 0은 없으므로 단계 2에서 1을 더한다.
    - `num * 45 + 1` => 1이상 46미만의 실수가 된다.
4. 정수형으로 전환: `parseInt();`
    - 소수점을 버리고 정수로 변환한다.
        ![parseint example](https://user-images.githubusercontent.com/60145951/152653352-62e692cd-b4a7-4caf-b957-d8fd75aedef9.png)

