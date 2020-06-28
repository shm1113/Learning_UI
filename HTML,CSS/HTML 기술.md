# HTML 기술

</br>

#### :book: block요소는 text-align영향을 안받기 때문에 display를 inline-block으로 변환해주어야 한다

</br>

#### :book:inline-block 보다 block요소가 범위를 더 꽉 채워준다

</br>

#### :book:요소가 켭치려면 무조건 absolute가 되야 하는건가 ??

</br>

#### :book:inline요소는 글자에 딱 맞는 크기만 가진다 

</br>

#### :book:**`:book:a`**태그 밑줄 없애는법 text-decoration:none;

</br>

#### :book:이미지 버튼과  이미지 링크를 잘 구분하자

</br>

## 가로나열하는 2가지 방식

1. #### float

2. #### inline-block

</br>

## 가운데정렬 

- #### margin : 0 auto  (0 auto 0 auto와 동일하다)

- #### 안되는 경우

    - ##### width연산이 불가능 하면 가운데 정렬을 할 수 없다

        - 해결책은 overflow:hidden

    - ##### inline속성의 태그인 경우

        - display:block을 해주면 된다

</br>

## 외부 폰트 가져오는 법

- #### @font-face로 폰트 다운로드

    - [https://webisfree.com/2017-09-04/css-%ED%8F%B0%ED%8A%B8-%EB%B0%94%EA%BE%B8%EA%B8%B0-font-face%EB%A5%BC-%EC%A0%81%EC%9A%A9%ED%95%98%EA%B8%B0](

</br>

## box요소 그림자

- ```css
    box-shadow: none | h-shadow v-shadow blur spread color | inset | initial | inherit ;
    출처: https://mini-sugar.tistory.com/54 [작은설탕의 달콤한 인생로그]
    /*
    	가로 : 음수=좌측 , 양수 =우측
    	세로 : 음수=위쪽 , 양수 =아래쪽
    	blur :  흐릿한 효과 길이
    	spread: (optional) 그림자를 확장하는 크기(size)입니다. 이 값이 클 수록 원			본 그림자보다 설정값만큼 그림자가 커지며, 음수도 사용가능합니다. (음			  수는 그림자가 작아지겠죠?)
    	color: 색깔
    	inset: 그림자를 안쪽으로 만들어 준다
    	initial : 현재 설정을 HTML문서의 기초값으로 만든다
    */
    ```

</br>

## div태그안에 img태그 맞추기

```css
   overflow: hidden;
	
```

</br>

## text-overflow

- **clip :** 기본값,텍스트를 자름
- **ellipsis :** 잘린 텍스트를 생략 부호(...)로 표시함

</br>

## label태그는 for속성

- 값을 id와 묶어 주거나 감싸면 input태그와 연결 할 수 있다.