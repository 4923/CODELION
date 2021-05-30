## JS의 반복문 (loop)

### for-loop
> 특정 횟수를 반복하고 싶을 때 사용
```js
// C와 비슷하다.
for (시작; 끝; 증감){
    // 반복할 내용
}

// EXAMPLE
for (var i=0; i<6; i++){
    lotto.push(parseInt(randomNumber*45 +1))
}
```
![for loop](https://user-images.githubusercontent.com/60145951/152655999-94d239e4-d4ce-4160-89df-30f893c4a2c1.png)

반복문을 이용해 난수를 여섯번 생성하고 로또 번호에 알맞은 형태로 변환했다.  
함수를 이용하면 반복문 안에 넣는 코드를 조금 더 간결하게 정리할 수 있을 것 같다.

### while-loop
> 반복문에 조건을 걸고 싶을 때 사용
```js
while (조건){
    // 반복하고 싶은 내용
}

// EXAMPLE:
// 배열의 길이가 6 미만일 때가 조건이므로 배열의 길이가 6이 되면 멈춤.
while (lottoArray.length < 6){
    // 생략
}
```

- 배열의 길이는 어떻게 확인할까?: `.length`
    - [참고: project_01/JS의 배열](https://github.com/4923/Web/blob/master/Front-end/JavaScript/project_01/05_lottery-array.md)