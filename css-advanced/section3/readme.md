# Sass
## Variables & nesting
- `$var-name: value;` 형식으로 변수를 지정해 값을 할당할 수 있다.
- 하위 요소를 nesting 방식으로 입력할 수 있다.
- nesting은 제한이 없어서 요소의 pseudo-class도 하위로 nesting할 수 있다. 다만 `:first-child`만 붙이게 되면 `navigation li :first-child`와 같은 코드가 되어 의미가 없어지므로 앞에 '&'를 붙여준다.
- 한 요소 안에서 nesting으로 동시에 여러 pseudo-class를 적용하게 할 수 있다.
- sass의 내장함수인 darken()/lighten()을 사용하면 간단하게 색깔을 더 어둡게/밝게 할 수 있다.(비율 지정 가능)

## Mixins, extends and functions
### Mixins
연관성은 없지만 코드가 겹치는 선택자가 있을 때 사용. 선택한 css 양식이 적용되도록 하는 커스텀 함수. 매개변수도 지정할 수 있다.
```sass
@mixin mixin-name($arg) {
  some css sutff...
}

.class {
  @include mixin-name(some-arg)
}
```

### Functions
일반적인 프로그래밍 언어에서 만들 수 있는 함수처럼 (스타일 대신)값을 리턴하도록 한다.
```sass
@function name($arg) {
  @return $arg * 2
}
```

### extend
연관성이 있는 선택자를 묶기 위해 사용
```sass
%name {
  styles here...
}

.some-class {
  @extend name
}
```