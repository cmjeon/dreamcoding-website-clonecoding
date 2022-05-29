# 드림코딩 포트폴리오 웹사이트 클론코딩

https://academy.dream-coding.com/enrollments

# note

## css variable

참고 : https://developer.mozilla.org/en-US/docs/Web/CSS/--*

css 에서 '--...' 로 변수를 선언할 수 있음 

```css
.first-list {
    background-color: thistle;
    color: whitesmoke;
    margin-left: 8px;
    --font-size: 32px;
    font-size: var(--font-size);
}
```

부모노드에서 선언한 css 요소에 있는 변수는 자식노드에서 사용할 수 있음

```css
.first-list {
    background-color: thistle;
    color: whitesmoke;
    margin-left: 8px;
    --font-size: 32px;
    font-size: var(--font-size);
}

.first-list li{
    font-size: var(--font-size);
}
```

보통은 root 에서 변수를 선언해서 사용

```css
:root {
    --base-fort-size: 32px;
}
```

calc 로 계산할 수 있음

```css
:root {
    --base-fort-size: 32px;
}
.first-list {
    font-size: calc(var(--base-font-size) * 2)
}
```

미디어쿼리에서 root 를 선언해서 사용가능

```css
@media screen and (max-width: 768px) {
    :root {
        --base-fort-size: 32px;
    }
}
```

## data attributes

참고 : https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes

HTML5 에서 추가된 속성

커스텀속성을 지정할 수 있는 방법

```html
<body>
    <div id="id-div" class="class-div" data-display-name="dream" data-index="1"></div>
    <div id="id-div" class="class-div" data-display-name="coding" data-index="2"></div>
</body>
```

data-display-name 속성의 배경을 변경할 수 있음

```css
[data-display-name='dream'] {
    background-color: beige;
}
```

특정 태그에만 적용 가능

```html
<body>
    <div id="id-div" class="class-div" data-display-name="dream" data-index="1"></div>
    <div id="id-div" class="class-div" data-display-name="coding" data-index="2"></div>
    <span id="id-div" class="class-div" data-display-name="dream" data-index="1">zzzzzzzzz</span>
</body>
```

data-display-name 속성의 배경을 변경할 수 있음

```css
div[data-display-name='dream'] {
    background-color: beige;
}
```

javascript 에서 document.querySelector 를 써서 선택 가능

```js
const dream = document.querySelector('div[data-display-name="dream"]')
console.log(dream.dataset);
console.log(dream.dataset.displayName); // dream
```

## BEM

Block Element Modifier

block__element--modifier

```css
// card1
.card
.card__img
.card__title
.card__description
.card__button

// card2
.card--dark
.card__img
.card__title
.card__description
.card__button--blue
```

component 단위로 작성한다

cards 에 card 가 있는 경우

```css
.cards
.card
.card__title
.card__descriptioin
```

BEM: http://getbem.com/introduction/

BEM 101 by CSS-Tricks: https://css-tricks.com/bem-101/

10 Common Problems And How To Avoid Them:

https://www.smashingmagazine.com/2016/06/battling-bem-extended-edition-common-problems-and-how-to-avoid-them/

## Navbar
 
https://developer.mozilla.org/ko/docs/Web/HTML/Element/img

## box-sizing

https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing
