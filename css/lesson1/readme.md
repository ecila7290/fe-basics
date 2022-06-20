# CSS
## 기본, 그룹 선택자
- '*': 모든 요소 선택
- 같은 선택자이면 뒤에 오는 것이 우선순위 높음
- tag: 태그 선택자
- .someclass: 클래스 선택자로 태그보다 우선순위 높음. 페이지상의 여러 요소가 같은 class를 가질수 있다.
- 태그.클래스: 다른 선택자에 이어붙일 수 있고, 이어붙인 것이 더 구체적이므로 우선순위가 높다
- #id: id는 페이지상에서 요소마다 고유해야 한다. class보다 우선순위가 높음
- 태그, 클래스, id: ','로 이어서 그룹을 선택할 수 있음

## 결합자와 가상 클래스
- .class tag: 공백으로 아래의 모든 자손 태그와 결합
- .class > tag: 직계 자식만 결합
- .class ~ tag: 클래스 아래의 모든 같은 형제 태그에 적용
- .class + tag: 뒤따르는 하나의 같은 태그에만 적용
- ol li:first-child(..etc): 가상 클래스
- :not(:psuedo-class): ~가 아닌 요소 가상클래스
- :not(.real-class): ~가 아닌 클래스에만 적용
- :nth-child(x): x번째에 요소 가상 클래스
  - xn을 넣으면 x번째 요소마다 가상 클래스 (xn+y)도 가능
  - odd/even: 홀수/짝수번째 요소마다
- hover: 마우스 호버링시 적용

## 선택자 연습
https://flukeout.github.io/ <br>
18번까지는 현재 배운 것으로 커버 가능