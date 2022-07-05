# Using advanced CSS & SASS

## Custom grid with floats

sass에서 calc 사용시 변수를 넣을 때는 `#{$variable}`처럼 사용.
<br>
float의 경우 컨테이너의 높이를 0으로 만들어버린다. 이는 float이 된 요소가 자리를 차지하지 않게 되어버리기 때문.
<br>
이를 해결하는 방법은 여러가지가 있지만 여기서는 mixin을 통해 해결.

- attribute selector: 주어진 특성의 존재 여부나 그 값에 따라 요소를 선택할 수 있다. 접두사/접미사 등도 사용 가능.
  https://developer.mozilla.org/ko/docs/Web/CSS/Attribute_selectors

- (-webkit)background-clip: text & colo: transparent로 설정하면 배경 색이 텍스트에 적용된다.
