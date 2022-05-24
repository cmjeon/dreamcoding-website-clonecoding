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

## data-

참고 : https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes