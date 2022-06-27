# 포지셔닝
## position
자식 요소에게 대물림되지 않는다.
- static: 페이지의 흐름에 따르며 top, bottom, left, right, z-index에 영향받지 않는다.
- relative: 원래 위치를 기준으로 top ~ right 속성이 적용. 요소의 위치는 이동하지만 공백의 위치는 유지
- absolute: **static이 아닌**(보통 relative) 첫 번째 부모 요소를 기준으로 top ~ right을 사용하여 위치 조정. 요소는 문서 흐름에서 벗어나 자리를 차지하지 않게됨(->다른 요소를 밀어내지 않고 원하는 자리로 이동)
- fixed: viewport 기준으로, 스크롤에도 영향 받지 않음
- sticky: 요소가 스크롤로 인해 이동을 시작하는 거리를 top ~ right 속성으로 제한

## z-index
static이 안니 요소간의 위아래 배치 순서 지정.
auto는 0이며, 숫자가 클수록 또는 같은 숫자일 경우 나중에 배치된 것이 위로 올라옴.