# Setup
예제 페이지 https://natours.netlify.app/
## Build Header (Part.1)
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

### 기타
- background-size: cover
박스의 너비와 상관 없이 항상 공간을 채우도록 한다.
- background-position
수평,수직 설정으로 이미지 위치 지정. 설정하지 않은 부분은 자동으로 center
- padding은 상속되지 않는다.
- transform: translate
요소의 표시 위치를 이동시키는 방법 중 하나. calc대신 이를 사용해서 요소를 현재 위치에서 지정한 값만큼 이동시킨다.