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
