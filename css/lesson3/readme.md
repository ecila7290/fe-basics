# 문단과 목록 스타일
## text-align
텍스트의 정렬 방식 지정. justify는 왼쪽과 오른쪽 모두 정렬한다.
- letter-spacing: 자간 조절
- word-spacing: 단어 간격
- line-height: 줄 높이

px, em, rem 등 사용할 수 있지만, em/rem처럼 상대적인 값을 넣어주는 것이 바람직하다.
- text-indent: 들여쓰기, 내어쓰기(음수값)

## list-style
ul, ol의 bullet, 숫자 스타일을 지정할 수 있다. 모양을 자유롭게 바꿔서 ol에 bullet을, ul에 숫자를 넣도록 할 수도 있다. <br>

- emmet '^': 한 단계 위로 갈 수 있다.
`ul>li{ul 아이템 $}*3^ol>li{li 아이템 $}*3`