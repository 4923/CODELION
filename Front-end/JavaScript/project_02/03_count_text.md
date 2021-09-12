### JS로 글자 수를 세보자!

### 1. `.length;` 로 글자 수 세기
> `.length;` 는 array 뿐 아니라 string에서도 쓸 수 있다.
```js
var content = document.getElementById('jasoseol').value;
console.log(content.length);
```
![.length](https://user-images.githubusercontent.com/60145951/152691149-614ebb9d-6006-4fbf-aca3-af4dc82c2440.png)
이렇게! console에서 확인할 수 있다.

### 2. innerHTML로 HTML 수정하기.
> documnet.write()를 사용할 수도 있지만, 원하는 위치에 원하는 형태로 출력하고 싶다면?

- 출력이 아니라 원하는 값을 담는 작업이 추가되었음에 유의
- 원래 `(0/200)` 이 적혀있어야 할 자리에 글자  `<textarea>`의 글자 수인 15가 적혀있는 것 확인할 수 있다.
    ![innerHTML](https://user-images.githubusercontent.com/60145951/152691726-1fa33734-6f7f-47b0-9155-28ad8a16503e.png)
    - 단, 아직 입력 textarea 안의 값을 수정하는대로 글자 수가 변경되지는 않는다.

- 그럼 `<span>` 태그 사이에 `(0/200)` 이건 왜 넣나?
    - 지워도 문제 없이 작동하지만 이 부분에 이런 내용을 넣겠다는 표현인것 같다.
    - 별도의 설명이 없으므로 일단 지나가보기.

### 3. 자동 형변환!
> JS는 문자열과 숫자를 더해 문자열로 만들 수 있다.
```js
document.getElementById('count').innerHTML = '(' + content.length + '/200)';
```
- 원하는 형태로 변형해보자! 
    ![count_temp_text](https://user-images.githubusercontent.com/60145951/152691840-d565ffae-88e4-45ad-92ac-4cf5ee668599.png)
- vs Python: python에서는 문자열끼리 더할 수 있므로 `TypeError`가 발생한다.
    ![vsPY](https://user-images.githubusercontent.com/60145951/152691915-29eaef7f-fa55-43de-9e6a-3d23be4355cc.png)

