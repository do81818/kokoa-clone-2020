# 노마드 코더 코코아톡

## Status Bar CSS

### 가상 선택자

- `element:first-child` : 형제 요소 중 첫번째 요소
- `element:last-child` : 형제 요소 중 마지막 요소
- `element:nth-child` : 형제 사이에서의 순서에 따라 요소를 선택

### CSS hack

No Service 부분이 다른 요소들 보다 상대적으로 크기 때문에 요소의 전체적인 정렬이 흐트러져 있다.

```CSS
.status-bar {
  justify-content: center;
}

.status-bar__column {
  width: 33%;
}

.status-bar__column:nth-child(2) {
  display: flex;
  justify-content: center;
}

.status-bar__column:last-child {
  display: flex;
  justify-content: flex-end;
}
```

각각의 요소에 `width: 33%;` 를 주고 flex를 이용해서 텍스트를 정렬시킨다.(`justify-content`)

---

## Sign Up Screen

- 클래스 이름을 명확하게 지을 것 (부모 요소가 status-bar 라면 status-bar\_\_column 이런식)
- CSS 를 컴포넌트화 해서 쪼개고. style.css 파일에 `@import` 해준다.

### reset.css

기본적인 UserAgent CSS 스타일을 없애버린다.

---

## Log In Form

- `element:not([type="submit])` : () 안의 요소가 아닌 곳에 속성 적용

---

## Navigation Bar

네비게이션 바 하단 고정

```CSS
.nav {
  position: fixed;
  bottom: 0;
  width: 100%;
  box-sizing: border-box;
}
```
