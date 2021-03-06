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

배경 이미지 여러개를 혼합(blend)할 수 있게 해준다.

## box-decoration-break

요소가 여러줄, 컬럼, 페이지로 분할되었을 때, 분할된 조각을 어떻게 렌더링할지 정할 수 있다. clone 옵션을 주면 각각의 조각이 하나의 요소인 것처럼 독립적으로 렌더링된다.

## shape-outside & float

인접하는 인라인 콘텐츠를, 설정한 형태에 따라 감싸도록 처리. circle()을 선택한 경우 `circle({radius} at {x} {y})`로 위치를 결정한다.

## filter

그래픽 효과를 요소에 적용.

- blur: 이미지가 흐릿해짐. px 단위의 값을 받고 값이 클수록 더 흐려진다.
- brightness: 이미지를 밝거나 어둡게. % 또는 0~1 사이의 값.

## video element

video 태그를 통해 영상을 추가할 수 있다. 이 때 src 옵션에 출처를 넣는 대신 태그 안에 source태그를 넣으면 여러개를 넣을 수 있다. 이 방법으로 브라우저에 맞는 영상 확장자(mp4, webm 등)가 재생될 수 있도록 할 수 있다. (js를 사용하게 되면 필요 없을 것 같다.)

## object-fit property

img, video와 같은 요소의 크기를 어떻게 조절할지 선택할 수 있다. https://developer.mozilla.org/ko/docs/Web/CSS/object-fit

- cover: 콘텐츠의 가로세로비를 유지하면서 요소의 콘텐츠 박스를 가득 채운다. 가로세로 비율이 일치하지 않으면 객체 일부가 잘려나간다.

## solid-color gradients

https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient <br>
linear-gradient의 color-stop 설정을 활용해서 solid-color와 transparent한 바탕을 동시에 나타낼 수 있다.

## general & adjacent sibling selectors

자식 요소가 아닌 같은 계층의 요소를 선택하고자 할 때는 + / ~를 사용한다. 이 때 +는 요소 바로 다음에 있는 요소 하나를 선택하게 되고 ~는 같은 계층의 모든 요소를 선택하게 된다.

## ::input-placeholder

## :focus, :invalid, :placeholder-shown, :checked

- :focus
  input등에서 클릭된 요소. `outline: none;`으로 설정해서 클릭시 감싸는 선을 제거할 수 있으나, 제거할 경우 칸이 선택됐다는 표시를 별도로 해주는 것이 좋다.

- :invalid
  input의 email처럼 html에서 validation을 제공하는 경우, 해당 pseudo-class를 사용해서 invalid한 경우의 스타일을 별도로 지정해줄 수 있다.

- :placeholder-shown
  input, textarea 등에서 placeholder를 설정한 상태일 때, placeholder가 나타난 경우의 스타일을 지정.

- checked
  radio button 등이 선택되었을 때의 스타일을 지정할 수 있도록 한다.

## build custom radio buttons

라디오 버튼의 체크 형태는 변경할 수 없다. 따라서 이를 `display: none`으로 설정하고 별도로 span 태그의 border를 원하는 형태로 설정하여 버튼을 대신하도록 하는 방식으로 커스텀 버튼을 사용한다.

## checkbox hack

햄버거에서 내비게이션 링크가 모여있는 화면을 띄울 때 checkbox hack을 사용한다. <br>
이를 적용하는 방법은, 클릭하면 사라지는 checkbox를 설정하고 해당 checkbox와 연결된 label을 설정한다. checkbox가 클릭되면(pseudo-class 사용) 내비게이션 링크가 모인 화면을 보여주도록 한다.

## cubic bezier curves

transition에서 요소를 제어할 때 cubic-bezier curve 효과를 주도록 하는 방법. ease-in, ease-out 등 빌트인 세팅이 있지만 좀더 커스텀한 제어를 원할 때는 https://easings.net/ko 에서 찾아볼 수 있다.

## how and why to use transform-origin

transformation이 일어나는 기준 축을 정한다. 기본값은 center.

## :target

id와 같은 고유한 요소와 링크의 href를 연결하고, 클릭했을 때 CSS를 적용할 수 있다.

## display: table-cell

사용하기 위해서는 부모 요소에 `display:table;`을 설정해야 한다. table-cell은 td로 변환한 것과 같은 효과를 내며 이로 인해 정렬을 쉽게 할 수 있다.

## CSS text columns

긴 텍스트를 신문처럼 컬럼으로 나누어 보여줄 수 있다. `column-count`로 컬럼의 개수, `column-gap`으로 컬럼간의 간격, `column-rule`로 컬럼 사이에 구분선을 설정할 수 있다. <br>
해당 기능은 prefix 필요

## hyphens

줄바꿈으로 인해 단어가 연결되지 않으면 하이픈으로 연결해준다. 적용하기 위해서는 html의 lang 설정이 필요하다. <br>
해당 기능은 prefix 필요

prefix는 손으로 입력하는 것이 아니라 auto prefixer 등을 사용하는 것이 바람직하다.
