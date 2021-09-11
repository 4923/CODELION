### [MISSION!] id로 Tag의 내용을 읽어오자

```html
<html>
    <head></head>
    <body>
        <h1>자기소개</h1>
        <!-- 이 부분! -->
        <textarea id='jasoseol'>
            먹고 사는건 원래 힘듭니다.
        </textarea>
    </body>
</html>
```

1. 태그에 접근:  `document.getElementById('id');` 
    - 위 코드블럭 예시에서 내용을 가져오려면? `document.getElementById('jasoseol');` 명령을 이용하자.
2. 내용을 읽어오기: `.value;` or `.innerHTML;`
    - `document.getElementById('jasoseol').value;` 로 태그 안쪽에 있는 값만 가져올 수 있다.
3. 출력하기: `console.log('message');`
    - browser가 아니라 console에 출력하려면 해당 명령어를 사용한다.
    - 어떻게 확인하지?: 브라우저 `f12`로 열 수 있는 개발자도구의 console 탭에서 확인 가능
        ![console.log](https://user-images.githubusercontent.com/60145951/152682244-95af39c5-e13d-4c27-9d94-6ce96947ba27.png)

<br><hr><br>

### [Optional] #1 읽어오는 태그들의 종류
> 목표를 명확하게 하자!
- 가져오고 싶은 태그의 종류에 따라 사용하는 명령이 달라진다.
    1. `.value`
        - `input` 같은 **form** 요소의 값을 가져온다.
    2. `.textContent`
        - input 외 `div` 나 `span` 요소 안의 내용(text)를 읽고 싶을 때 사용한다.
        - 객체 안의 값을 변경할 때 사용
            - 그럼 `.value`는??? 변경을 못해???
- `.innerHTML` vs ` .innerText` vs `.textContent`

- [참고: velog/Javascript: value vs textContent, innerHTML, innerText](https://velog.io/@minjae-mj/Javascript-value-vs-textContent-innerHTML-innerText)

### [Optional] #2 왜 console에 출력하지?
> console pannel에서는 에러를 확인할 수 있다!
개발자 도구를 좀 자주 써봤으면 의문을 가지지 않았을 텐데...  
윈도우 기준 `f12`로 개발자 도구를 연 후 `esc`를 입력하면 하단에 콘솔 창이 열린다.  
콘솔 창에 명령어를 입력하고 `enter`로 실행하는 과정을 거치기 때문에 `console`에 실행 결과를 기록하는 `log` 명령어가 생겼다.  
- 덤으로, python에서 return 값에 아무것도 주지 않으면 `None`을 반환하는데 JS가 아무것도 반환하지 않으면 `undefined`가 출력된다.
    ![return](https://user-images.githubusercontent.com/60145951/152685612-1f636b56-e68b-4c28-bec4-647758d27463.png)

- 참고
    - [코어 자바스크립트/소개/개발자 콘솔](https://ko.javascript.info/devtools)
    - [코어 자바스크립트/코드 품질/Chrome으로 디버깅하기](https://ko.javascript.info/debugging-chrome)