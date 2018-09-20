## Sass magic: Operators

.left-float.col-3.center.text-xl[
#### Calculation
`+`

`-`

`*`

`/`

`%`
]

--
count: false

.left-float.col-3.center.text-xl[
#### Comparison

`>`

`>=`

`<` `<=`
]

--
count: false

.left-float.col-3.center.text-xl[
#### Equality

`==`

`!=`

]

???
Can evaluate all data types, not just numbers

---

## Sass magic: Operator example
### What we're going for

.center.img-w-75[
  ![slideshow screenshot](03/slideshow-example.png)
]

---
count: false

## Sass magic: Operator example
### What we're going for

.center.img-w-40[
  ![slideshow screenshot](03/slideshow-example.png)
]

```html
<div class="slideshow">
  <img alt="This is a placeholder image" class="slideshow__img" src="https://placebeyonce.com/500-500">
  <button class="slideshow__button slideshow__button--prev" type="button"></button>
  <button class="slideshow__button slideshow__button--next" type="button"></button>
</div>
```

---

## Sass magic: Operator example

```scss
@mixin arrow() {
  @include size(20px);
}
```

???
A mixin inside a mixin? No problem!

---
## Sass magic: Operator example

```scss
@mixin arrow() {
  position: absolute;
  top: calc(50% - 10px);
  @include size(20px);
}
```

???
- maybe we can't use flexbox, so let's postion the arrows absolutely
- the top calc seems like a magic number, but not b/c???

---

## Sass magic: Operator example

```scss
@mixin arrow() {
  // prev code plus this
  &::before {
    background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="60" height="100" version="1">
      <path d="M10 0l50 50-50 50L0 90l40-40L0 10z" /></svg>') no-repeat center/contain;
    content: '';
    display: block;
  }
}
```

--
count: false

.center[
  ![arrow svg](03/arrow.svg)
]

???
This is what that SVG looks like. Going forward, I'm going to shorten that bit of the code to keep things simple.

---

## Sass magic: Operator example

```scss
@mixin arrow() {
  &:hover,
  &:focus {
    cursor: pointer;
    opacity: 0.6;
  }
}
```

---

## Sass magic: Operator example

```scss
@mixin arrow() {
  position: absolute;
  top: calc(50% - 10px);
  @include size(20px);
  &:before {
    background: url(SVG) no-repeat center/contain;
    content: "";
    display: block;
    @include size(20px);
  }
  &:hover,
  &:focus {
    cursor: pointer;
    opacity: 0.6;
  }
}
```

---

## Sass magic: Operator example
### Great, we got a button

<iframe height='520' scrolling='no' title='Mixin: Slider Arrows (updated. single arrow)' src='//codepen.io/angeliquejw/embed/gdzqVa/?height=520&theme-id=15346&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/angeliquejw/pen/gdzqVa/'>Mixin: Slider Arrows (updated. single arrow)</a> by Angelique (<a href='https://codepen.io/angeliquejw'>@angeliquejw</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>

---

## Sass magic: Operator example
### What we're going for

.center.img-w-50[
  ![slideshow screenshot](03/slideshow-example.png)
]

???
Could use two images. But that's 2 resources, 2 downloads and we don't gotta

--
count: false

```html
<button class="slideshow__button slideshow__button--prev" type="button"></button>
<button class="slideshow__button slideshow__button--next" type="button"></button>
```

---

## Sass magic: Operator example

```scss
@mixin arrow($direction) {

}
```

---
count: false

## Sass magic: Operator example

```scss
@mixin arrow($direction) {

  @if $direction == right {
    right: 0;
  }

}
```

--
count: false

.right[
  ![arrow svg](03/arrow.svg)
]

---

## Sass magic: Operator example

```scss
@mixin arrow($direction) {

  @if $direction == right {
    right: 0;
  } @else if $direction == left {
    left: 0;
  }

}
```

--
count: false

.left[
  ![arrow svg](03/arrow.svg)
]

---
count: false

## Sass magic: Operator example

```scss
@mixin arrow($direction) {

  @if $direction == right {
    right: 0;
  } @else if $direction == left {
    left: 0;
    transform: rotate(180deg);
  }

}
```

.left[
  ![arrow svg](03/arrow2.svg)
]

---

## Sass magic: Operator example

```scss
@mixin arrow($direction) {

  @if $direction == right {
    right: 0;
  } @else if $direction == left {
    left: 0;
    transform: rotate(180deg);
  }

}
```

```scss
.slideshow__button--prev {
  @include arrow(left);
}
.slideshow__button--next {
  @include arrow(right);
}
```

---

## Sass magic: Operator example

```scss
.slideshow__button--prev {
  @include arrow();
}
```

???
What happens when we do this?

---
background-image: url(https://media.giphy.com/media/zH2UJxZ0OPDxu/giphy.gif)
class: bkgd-cover, center, middle

--
count: false

.bkgd-color[
  # Does not compute
]

---

## Sass magic: Operator example

.col-2.left-float[
```scss
@mixin arrow($direction:right) {

  @if $direction == right {
    right: 0;
  } @else if $direction == left {
    left: 0;
    transform: rotate(180deg);
  }

}
```
]

--
count: false

.col-2.right-float[
```scss
@mixin arrow($direction:right) {

  @if $direction == left {
    left: 0;
    transform: rotate(180deg);
  } @else {
    right: 0;
  }

}
```
]

---

## Sass magic: Operator example

<iframe height='520' scrolling='no' title='Mixin: Slider Arrows (updated)' src='//codepen.io/angeliquejw/embed/preview/XPqooN/?height=520&theme-id=15346&default-tab=css,result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='https://codepen.io/angeliquejw/pen/XPqooN/'>Mixin: Slider Arrows (updated)</a> by Angelique (<a href='https://codepen.io/angeliquejw'>@angeliquejw</a>) on <a href='https://codepen.io'>CodePen</a>.
</iframe>
---

## Sass magic: Control directives

--
count: false

.left-float.col-2.center.text-xl[

  `@if`

  `@else if`

  `@else`

  ]

--
count: false

.right-float.col-2.center.text-xl[

  `@each`

  `@for`

]

???
- each: For each item in a list or map
- for: For this many instances
