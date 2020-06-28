# CSS기술

</br>

#### :book:text-align속성은 블록 요소에만 적용할 수 있는 속성**이며 블록 요소 안의 **텍스트 뿐만 아니라 인라인 요소도 같이 정렬**된다

#### :book:horizontal : 수평  vertical :수직

#### :book:글자 수직정렬하는법 :    `line-height: 70px`( 줄간격)



</br>

## Margin상쇄 현상★(보충)

- https://thrillfighter.tistory.com/479

- https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing

- 발생하지 않는 경우

    1. float효과가 지정되어있거나 
    2. position효과로 절대값 기준으로 위치가 지정되는 경우 
    3. display속성이 인라인 속성인경우 마진겹침현상이 발생하지 않는다.

- 좌우로는 발생하지 않고 **위아래로만 발생**한다

- 서로의 margin값이 겹칠 때 **더 큰 값을 적용**한다

- 부모와 자식관계에서 부모에게 **시각적효과가없을때(border,글자 등..,컬러(X))** margin값이 합쳐진다

</br>

## 헷갈림

1. **`background-clip`속성** : 배경색을 어디까지 칠 할지 지정하는 속성
2. **`box-sizing` 속성** : 요소의 크기를 border까지 합칠지 contnet만 포함할지 결정하는 속성

</br>

## background-image 두가지를 한번에 쓰는법(CSS기술.md)

```scss
//url 두개를 연달아쓰면 두개다 적용된다 
// 조건 1. 투명도가 있는 .png 파일이어야 한다.
// 조건 2. 두파일 중에 하나만 투명도가 있을경우 투명도 있는파일이 앞에와야한다 
background-image: 
url("resources/img/kakao.jpg"),url("resources/img/kakao2.png");
```

</br>

## white-space, text-overflow, word-wrap, word-break 속성 정리

-   https://ahribori.com/article/5a0994626c9eef13d882e379

</br>

