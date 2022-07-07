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

## Icon font

svg기반의 벡터 그래픽을 폰트파일로 만들어 CSS를 통해 아이콘을 사용할 수 있도록 한다.
이미지를 관리할 필요가 없이 폰트 파일과 CSS만 관리하면 되므로 유지보수에 유리하다.

## skewed section

컨테이너에 skew()를 적용하게 되면 안에 있는 요소들도 기울어지게 된다. 이를 해결하기 위해서 direct child selector를 사용한다.

## direct child selector

'>'를 사용해 직계 자식 요소만을 선택할 수 있다.

## perspective

perspective 속성은 CSS로 3D효과를 줄 수 있는 속성으로, 값만큼 멀어져 있는 효과를 낸다. -> 값이 작을수록 변화가 극적이다.

## backface-visibility

hidden으로 설정하면 요소의 뒷부분을 숨긴다.

## background blend mode

## box-decoration-break
