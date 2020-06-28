# HTML 



## 태그 

**`<q>`태그** : 둘러싼 텍스트가 **짧은 인라인 인용문**이라는것을 나타냅니다,줄 바꿈이 없는 짧은 경우에 적합**(inline요소)**

**`<blockquote>`태그** : **긴 인용문**을 나타낼 때 쓴다 **(block요소)**

>   - **`<cite>`태그:** 작품의 제목을 지정할 때 사용한다 ,이텔릭체로 표시
>   - **`title`속성**: 마우스를 가져다 댓을때 뜨는 정보 
>
>   - **`cite`속성 :**  출처를 표시할 수 있다 검색엔진이 이 주소정보를 사용할 수 있다

```
<blockquotecite="#" title="드래곤라자 명언">
	<cite>드래곤라자</cite> 나는 단수가 아니다</blockquote>
	<!--title속성은 마우스를 가져다 댓을 때 뜨는 정보, cite는 출처를 표시할 수 있다-->
	<q cite="#" title="드래곤라자 명언"> 나는 단수가 아니다</q>
```

**`hr`태그 :** 밑줄태그 

**`div`태그:** 영역을 정의하는 태그 **(block요소)**

**`p`태그 :** 단락을 정의하는 태그 (**block요소)**,  

### 글자태그

- **`strong`태그** : 굵게 (강조) : **`b`태그**
- **`em`태그** : 기울기 : **`i`태그**
- **`strong`태그**와 **`em`** 태그는 **웹 접근성**과 관련되어 있다
    - 글씨를 음성으로 들려줄 때 더 강하게 말하는 등의 역활을 해줄 수 있다.

</br>

## 블록요소와 인라인요소 

- **블록요소** : 한줄을 다 먹는 친구

    - 블록 요소안에 특스트와 인라인 요소 포함 가능
    - 블록 요소안에 블록 요소 포함가능(<u>**일부불가**</u>)

- **인라인요소** : 해당줄에 포함되는 친구

    - 인라인 요소 안에 텍스트와 인라인 요소 포함가능   ( 인라인 ⊃ [텍스트 | 인라인요소] )

    - **인라인 요소 안에 블록요소 포함 불가** (실행은 되어도 warning이 뜨고 에러를 유발할 수 있다.)

    - ```html
      <span>인라인 요소안에 <p>블록요소</p> 포함불가 </span>
      			<!-- 사용은 가능하나, 지양하자 -->
      ```

- **HTML5 블록 요소**

    - ```html
        address`, `article`, `aside`, `audio`, `blockquote`, `canvas`, `dd`, `div`, `dl`, `fieldset`, `figcaption`, `figure`, `footer`, `form`, `h1`, `h2`, `h3`, `h4`, `h5`, `h6`, `header`, `hgroup`, `hr`, `noscript`, `ol`, `output`, `p`, `pre`, `section`, `table`, `ul`, `video
        ```

- **HTML5 인라인 요소** 

    - ```html
        a`, `abbr`, `acronym`, `b`, `bdo`, `big`, `br`, `button`, `cite`, `code`, `dfn`, `em`, `i`, `img`, `input`, `kbd`, `label`, `map`, `object`, `q`, `samp`, `small`, `script`, `select`, `span`, `strong`, `sub`, `sup`, `textarea`, `tt`, `var
        ```

</br>

## HTML규칙

-   시작 태그에 속성을 줄 수 있다
-   시작태그와 끝태그 사이에 값이 들어갈 수 있다
-   요소를 정확하게 매칭
-   요소, 속성 이름은 소문자
-   요소는 항상 닫아야 한다 (일부 단일 태그 존재 ex <img ... />) ( HTML5부터 생략가능 하긴 하다) 
    -   </태그>시작이면서 끝인 태그인데 html4부터는 안써줘도 된다
-   <u>특수문자</u>를 쓸 때는 <u>**Entity Name(code)** 으로 사용</u>한다

## HTML의 특수 문자 (Entity Name(code) )

**참고주소 :** https://www.w3schools.com/html/html_entities.asp

```html
	&lt; &nbsp; 태그연습 &nbsp; &gt;
	<!-- 
		&lt; : <
		&gt; : >
		&nbsp : white space
		&quot; : "
		&amp; : &

		(띄어쓰기)
        &nbsp; -작은
        &ensp; -보통 
        &emsp;  -큰

Entity(code)로 사용하는 이유??
-HTML은 태그로 구조화를 해주는데 태그는 <와 > 를 사용하므로 인식에 오류가 발생할 수 있다.
-공백이 많아도 공백을 하나만 인식한다
-->
```

</br>

## DTO(Document Type Definition)선언

-   HTML5는 `<!DOCTYPE html>`만 선언 해준다
-   **strict :** 선언된 html 버전의 문법과 구조를 정확하게 사용
-   **transitional :** 선언된 html버전 이외의 문법과 구조를 허용
-   **fameset :** transitional + frame 지원(사실상 transitional과 동일)
-   <u>**읽는 법만 알면 된다**</u>
    -   ![DTD읽는법](D:\KH\UI\UI수업자료\DTD읽는법.PNG)



## Document(문서)

- **문서**: 데이터가 저장 되어있는 것을 도식화시키는 것
- **HyperText**(Link) : 문서에서 문서로 넘어가는것 
- **Markup** : <u>구조화</u> , 트리와 같은 그림으로 표현할 수 있는것 
- **HTML(Hyper Text  Markup Language)**: 문서를 <u>태그를 이용</u>하여 구조화시키는 언어 

- **HTTP**: 통신규약, 약속,요청하고응답받는것에 대한 규약

- **빅데이터**: 가공된 데이터를 시각화하는 것까지

- ```html
    <!DOCTYPE html> <!--document의 타입이 html이다를 알려준다-->
    ```

</br>

## 시맨틱 태그

#### 시맨틱태그의 종류와 설명

-   **`header`**: 문서의 헤더를 의미하고 **사이트소개나 로고**등에 사용한다

-   **`nav`** : 내비게이션을 의미하고 **웹 문서 내의 메뉴** 등에 사용한다

-   **`section`** : 문서의 내용을 의미하고 **웹 문서의 본문** 등에 사용된다

-   **`article`** 
    -   여러개의 내용으로 나누는 구분을 의미하고 **본문 내의 세부 절** 등에 사용된다
    -   사용예 : 포럼게시물, 블로그 포스트, 신문기사 

-   **`aside`** : 주요 내용 이외의 문서 내용을 의미하고 **블로그의 사이드 바** 등에 사용된다

-   **`footer`** 
    -   문서의 바닥글을 의미하고 문서 작성자,저작권 정보,이용 약관 링크 , 연락처 정보등이 포함된다
    -   `<footer>`에 요소 가있을 수 있습니다 .

![](https://img1.daumcdn.net/thumb/R800x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F246184395656761521)

</br>

## 테이블

- **`th`태그**: 제목행
- **`td`태그**: 내용행
- **`caption`태그**: 테이블의 제목
- **`colgroup`태그** : col태그를 묶어준다
    - **`col`태그** :  열 한줄 한줄을 가리키고 <u>**각자의 크기를 지정해줄 수 있다**</u>.
- **`thead`태그** : 테이블의 최상단 행을 차지한다 , 어느 위치에 써져도 가장 위를 가리킨다.
- **`tfoot`태그** : 해당 테이블의 가장 밑의 행을 차지한다
- **`tbody`태그**: 테이블의 내용부분으로 따로 지정하지 않아도 <u>자동생성된다.</u>
- <u>칸의 갯수를 넘어서면 삐져나간다</u> 

</br>

##### `border-collapse`속성

-   ```css
    border-collapse: collapse; /*테두리 합치기*/
    ```

##### `bgcolor ="red"` 속성

-   테이블의 배경색을 변경해준다

##### `border ="1"`속성

-   테이블 테두리

##### `aligns`속성

-   정렬

##### `background="파일경로"`속성

-   배경이미지

##### `colspan`속성 : 양옆합치기

##### `rowspan` 속성: 위아래합치기

##### `border-spacing`속성(셀 간격)

- border와 border사이의 공간을 지정한다

- ```css
    table{
                       border-spacing: 20px;
    }
    ```

##### `colgroup`태그

- 테이블에서 서식 지정을 위해 하나 이상의 열을 그룹으로 묶을 때 사용한다
- table 요소의 자식 요소로, 모든 <u>**caption 요소보다 뒤**</u>에 위치해야 하며 모든 **<u>thead, tbody, tfoot, tr 요소보다는 앞</u>**에 <u>**위치해야 합니다.**</u>

```html
<colgroup span="2" style="background-color: lightpink"></colgroup> <!--2개의 열에만 적용-->
```

##### `col`태그

- **`colgroup`**요소에 속하는 각 열(column)의 속성을 정의할 때 사용한다
- col 요소는 각 행(row)이나 셀(cell)의 스타일을 반복하지 않고, 열(column)마다 각각 다른 스타일을 적용하고 싶을 때 유용하게 사용할 수 있습니다.
- **`span="숫자"` 속성** : 몇개의 열을 제어할건지 설정 할 수 있다

```html
<table>
    <colgroup>
        <col style="background-color: lightgreen">
        <col span="2" style="background-color: yellow">
    </colgroup>
    <tr>
        <th>학번</th>
        <th>이름</th>
        <th>학과</th>
    </tr>
    <tr>
        <td>2006123456</td>
        <td>홍길동</td>
        <td>전자공학과</td>
    </tr>
</table>
```

</br>

## `img`태그

- **`alt`속성  :** 이미지 파일이 없을 때 실행한다

- **`usemap` :**속성:  해당 img태그에서 map태그를 사용할것을 알려주는 속성

    - **`map`태그**

        - https://tonks.tistory.com/39
        - 이미지의 특정 부분을 지정하여 링크를 걸 때 사용하는 태그 
        - 반드시 area태그를 포함한다 
        - 하나의 그림에 여러 링크를 걸 때 사용한다
            - **이미지맵** : 클릭할 수 있는 영역을 지닌 이미지

    - **`area`태그** 

        - 이미지맵에서 영역을 지정한다

    - ```html
        <img src="image/kakao.jpg" alt="test" width="100px" height="100px" usemap="#my"/>
          		<map name="my">
          			<area shape="rect" coords="25,25,75,75" href="index.html" alt="가즈아 인덱스!"/>
          		</map>
        ```

</br>

## `a`태그

- `title`**속성** : 마우스를 가져다 데면 뜨는 문장

- <u>**#id값을 이용해서 페이지의  원하는 부분으로 포커스를 이동할 수 있다**</u>

- ```html
    <a href="#a">1번</a><br/>    <!-- 클릭시 -->
    
    <p id="a">1번</p>			<!-- 여기로 이동-->
    ```

</br>

## 목록태그

- ### `ol` : 순차적 리스트

- ### `ul`: 비순차적 리스트

    - **`li`** :목록

- ### `dl`: 정의형 목록

    - **`dt`** : 제목
    - **`dd` **: 목록

- **`list-style : none`** : 리스트의 표식을 없애준다

</br>

