# 사용자로부터 입력 받기 III
## textarea
- cols: 글자수 단위의 너비
- rows: 표시되는 줄 수

기본값을 넣으려면 value가 아닌 태그 안에 입력해야 한다.
placeholder는 가능.

## 옵션들을 사용하는 태그
- select
multiple: 다중 선택 가능. 드롭다운 대신 상자로 표시

- option
  - selected: 미리 선택됨 표시
  - value: 실제로 전송될 값

- optgroup
그룹을 만들어 선택할 수 있도록

- input
list: 연결할 datalist의 id
datalist: 미리 정해놓은 값. 다른 값을 입력할 수도 있음

## 정도를 표현하는 태그
- progress
  - max: 기본 1
  - value: 진행된 정도. js로 변경
- meter: 고정된 수치를 보여줄 때
  - min, max
  - low, high: 전체 범위를 3등분하는 두 수치
  - optimum: 이상적인 값. 3개의 구간 중 한 곳에 위치. 이 값보다 크거나 같으면 안좋아 보이는 색으로 변함
  - value: 실제 전송되는 값