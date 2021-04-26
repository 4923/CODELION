## Semicolon (`;`)을 사용하지 않는 언어, JavaScript
- C나 Java에서 세미콜론은 하나의 명령이 끝났음을 알리는 표시자이나, JS는 '유연한'언어이므로 Python처럼 명령의 끝에 세미콜론을 강제하지 않으며 한 **줄**이 명령어로 인식된다.
1. YES! **줄 개행만 제대로 되어있다면** 세미콜론은 써도 되고, 쓰지 않아도 상관없다.
    ```js
    // OK
    document.write('명령1')
    document.write('명령2');
    document.write('명령3')
    ```
    ![image1](https://user-images.githubusercontent.com/60145951/152650277-e64cc274-0d80-4bd3-b696-2459821d8db2.png)
2. NO! 개행이 되어있지 않은 상태에서의 (한 줄에서) 여러 명령 사용은 문법에 맞지 않다.
    ```js
    // NOT ok
    document.write('명령1')document.write('명령2')
    ```
    ![image2](https://user-images.githubusercontent.com/60145951/152650243-76dd897f-94c3-4c01-a161-29f86aa0ec11.png)
3. YES! 한 줄에서도 세미콜론만 제대로 써준다면 여러가지 명령을 입력할 수 있다.
    ```js
    // OK
    document.write('명령1'); document.write('명령2')
    ```
    ![image3](https://user-images.githubusercontent.com/60145951/152650266-b1c177e5-1191-4d08-b87a-37eacc1a3a66.png)

세미콜론을 빠트려도 되는 C라고 생각하자.
세미콜론가 원래는 줄개행을 나타내는 용도가 아닌 **명령어끼리의 구분자**였다는 유래를 알면 이해가 쉽다. ([참고:C나 자바에서 세미콜론을 쓰는 이유](https://flative.github.io/blog/2017/01/22/semicolons-c-java/))

## JS에서의 주석
> VSCode에서 주석은 `ctrl + /` 이며 언어에 맞춰 주석을 생성해준다.

주석은 컴퓨터가 읽을 수 없는 문구로, 컴퓨터가 아닌 프로그래머를 위해 적는다.  
주석이 필요 없을만큼 잘 설명된 코드를 적을 수 있다면 좋겠지만, 그럴 수 없을 경우 가능한 상세히 적는다.

언어에 따라 주석의 시작을 표기하는 표시자가 달라진다.  
js에서는 아래와 같이 주석을 표기한다. C에서의 표기와 동일하다.
- 한줄 주석: `//`
- 블록형 주석: `/* */`

```js
// 코드블럭에서도 마찬가지.

/*
backtick(`) 세개로 시작하는 코드블록 바로 옆에 언어명을 적어주면
markdown에서도 언어에 따른 하이라이팅이 가능해지고, 
vsc 역시 언어에 맞는 주석 표기를 해준다.
*/
```

비교를 위해, Python에서의 표기를 덧붙인다.
- 한 줄 주석: `#`
- 블록형 주석: `''' '''`

