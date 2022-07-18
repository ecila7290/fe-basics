# Advanced Responsive Design

## Desktop-first vs Mobile-first

max-width min-width media query가 적용되는 한계. media query는 소스코드 순서에만 영향을 받기 때문에 항상 맨 마지막에 위치해야 한다.(+ max-width는 큰 것->작은 것 순서로)

## brakpoints

어디에 media query를 적용할지.
일반적으로는 기기별로 유사한 사이즈를 모으고 기기의 종류(모바일, 패드, 노트북 등)를 기준으로 breakpoint를 잡는다. 가장 완벽한 방법은 기기에 대한 고려 없이 content를 기준으로 코드를 작성하고, 디자인이 깨지는 시점에 이를 위한 breakpoint를 추가하는 것이지만 현실적으로 실행하기 어려운 방법.

https://gs.statcounter.com/screen-resolution-stats#monthly-202106-202206-bar 에서 세계적으로 많이 사용되는 스크린 해상도를 볼 수 있다.

## Sass mixin

미디어쿼리를 사이즈별로 필요한 요소에 적용하는 방식은 프로젝트가 커질수록 수정이 어려워진다. 따라서 sass mixin을 활용해 좀더 손쉽게 미디어쿼리를 적용할 수 있다.

## @content & @if

mixin을 적용할 때 @content를 통해 스타일 블록을 추가하도록 할 수 있다.

## 기타

- rem은 미디어쿼리에서 의도대로 동작하지 않는 경우가 있어 em을 사용한다.
- sizzy에서 기기별로 미디어쿼리가 적용된 화면을 볼 수 있다.

# Responsive Image

단순히 화면 크기에 따라 이미지 사이즈를 변경하는 flexible image와는 달리, 사용자의 화면 크기에 맞추어 적절한 용량의 이미지 데이터를 제공한다.

## Art direction and density switching

### srcset attribute on img, source element

src대신 srcset을 넣고 `<img srcset="img/logo-green-1x.png 1x, img/logo-green-2x.png 2x"`처럼 이미지 파일 경로와 density를 넣어주면 화면 해상도에 따라 자동으로 적합한 이미지를 보여준다.

### picture element

화면 크기에 따라 다른 이미지를 넣어줄 수도 있는데, 이 때는 picture를 사용하고 태그 안에 source 태그를 추가한다. 그리고 img태그도 같이 추가해서 source에 에러가 발생했을 때를 대비한다.  
source태그에는 srcset 속성과 media 속성을 넣는데, 그중 media 속성은 media query와 같이 max-width 등의 조건을 넣어줄 수 있다.  
`<source srcset="img/logo-green-small-1x.png 1x, img/logo-green-small-2x.png 2x" media="(max-width: 37.5em)">`

## 기타

- media query는 and, not, only를 사용해 여러 조건을 결합할 수도 있다. or 조건은 콤마를 사용한다.

# Browser support

## @supports

브라우저가 기술된 조건의 요소를 지원하면 적용하고, 그렇지 않으면 적용하지 않는다.
media query와는 다르게 or는 or로 입력해야 한다.

## backdrop-filter

요소 뒤의 영역에 다양한 효과를 줄 수 있음. blur와 더불어 색상 변화도 가능. 요소 뒤 모든 영역에 적용되기 때문에 효과를 확인하려면 요소나 배경을 어느정도 투명하게 해야 함.

# Final considerations

- 드래그 색상 변경: `::selection` pseudo element를 드래그했을 때의 스타일을 변경할 수 있다.
- only screen: media query가 스크린에서만 적용되도록 한다. (프린트 시에는 적용 안되는 등.)
- `<meta name="viewport">`: 반응형 디자인을 위해서는 해당 태그에 `content="width=device-width, initial-scale=1.0"` 속성을 넣어야 한다.
-
