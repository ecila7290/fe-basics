# 표 만들기
- table	테이블	
- caption	표 설명 또는 제목으로,	선택사항
- tr	테이블의 행	
- td	테이블의 데이터 셀	

## 더 상세한 내용의 테이블
- thead	테이블의 헤더 부분	&lt;tbody&gt; 앞에 와야 함
- tbody	테이블의 본문	본 내용을 담음
- tfoot	테이블의 푸터 부분	&lt;tbody&gt; 뒤에 와야 함
- th	열 또는 행의 헤더	scope 속성으로 row, col 중 선택

## 테이블 병합
- colspan	열 병합
- rowspan	행 병합
예전에는 레이아웃으로 사용하기도 했지만 현재는 절대 사용해서는 안됨

## 기타
- colgroup 표의 열을 묶어서 속성 부여. caption보다는 뒤, 그 외 요소보다는 앞에 와야 함
- col span 속성으로 묶을 열 수 지정