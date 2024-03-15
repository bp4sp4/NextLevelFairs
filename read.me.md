# Parallax Button(w.fastcompus)

<h2>24/03/14(목) 시작 ~ 24/03/15(수) 끝<h2>

데모사이트 : <a href="">Demo Site</a>

<h3>학습 내용</h3>

- 커서모양을 바꾸고 푸쉬 버튼 영역을 클릭
- 화면이 커지면서 hidden 영역을 보여줌을 처리
- 마우스 방향에 따라 Parallax 기법을 사용해 글자와 도형들이 움직임을 처리
- 밑으로 스크롤 하였을떄 Obsever API 를 사용해 스크롤 하였을때 어느 위차에 도달했을때 사진들을 애니메이션 처리해 나타나게함

<h3 color="red">Intersection Observer API</h3>

- 요소가 화면에 들어오거나 나갈 때 실해될 콜백 함수를 넘겨 IntersectionObserver 객체를 만든다
- 관찰하고 싶은 요소를 인자로, IntersectionObserver 객체의 observe 메소드를 호출하여 관찰을 시작한다.
- 콜배 함수의 단일 인자인 entries(요소의 노출 정도, 위치 , 크기 등 포함)로 필요한 정보를 얻는다.

```
let observr = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
        if (entry.isINtersecting) {
            // 요소가 50% 이상 보일때 행하는 동작
        }
    })
}, {threshold: 0.5});

let element = document.querySelector("#my-element);
observer.observe(element);
```
