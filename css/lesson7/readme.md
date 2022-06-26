# 박스 모델 II
## border
선 굵기, 스타일 색 순서로 지정
- box-sizing: 너비와 높이 값에 padding, border 값을 포함시킬지 결정. content-box(포함X), border-box(포함O)
- border-radius: 모서리를 둥글게 하는데 사용. 완전한 동그라미는 50%.

## overflow
부모 요소보다 높이나 너비가 큰 자식 요소를 어떻게 나타낼지. default: auto
- visible: 자식 요소를 그대로 보여줌 (부모, 자식 요소에 모두 적용해야 한다)
- overflow-x, overflow-y로 따로 지정할 수도 있다.

## box shadow
박스 요소의 그림자를 줄 때 사용
- spread-radius: 그림자가 퍼진 정도. 음수값일 경우 그림자가 박스 크기보다 작아짐
- inset: 있을 경우 그림자가 안쪽(왼쪽위)으로 들어간다