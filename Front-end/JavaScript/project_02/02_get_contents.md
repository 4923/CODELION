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
            - 그럼 `.value`는??? -> [[Optional] #2 JS에서 값을 조작하는 과정](#-optional---2-js-------------) 항목에서 보충

- `.innerHTML` vs `.innerText` vs `.textContent`
    - 공통점: 마크업 언어를 가져와 변경할 수 있다.
    - 차이점: 일단 눈으로 보자.
        ```html
        <div id="statement">
            Keep Calm and          Drink <strong>Coffee</strong>
            <span style="display:none">Sometimes, Tea</span>
        </div>
        ```
        |tag|view|
        |:-:|:-:|
        |browser|![browser](https://user-images.githubusercontent.com/60145951/152688301-d2353801-7ee7-4bea-acaa-001f84b5cb79.png)|
        |`.innerHTML`|![innerHTML](https://user-images.githubusercontent.com/60145951/152688463-7ed41a9a-35eb-4c58-a069-c5b1bc14c153.png)|
        |`.innerText`|![innerText](https://user-images.githubusercontent.com/60145951/152688468-593f140f-a9ab-44cf-a0b9-33f8cafa5bc0.png)|
        |`.textContent`|![textContent](https://user-images.githubusercontent.com/60145951/152688478-7dbb36b7-aba8-4e4c-af76-991516a547ea.png)|

    

    1. `.innerHTML`: 마크업 언어를 핸들링할 수 있다.
        - 안에 (inner) HTML을 넣는다 !!!
        - 무슨 말이냐?: input에 `<div>` 등을 넣어 HTML 파일을 직접적으로 수정할 수 있다는 말이다.
        - 당연히: 개발자가 의도한 방향이 아닐테고, 공격에 취약해진다.
            - 이런 공격을 `XSS 공격`이라고 한다.
            - XSS 공격이란?: Cross Site Scripting의 약자로 입력 태그를 통해 직접적으로 DOM을 조작할 수 있는 악의적인 script를 주입하는 공격 방법이다. 주 목적은 사용자의 정보를 가로채는 것이다. [더보기](https://nordvpn.com/ko/blog/xss-attack/)
    2. `.innerText`: 마크업 언어를 적용 된 == 렌더링 된 형태로 읽어온다.
        - `.innerHTML`과 뭐가 다르냐: HTML을 넣는지, Text를 넣는지가 다르다. **HTML 요소가 제거된** 텍스트만 불러오니 좀 더 안전하다.
        - 사용자에게 보이는 최종 결과 값만 보여준다.
    3. `.textContent`
        - 항목 1과 2 사이의 명령이라고 생각하자.
        - div 태그 안에 작성되는 **실제 내용** 이다. (위의 예: `Keep Calm and          Drink <strong>Coffee</strong>\n <span style="display:none">Sometimes, Tea</span>`) 
        - 개발자의 눈에 보이는 값과 같으므로 개발 과정에서 사용하기에 적합하다.

    - [참고: velog/Javascript: value vs textContent, innerHTML, innerText](https://velog.io/@minjae-mj/Javascript-value-vs-textContent-innerHTML-innerText)

### [Optional] #2 JS에서 값을 조작하는 과정

JS에서 값을 조작하는 과정!  
저도 참 궁금한데요  

JS에서 DOM Tree를 수정하는 방법은  
JS를 사용해서 DOM Tree에 접근하고 수정하는 방법이라고 합니다.  
어렵지 않죠?  

다음에 더 알아보도록 해요 :wave:  
그럼 안녕!


### [Optional] #3 왜 console에 출력하지?
> console pannel에서는 에러를 확인할 수 있다!

- 개발자 도구를 좀 자주 써봤으면 의문을 가지지 않았을 텐데...  
- 개발자 도구를 열며 console.log의 의미를 파악하기
    1. 윈도우 기준 `f12`로 개발자 도구를 연 후 `esc`를 입력하면 하단에 콘솔 창이 열린다.  
    2. 콘솔 창에 명령어를 입력하고 `enter`로 실행하는 과정을 거치기 때문에 `console`에 실행 결과를 기록하는 `log` 명령어가 생겼다.  

- 덤으로, python에서 return 값에 아무것도 주지 않으면 `None`을 반환하는데 JS가 아무것도 반환하지 않으면 `undefined`가 출력된다.
    ![return](https://user-images.githubusercontent.com/60145951/152685612-1f636b56-e68b-4c28-bec4-647758d27463.png)

- 참고
    - [코어 자바스크립트/소개/개발자 콘솔](https://ko.javascript.info/devtools)
    - [코어 자바스크립트/코드 품질/Chrome으로 디버깅하기](https://ko.javascript.info/debugging-chrome)