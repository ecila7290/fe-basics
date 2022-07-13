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

rem은 미디어쿼리에서 의도대로 동작하지 않는 경우가 있어 em을 사용한다.

## 