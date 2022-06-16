# 사용자로부터 입력 받기 II
## input type=text일 때 속성들
- placeholder
- maxlength: 넘어가면 지워짐
- minlength: 위반시 submit 거부됨

## search type
브라우저마다 다르지만 대부분 오른쪽에 X표시가 있어 한번에 지울 수 있다.

## input type=number일 때 속성들
- min, max: 데이터 타입마다 형식이 달라진다.
- step: 간격

## input type=checkbox일 때 속성들
- checked: 체크박스/라디오일 때  미리 체크됨 여부
- name: (일반적인 기능 + 라디오에서)옵션들의 그룹
- value: 각 옵션마다 실제로 넘겨질 값

name으로 그룹을 맞춰주지 않으면 중복선택이 가능한 것처럼 보이게 된다.

## 기타 인풋 타입
- file
  - accept: 받아들일 수 있는 파일 형식
  - multiple: 여러 파일 업로드 가능 여부
- hidden
사용자에게 보여주지 않아도 될 정보를 같이 전송해야 할 경우 사용
- email
email 형식이 아니면 제출했을 때 에러
(철저하지는 않으므로 js에서 처리)

## 공통 속성
- value: 미리 값이 들어가 있음
- autofocus: 커서가 미리 들어가 있음
- readonly: 읽기만 가능 but **값 전송됨**
- required: 작성 안하면 에러
- disabled: 입력 불가 and **전송 안됨**