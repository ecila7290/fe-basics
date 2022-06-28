# Flex 레이아웃
## flex (container)
- inline-flex: 컨테이너의 요소를 inline으로 만들어 다른 요소가 옆에 올 수 있도록 한다.
- flex-direction: row는 행부터 채움. column은 열부터 채움. 여기서 결정한 축이 메인 축이 되고 그 반대가 수직 축으로 정의. 이 값에 따라 justify-content, align-items, align-content 등의 속성들이 작용할 방향이 결정된다.
- justify-content: 메인 축에서 아이템을 정렬할 방식 결정
  - flex-start, flex-end: start, end도 있지만 reverse에 영향 받지 않으므로 flex붙은 것으로 쓰기
- flex-wrap: 내부 요소의 개수 x 길이가 컨테이너를 넘어갈 때, 넘어간 것들을 여러줄에 걸쳐 나열하게 된다.
- align-items: 수직 축에서 아이템을 정렬할 방식 결정. 여러 줄이 되면 align-content를 통해 다양한 방식으로 정렬 가능
- gap: 아이템간의 간격. 가로/세로 다르게 지정 가능

## flex (inside container)
- flex-basis: 메인 축상의 길이 조절. flex-direction 값에 따라 너비/높이 적용
- flex-grow: 빈 공간을 채울지 여부. 채울 시 다른 아이템의 같은 속성값에 비례해서 공간을 채운다.(공간이 남을 때 내거로 얼마나 더 채울지)
- flex-shrink: 전체 공간이 부족하게 될 때 해당 아이템의 길이가 컨테이너 너비 또는 flex-basis로 지정한 값보다 작아질 수 있는지 지정. 기본 1이고 값이 증가할수록 많이 줄어든다. (공간이 부족할 때 내거를 얼마나 더 줄일지)