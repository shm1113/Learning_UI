# CSS스타일

- ## 크기단위

    #### 고정 크기 단위

    - 부모 요소나 기타 요소들에 영향을 받지 않고 **<u>일정한 크기를 유지하는 단위</u>**
    - **`in`** : 인치를 뜻한다  사용자나 운영체제의 설정에 따른 논리적인 크기
    - **`px`** : 화소단위, 정확하게 배치하거나 크기를 잡을 때 사용하기 좋다
    - **`pt`** : 포인트 1pt= 1/72in
    - **`pc`** : 파이카 1pc= 1/6in
    - **`cm`** : 논리 센티미터 1in= 2.54cm
    - **`mm`** :논리 밀리미터 1in = 25.4mm

    #### 가변 크기 단위

    - **상대적인 크기를 가지는 단위**
    - **`em`**
        - 해당 태그의 font-size값을 상속받아 정해진다,해당 태그에 font-size가 없을 경우 부모 font-size를 기준으로 한다.[ 지정한 글자 크기를 기준으로 배율을 조정한다
        - 2em일 경우 부모 요소의 글자크기의 2배, 글자크기에 따라 레이아웃을 유동적으로 만들 때 사용한다
    - **`ex`** 
        - 요소에 들어있는 폰트의 소문자'x'의 높이를 기준으로한 비율
        - 1em은 1ex보다 약 두배크다 , 거의 쓰지 않는다
    - **`rem`**
        -  root em 이라는 뜻으로 HTML문서의 root 요소인 <html> 태그를 나타내며 루트 태그의지정된 font-zie크기를 기준으로 상대적인 값을 가지게 된다
    - **`%`** : 요소의 크기의 비율을 따져 크기를 가진다 

</br>

## 폰트

- **설명**

    - **text-align속성은 블록 요소에만 적용할 수 있는 속성**이며 블록 요소 안의 **텍스트 뿐만 아니라 인라인 요소도 같이 정렬**된다

- font style 하나하나쓸 때는 순서가 상관없지만 한번에 줄 때는 상관있다

- **font style 한번에 줄 때 순서** 

- ```scss
    //font-style,font-variant,font-weight,font-size/line-height,fontfamily
    //font-family는 반드시 넣어줘야한다 
    font: italic small-caps bold 12px/1.6 arial,-77 -elvetica, sans-serif
    ```

    

</br>

## cursor속성

- **기본 속성**

- https://developer.mozilla.org/ko/docs/Web/CSS/cursor

    ```css
    cursor : pointer;  /*링크를 나타내는 포인터
    ...많다*/
    
    ```

- url을 사용해서 **임의의 이미지**를 줄 수도 있다.

- https://developer.mozilla.org/ko/docs/Web/CSS/cursor/Using_URL_values_for_the_cursor_property

- ```css
    cursor: [<url>,]* keyword;
    ```



## z-index속성

- 위치 지정요소와 , 그 자손 또는 하위 플렉스 아이템의 z축 순서를 지정한다 
- 더큰 값이 위로 올라온다
- 위치 지정 요소(position이 static 외의 다른 값인 요소)의 박스에 대해 z-index속성은 다음 항목을 지정한다
    - 현재 쌓임 맥락에서 자신의 위치
    - 자신만의 쌓임 맥락 생성여부

```css
z-index: 2;
```

</br>

## 텍스트 관련 스타일 

#### 폰트

- ##### **설명**

    - **text-align속성은 블록 요소에만 적용할 수 있는 속성**이며 블록 요소 안의 **텍스트 뿐만 아니라 인라인 요소도 같이 정렬**된다

- font style 하나하나쓸 때는 순서가 상관없지만 한번에 줄 때는 상관있다

- **font style 한번에 줄 때 순서** 

- ```scss
    //font-style,font-variant,font-weight,font-size/line-height,fontfamily
    //font-family는 반드시 넣어줘야한다 
    font: italic small-caps bold 12px/1.6 arial,-77 -elvetica, sans-serif
    ```

</br>

-   **`line-height: x%` :** 줄 간격,숫자입력시(em단위)

-   **`text-decoration : underline` :**밑줄
    
-   **`overline | line-throught | underline | none`**
    
-   **`text-align : center`:** 텍스트 정렬

    -   **`left | right | center | justify`**

    -   ##### :star: 블록 요소에만 적용할 수 있는 속성이며 블록 요소 안의 텍스트 뿐만 아니라 인라인 요소도 같이 정렬된다

-   **`letter-spacing :10px`:**  글자와 글자간의 간격을 조정한다 

-   **`font-size`:** 글자크기를 지정한다

-   **`text-indent` :**들여쓰기 효과를 지정한

</br>

## 온라인 font 가져오기 

1. http://blog.naver.com/PostView.nhn?blogId=pungwun&logNo=220367365537

2. 원하는 폰트파일(.ttf)를 다운받는다 

3. ```css
    @font-face{		 
                font-family: "Goyang";	//사용할 글꼴
                src: url("resources/css/Goyang.ttf") format("truetype");	//글꼴의 위치,폰트확장자에 따른 파일 형식을 입력해준다 
            }
    #goyang{
                    font-family: "Goyang";
                    font-size:30px;
            }
    ```

</br>

## background 

- ```scss
    <style type="text/css">
          h1{
              background-image: url("resources/img/kakao.jpg");   	//해당 이미지파일을 가져온다
              background-repeat: no-repeat;    //배경이미지 반복 여부
              background-attachment: fixed;    //배경이미지 스크롤 여부
    /*scroll : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미					지는 스크롤되지 않습니다.
    fixed : 움직이지 않습니다.
    local : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미지도 스크롤됩		니다.
    initial : 기본값으로 설정합니다.
    inherit : 부모 요소의 속성값을 상속받습니다.	*/
          }
        p{
          background-image: url("resources/img/kakao2.png");
            background-position: center;	//배경이미지의 시작위치를 지정한다
        }
    </style>
    ```

</br>

## 박스

#### 꿀팁!!

- <u>시작할 때 margin 과 padding은 0으로 만들어 놓고 시작해라!!</u>

#### `margin` 속성

- 요소의 테두리 바깥쪽에 투명한 공간
- auto(기본값), 길이, %로 속성값을 줄 수 있다.
- margin의 설정값은 1~4개로 줄 수 있다
- 한번에 줄 때 순서: 상 , 우 , 하 , 좌

#### :star:Margin상쇄 현상(CSS기술.md)

- https://thrillfighter.tistory.com/479

- https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing

- ##### 발생하지 않는 경우

    1. float효과가 지정되어있거나 
    2. position효과로 절대값 기준으로 위치가 지정되는 경우 
    3. display속성이 인라인 속성인경우 마진겹침현상이 발생하지 않는다.

- 좌우로는 발생하지 않고 **위아래로만 발생**한다

- 서로의 margin값이 겹칠 때 **더 큰 값을 적용**한다

- 부모와 자식관계에서 부모에게 **시각적효과가없을때(border,글자 등..,컬러(X))** margin값이 합쳐진다


#### `padding`속성

- 요소의 테두리 안쪽과 콘텐츠와의 사이에 투명한 공간을 확보한다 

#### `box-sizing` 속성

- 레이아웃을 정할 때 box를 content에 맞출지 border에 맞출지를 먼저 결정한 후에 통일된 레이아웃을 설계하는 것이 중요한데 이러한 것을 box-sizing속성으로 결정한다 

- ##### **`content-box`** 

    - width와 height 속성이 <u>content의</u> 가로와 세로의 길이를 설정하도록한다 (기본값)

- ##### **`border-box`**

    - width와 height속성이 <u>content와 padding과 border의 두께</u>까지 합친 값으로 설정한다 

</br>

## float

- float 속성은 웹 개발자가 텍스트 열 내부에 float하는 이미지를 포함하고, 아울러 **해당 이미지의 좌측 우측 주변으로 텍스트를 둘러싸는 간단한 레이아웃을 구현할 수 있는속성**

- **`inherit`** :부모 요소에서 상속

- **`left`**: 왼쪽에 부유하는 블록 박스를 생성하고 페이지 내용은 박스 오른쪽에 위치하며 위에서 아래로 흐름

- **`right`** : 오른쪽에 부유하는 블록박스를 생성하고 페이지 내용은 왼쪽에 위치하며 위에서 아래로흐름 

    - 이후 요소에 clear 속성이 있으면 페이지 흐름이 달라짐
    - none이 아니라면(left,right) display속성은 무시된다

- **`none`**: 요소를 부유 시키지 않음

    ```scss
    float: left;  //자신의 사이즈만큼만 크기를 차지하고 나머지내용을 연결해준다 
    ```

## clear속성

- float에 의해 변화된 박스의 흐름을 원상태로 돌린다 
    - **`both`** : 양쪽  float 모두를 지운다
    - **`left`**:  왼쪽 float를 지운다
    - **`right`**:  오른쪽 float를 지운다

</br>

## display속성

- 요소를 표시하는 방법을 지정하는 속성 
- **크기순서** :  block > inline-block > inline
- **`none`** : 보이지않음   ---- (visibility 속성을 hidden으로 설정한것과 달리,영역을 차지하지 않는다)
- **`block`** 
    - 블록 박스(div, p, h, li) 
    - 가로영역을 모두 채우며, block요소 다음에 등장하는 태그는 줄바꿈이 된 것처럼 보인다.
    - **block요소 뒤에 등장하는 태그가 그 이전 block 요소에 오른쪽에 배치될 수 있어도 항상 다음줄에 렌더링** 된다 
- **`inline`** 
    -  인라인 박스(span, b, i, a)
    -  block과 달리 줄바꿈이 되지 않는다 
    -  <u>**width와 height를 지정할 수 없다**</u>
    -  글자나 문장에 효과를 주기 위해 존재하는 단위라고 할 수 있다.
- **`inline-block`** 
    -  block과 inline의 중간 형태 
    -  **줄바꿈이 되지 않지만 width와 height를 지정할 수 있다.**
- **`flex`** :CSS3에 새로 생긴 값으로 블록-레벨의 flex 컨테이너처럼 요소를 표현한다 

</br>

## visibility속성

- 요소를 **보여주거나 숨기도록 하는 속성**
- **기본적으로 값이 상속된다** 
- **`visible`** : 박스가 보여진다
- **`hidden`** : 박스가 **보이지는 않지만 공간은 확보**해서 레이아웃에 영향을 미친다
- **`collapse`** : 내부 테이블 객체(행,행그룹,열,열그룹)에 적용된다, hidden과 유사하다,공간을 차지하지 않는다
- **`inherit`** : 부모 요소의 값을 상속

</br>

## display: none' vs 'visibility: hidden' 차이점(CSS기술.md)

언뜻 보면, 이 두 가지 속성은 거의 같아 보입니다. 둘 다 요소를 숨기는 것이죠.

하지만, 이 둘은 약간의 차이가 있습니다. 가장 큰 차이는 **`display:none`**은 해당 요소가 **흔적도 없이 사라지는** 반면,**`visibility:hidden`**은 해당 요소의 **영역을 남겨 놓습니다**. 그러니까 보이지는 않지만, 해당 요소의 영역 만큼 빈 공간을 그대로 보여줍니다.

</br>

## overflow속성

- 콘텐츠가 요소의 박스를 넘칠 때 표현방법을 지정하는 속성
- **`visible`**: 넘치는 컨텐츠를 자르지 않고 요소 **박스를 넘어 표시(****기본값**)
- **`hidden`** : 넘치는 컨텐츠를 **자르고 보이지 않게 한다** 
- **`auto`**  : **스크롤바가 위아래**만생김
- **`scroll`**: **스크롤바가 위아래 양옆** 생김

## text-overflow속성

- 요소 내에 문자열의 넘침 현상을 처리하는 표현방법
    - **`clip`**: 텍스트를 **잘라낸다**
    - **`ellipsis`**: 텍스트가 잘렸다는 것을 표현하기 위해 **말줄임표(...)를 표시**
    - **`string`**: **지정된 문자열을 출력**
- **조건**
    - white-space: nowrap(자동줄바꿈이 되지 않은 텍스트에 대해서 정의하는 속성이기 떄문에 )
    - width가 지정되어야함(즉 display속성은 block or inline-block이어야함)
    - overflow 속성이 visible 말고 다른 속성으로 지정되어야 함(hidden,scroll,auto...등)

</br>

## positon속성

- 태그들의 위치를 지정하는 속성
- **`static`** :기본값으로 따로 써주지 않아도 된다 **,차레대로 왼쪽에서 오른쪽, 위에서 아래로 쌓인다** 
- **`relative`**: **원래 위치(static) 에서** 얼만큼 움직이는지,**top,left,right,bottom을 사용**한다
- **`absolute`**
    - static속성을 가지고 있지 않은 **부모(relative,absolute,fixed)의 위치(**나를 감싸고있는태그)를 **기준**으로 결정한다
    - 만약 부모 중에 **relative,absolute,fixed가 없다면** 가장위의 태그**(body)가 기준**이 된다
    - :star:**absolute가 되면 div(block요소)여도** width: 100% 가 아니다(**한줄을 다차지하지 않고 인라인처럼 줄바꿈이 일어나지 않는다**)
- **`fixed`**
    -  브라우저 기준에서 얼만큼 움직이는지 
    -  **스크롤 해도 위치가 고정이다**
    -  **absolute와 마찬가지로 div(block요소)여도 width:100%가 아니다**

</br>

## border 

- 요소의 테두리를 설정하는 속성

- border 한번에 작성하는법

    - ```scss
        border-width, border-style, border-color //순으로 작성한다 ,생략가능
        ```

- **`border-style`**

    - `solid(기본값)/none/dashed/dotted/double/grove/ridge/inset/outset/hidden`

- **`border-radius`**

    - CSS3에 추가된 속성으로 **테두리 모서리에 반영될 반지름을 지정**한다 

    - 하나만 적용하면 네 모서리 모두 적용되고 ,네 모서리 따로줄 수 있다.

    - ```scss
        border-radius: 50px 50px 50px 50px; 
        ```

        

- **`border-collapse`** (table태그)

    - 표의 칸종류를 조정하는 속성
    - 표의 테두리가 중복되는 부분을 축소할지 분리할 지 결정하는 속성
    - **`collapse`**(합침), **`separate`**(나눔)**(기본값)** 속성을 줄 수 있다

</br>

## background속성

#### background-size 속성

- **`cover`** : 화면을 가득 채운다 

- <u>**배경 두가지를 한번에 쓰는법**</u>(CSS기술.md)

    ```scss
    //url 두개를 연달아쓰면 두개다 적용된다 
    // 조건 1. 투명도가 있는 .png 파일이어야 한다.
    // 조건 2. 두파일 중에 하나만 투명도가 있을경우 투명도 있는파일이 앞에와야한다 
    background-image: 
    url("resources/img/kakao.jpg"),url("resources/img/kakao2.png");
    ```

#### background-clip속성

- **배경을 어디까지 색칠할지 지정하는 속성**
- `**border-box**` :(기본값) border 즉 테두리 영역까지 배경을 칠한다 
- `**padding-box**` : padding 영역에까지 배경을 칠함
- `**content-box**` : content즉 내용 영역까지 배경을 칠함 

</br>

## text-shadow 속성

- 글자에 그림자를 부여하는 속성 

- ```CSS
    text- shadow : offset-x offset-y blur-dadius color | none | initial | inherit
    ```

- offset-x : 그림자의 수평거리를 지정 

- offset-y : 그림자의 수직 거리를 지정

- blur-radius : 흐림 정도를 정한다 (선택사항, 정하지 않으면 0)

    ```css
      #txtshd{
                text-shadow: 1px 2px #ccc;       }
    ```

</br>

## word-wrap속성

- 박스안에 글자를 쓸 때 범위를 벗어날 경우 자동으로 **박스 사이즈에 맞게 글자를 배열**해주는 속성 
- word-wrap이 가능한 요소
    - height나 width를 지닌 인라인 요소
    - 블록요소이거나,절대적 위치의 블록요소

</br>

## 다단(단락)편집

- http://tcpschool.com/css/css3_expand_multicolumn
- 칸수 또는 사이즈 둘 중 하나만 가능하다

```scss
     p{
            column-count:3;	//나눌칸수
         	column-width: 100px; //나눌사이즈
            column-gap: 20px;	//단과단사이의 거리
            column-rule: 2px dotted red;//단을 나누는 선 스타일 
          column-span : all //몇 개의 칼럼을 병합하여 표현할지를 설정한다
        }
```



</br>

## 브라우저마다 다른CSS적용 가능하다

```scss
-webkit-border-radius: 50px 50px 50px50px;
-moz-border-radius: 50px 50px 50px 50px;
-ms-border-radius: 50px 50px 50px 50px;
-o-border-radius: 50px 50px 50px 50px;
/*
	webkit : 구글, 사파리
	moz : 파이어폭스
	ms : 익스플로러
	o : 오페라
*/
```

****