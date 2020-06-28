# CSS정리

</br>

## CSS란

- **CSS(Cascading style sheet,종속형 시트)정의** : 문서에 스타일을 지정해주는 언어

</br>

## CSS규칙

- 세미콜론(;)은 각각의css끝에 마다 붙여준다

</br>

## CSS의 우선순위

- ##### 인라인 > 내부 > 외부

- ##### 같은 방식의 경우: (마지막에 선언된 스타일이 우선순위를 가진다.)</u>

- ##### id > class >name > 태그

    - 선순위가 같다면 개수가 많이 나온 것이 우선시 된다는 설명도 있지만 어느 정도 맞는 말이지만 정확하지 않습니다. 정확한 설명은 스타일에 적용되어진 조합들을 토대로 <u>**특정도값을 계산해서 가장 많은 점수를 받은 것이 우선**</u>됩니다! 

        출처: https://engkimbs.tistory.com/913 [새로비]

## CSS적용방법 3가지

- #### 내부 스타일시트

    - ```css
        <style type="text/css">  /*텍스트형태의 style이 css의역활을 합니다*/
        /*css 작성*/
        </style>
        ```

- #### 외부 스타일시트 

    1. ##### Link태그 

        - 해당 문서와 외부 문서를 연결해주는 태그

        - <u>대체 스타일시트를 제공할 수 있다</u>,파이어폭스나 사파리,오페라 같은 브라우저들이 제공하는 rel="alternate stylesheet"속성을 통해 사용자들이 이를 바꿀 수 있도록 한다.

        - http://tcpschool.com/html-tags/link

        - ```css
            <head>
            <link rel="stylesheet" href="resources/css/basic.css" type="text/css">
            </head>
            href:파일경로
            rel:현재문서와 연결문서의 관계 표시(stylesheet로 만들어져 있다 = style과 관련된 내용이다)
            type: 해당 파일의 정보값(text로 작성되어 있으며 , css 기능을 한다.)
            	-css 파일일 경우 type="text/css"
            	-js 파일일 경우 type="text/javascript"
            	-xml 파일일 경우 type="application/txml"			
            ```

    2. ##### @import 

        - **규칙**

            - <u>CSS파일 맨 처음에 위치해야한다</u>.
            - <u>스타일시트에서 다른 외부의 스타일시트를 import할 수 있다.</u>
            - 오래된 브라우저에서 @import를 인식하지 못하게해서 CSS를 숨길 수 있다.

        - ```css
            <style>@import url("resources/css/basic.css"); </style>
            /* style태그 안에다가 써준다 */
            /*★style태그의 가장 위에 써줘야 먹힌다★*/
            ```

- #### link방식과 @import방식의 차이점

    - ##### **link방식**

        -  한번 다운로드받은 css는 임시저장폴더에저장해서(cash) 네트워크를 사용하지않고 읽는다 
        -  병렬방식이다

    - ##### **1@import방식**

        -  @import는 css안에서 다른 css를 참조 할 수도 있다.
        -  직렬방식이다

