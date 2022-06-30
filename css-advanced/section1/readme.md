# Setup
예제 페이지 https://natours.netlify.app/
## Build Header
### universal selector
universal selector '*'로 전 범위에 대한 css설정. 보통 블록 요소들에 있는 margin, padding 제거하기 위해 사용
- box-sizing: border-box
border, padding이 width, height에 더해지지 않도록 함

### project-wide font definitions
font와 관련된 property들은 대부분 상속되기 떄문에 universal selector를 사용하는 것이 아니라 body에 사용

### clip-path
이미지가 보일 영역의 폴리곤을 지정 <br>
왼쪽 위가 0 0, 끝에서 끝은 100%.
단위는 %/픽셀/viewport 가능 <br>
clippy 검색하면 쉽게 원하는 모양 만들 수 있음.

## CSS animations
### keyframes
JS 없이 CSS 만으로도 애니메이션을 구현할 수 있게됨.<br>
keyframe은 특정 지점(0%~100%, from~to)의 애니메이션을 제어할 수 있도록 한다.
<br>
```CSS
@keyframes {identifier} {
  ...
}
/*정의하고 요소 안에 animation-name: identifier
animation-duration: 시간 지정
*/
```

### animation
- animation-name
설정한 identifier를 넣어준다.
- animation-duration: 지속시간
- animation-delay: x초 후에 수행된다.
- animation-iteration-count: 애니메이션 반복 횟수
- animation-timing-function: 애니메이션이 어떻게 진행될지 설정
  - 키워드로 조절할 수도 있고 함수로 조절할 수도 있다.
- animation-fill-mode: 애니메이션이 실행 전/후 언제 적용될지 선택.

## Animated buttons
### pseudo-element, pseudo-class
특정 조건에서 스타일을 적용하기 위해 사용
- :link, :visited
href 속성을 가진 요소 중 방문하지 않은 것, 방문한 것을 선택
- :active
활성화한 요소. 마우스 버튼을 누르는 순간부터 떼는 시점까지.
각각의 pseudo-class는 연속적이지 않다. hover 다음 active 있어도 동작이 이어지는 것이 아니라 초기 상태로 돌아갔다가 다음 단계로 넘어간다.

### ::after
선택한 요소의 맨 마지막 자식으로 의사 요소를 하나 생성. 안에 반드시 content 요소가 있어야 한다. (값은 ""이어도 됨)

### transition
transition으로 애니메이션을 적용할 때 항상 initial state인 곳에 적용해야 한다.

## 기타
- background-size: cover
박스의 너비와 상관 없이 항상 공간을 채우도록 한다.
- background-position
수평,수직 설정으로 이미지 위치 지정. 설정하지 않은 부분은 자동으로 center
- padding은 상속되지 않는다.
- transform: translate
요소의 표시 위치를 이동시키는 방법 중 하나. calc대신 이를 사용해서 요소를 현재 위치에서 지정한 값만큼 이동시킨다.
- backface-visibility: hidden
transform할 때 요소의 뒷면이 보이지 않도록 한다. (default visible)
- transform: scale(n)
n배만큼 커지게 한다.