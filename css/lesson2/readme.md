# 글자와 텍스트 스타일
## font
- font-style: 글자를 기울일 때 사용
  - italic과 oblique
  italic이 기울여서 '새로' 쓴 서체, oblique는 기존 서체를 기울여 놓은 것 (둘 중 하나만 있으면 있는 쪽이 적용됨)
- font-weight: 글자의 굵기 조절
  - normal / bold 또는 100~900까지의 숫자로 조절
- font-size
  - px: 절대값으로, 픽셀 단위
  - %, em: 100%가 1em. 부모 요소와의 상대적 크기 (중첩된 태그가 있으면 각각 다른 값을 갖게 됨)
  - rem: 최상위(root) 요소인 &lt;html&gt; 요소와의 상대적 크기. 요소 중첩에 영향을 받지 않음
  - pt: 1인치/72. 프린트할 컨텐츠에 사용

## text style
- text-decoration: 밑줄, 취소선, 물결선 등. 선의 형태/색/굵기 등의 디테일도 함께 지정 가능
- text-transform: 알파벳의 대소문자 표시에 사용. HTML, CSS처럼 대문자로 작성된 텍스트에는 적용되지 않음
- text-shadow: 텍스트에 그림자. 