# 사용자로부터 입력 받기 I
## form
|태그 |	설명	|비고|
|---|---|---|
|&lt;form&gt;|	정보를 제출하기 위한 태그들을 포함|	autocomplete 속성: 자동완성 여부 (기본: on)|
|&lt;input&gt;|	입력을 받는 요소|	type 속성을 통해 다양화|
|&lt;label&gt;|	인풋 요소마다의 라벨|	for 속성값을 인풋 요소의 id와 연결. 인풋의 클릭 영역 확장|
|&lt;button&gt;|	버튼|	type 속성에 submit(제출), reset(초기화), button(기본 동작 없음)|

인풋의 클릭 영역 확장 -> label 클릭해도 input으로 간다.

## 폼 안의 요소들 그룹으로 묶기
form 안에 fieldset <br>
legend로 제목 표현<br>
그룹별로 disabled 속성을 지정해서 입력을 비활성화 시킬 수 있다.