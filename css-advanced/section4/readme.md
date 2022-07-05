# Using advanced CSS & SASS

## Custom grid with floats

sass에서 calc 사용시 변수를 넣을 때는 `#{$variable}`처럼 사용.
<br>
float의 경우 컨테이너의 높이를 0으로 만들어버린다. 이는 float이 된 요소가 자리를 차지하지 않게 되어버리기 때문.
<br>
이를 해결하는 방법은 여러가지가 있지만 여기서는 mixin을 통해 해결.

- attribute selector: 주어진 특성의 존재 여부나 그 값에 따라 요소를 선택할 수 있다. 접두사/접미사 등도 사용 가능.
  https://developer.mozilla.org/ko/docs/Web/CSS/Attribute_selectors

- (-webkit)background-clip: text & colo: transparent로 설정하면 배경 색이 텍스트에만 적용된다.

- outline: 박스에 테두리를 그려준다.
  <br>
- border vs outline
  - border는 특정 테두리에만 효과를 줄 수 있다. 또한 옵션으로 주는 두께만큼 박스의 크기도 늘어난다.
  - outline은 offset을 통해 간격을 조절할 수 있다. 또한 요소 밖에서 생성되어 박스 크기에 영향을 주지 않는다.
