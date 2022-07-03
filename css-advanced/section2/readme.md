# How CSS works behind the scenes
## 3 pillars of writing good HTML & CSS
### Responsive design
- fluid layouts
- media queries
- responsive images
- correct units
- desktop-first vs mobile-first

### Maintainable & scalable code
- how to organize files
- how to name classes
- how to structure HTML

### Web performance
- less HTTP requests
- less code / compress code
- use CSS preprocessor (eg; SASS)
- less images / compress images ()

## Overview
![overview](./overview.png)

## How CSS is parsed
### Cascade
여러 stylesheet(author, user, browser)를 합치면서, 요소에 1개 이상의 규칙이 적용될 때 발생하는 충돌을 해결하는 과정
- 우선순위
  - importance: !important 선언 등
  - specificity: inline style > ID > class, pseudo-class, attribute > elements, pseudo-elements
  요소 안에 해당 범주의 개수를 측정((0,1,2,3) 처럼)하고 순서대로 비교하면서 먼저 나온 것+숫자가 큰 것을 우선적으로 적용한다.
  - source order: specificity까지 같다면 가장 마지막에 선언된 내용이 적용된다.

- universal selector는 (0,0,0,0) 값이므로 우선순위가 가장 낮다.
- 순서보다는 specificity에 의존하는 것이 유지보수하기가 좋다.
- 서드파티 stylesheet를 사용하는 경우에는 순서가 중요. author stylesheet를 마지막에 둔다.

### Value processing
- em, rem은 font-based
- font의 em은 부모 요소의 크기에 영향을 받고 length의 em은 현재 요소의 크기에 영향을 받는다.

### Inheritance
- 보통 text와 관련된 property는 상속된다. (font-size, font-family, color ...)
- 부모 요소에서 계산된 값이 상속되는 것이지 자식 요소에 선언된 값을 계산하여 상속되는 것이 아니다.
- inherit, initial 키워드를 사용해 강제로 상속시키거나 초기화할 수 있다.

## How CSS renders a website
### Visual formatting model
- box model
박스의 너비/높이의 길이는 width/height+padding+border. box-sizing: border-box로 설정하면 너비/높이의 길이를 padding, border 포함된 값으로 정할 수 있음. 
- box types
  - inline: content의 공간만큼 차지, line-break 없음, padding, margin은 왼쪽&오른쪽에만 적용
  - block: 구분되는 블록으로 존재, 너비는 부모 너비의 100%, box-model이 보이는대로 적용
  - inline-box: content의 공간만큼 차지, line-break 없음 but box-model 보이는대로 적용
- positioning scheme
  - normal flow: NOT floated, NOT absolute position, 요소가 순서대로 정렬
  - floats: normal flow로부터 제외됨, 주변의 text, inline element는 float element를 감싸게 된다. (=주변의 content가 변형됨)
  - absolute positioning: normal flow로부터 제외됨, 그러나 주변 content, element에 영향 주지 않음
- stacking context: 요소가 페이지에 렌더링되는 순서. 보통 z-index로 설정하나 opacity 등 다른 CSS property 도 영향을 줄 수 있다는 점에 주의
