## js를 사용하는 방법
1. HTML의 `<script/>`
2. `.js` 파일

## HTML의 JS
1. 위치: 어디에 작성해도 상관없다.
    - 하지만 위에서 아래로 읽는 HTML 특성 상 모든 html 내용을 불러온 후에 작성한다.
        - `</body>` 바로 위
        - 예시
            ```html
            <body>
                <!-- HTML scripts -->
                <script>
                </script>
            </body>
            ```
    - 왜? 미리 불러오면 되는게 아닌가?
        - *[Naver D2, 브라우저는 어떻게 동작하는가?/스크립트와 스타일 시트의 진행 순서](https://d2.naver.com/helloworld/59361)*
        - 웹의 동기적 특성상 HTML parser는 `<script>` 태그가 닫힐 때 까지 문서의 파싱을 중단하므로 가장 마지막에 불러오는 것이 효과적이다. 또는 스타일 시트에 작성하도록 하자.
        - 이게 도대체 무슨 말이냐
            1. 웹은 읽어오는 것과 만드는 것을 동시에 수행하는 **동기화(synchronous) 모델**이다.
                |동기화|브라우저 엔진|
                |:-:|:-:|
                |![sync?](https://user-images.githubusercontent.com/60145951/152646590-22905803-e643-4c37-9299-03fbbad026c4.gif)|![browser engine](https://user-images.githubusercontent.com/60145951/152646776-e5e1fe4f-0471-4528-82ef-67ed36ffe0ac.png)|
            2. 그래서?
                - 스크립트(`<script>`)를 불러오는 동안 불려와야 할 HTML 등이 불려오지 못한다면 사용자에게 답답함을 줄 수 있다.
                - 중요한 내용, 웹페이지의 기틀이 되는 내용을 먼저 불러오고 곁다리인 스크립트는 나중에 불러오도록 하자.
                    1. 그 방법 1) 스타일시트에 작성하기
                        - 스타일시트는 말그대로 '스타일' 이므로 DOM Tree parsing에 영향을 미치지 않는다.
                        - 그러므로 스크립트를 스타일시트에 적는다면 네트워크로부터 불러오는 자원을 적절하게 사용할 수 있다. 예외도 있지만 일단 넘어간다.
                    2. 그 방법 2) 예측 파싱
                        - 스크립트를 읽어오는 동안 문서의 다른 부분을 읽어온다. 일종의 병렬 처리.
            3. 그런데...
                - <font color="orange"> HTML5는 스크립트를 비동기로 처리</font>하는 속성을 추가했다.
                - 따라서 HTML5부터는 스크립트가 별도 맥락에 의해 파싱 및 실행된다.
                - 그렇지만 HTML5에서 추가된 속성이니 관례로 굳어졌을 방식에 익숙해지도록 하자.
2. `document.write();`
    ```js
    document.write();
    ```
    - write의 인자로 원하는 말을 넘기면 그 말이 브라우저에 표시되는 기능.
    - python의 print와 유사하나 브라우저에 표시된다는 점은 다르다.

## `.JS`

```js
documnet.write("자바스크립트 파일에서 불러온 명령")
```

별도의 js 파일을 만들고 (`.js` 확장자) HTML 파일에 스크립트 명령을 입력한다.

```html
<!-- 생략 -->
<script src="file path"></script>
```

내용은 동일하지만 별도의 파일로 관리하는 셈이다. 이 때 js 파일명은 **camelCase**를 사용한다.

## Done!
![firstScript](https://user-images.githubusercontent.com/60145951/152649720-7d343b40-ed64-4cf3-9b51-42ab52f9d829.png)

`index.html`를 preview한 결과다. 
html이 그렇듯이 `<br>` 로 줄개행을 하지 않으면 다른 태그의 내용도 한 줄에 작성된다.
