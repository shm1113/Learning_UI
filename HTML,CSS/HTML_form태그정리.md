## `form`태그(중요)

- **설명**

    - 여러개의 값은 &로 구분하여 보내준다
    - **get방식**은 보내는 정보가 url에 보여진다
    - **post방식**은 보내는 정보가 보이지 않는다 

- **`action`속성**: 데이터를 보낼위치

- **`method`속성**: 데이터를 보내는 방식 (get 또는 post)

- **`value`속성** : 해당 태그의 값 (대소문자 구분)

    </br>

## `filedset`태그

- #####  form태그 안에서 테두리로 영역을 구분하는 태그

- ##### **`legend`태그** :  fieldset으로 생겨난 테두리에 제목을 만들어주는 태그

</br>

## input 태그 type종류

| 속성값       | 내용                                                         |
| ------------ | ------------------------------------------------------------ |
| text         | 한 줄짜리 텍스트 입력 필드                                   |
| password     | 비밀번호를 입력할 수 있는 필드(***형태로 표시)               |
| hidden       | 사용자에게 보이지 않지만 서버로 넘어가는 필드                |
| search       | 검색 필드 생성                                               |
| tel          | 전화번호 입력 필드                                           |
| url          | URL 주소를 입력할 수 있는 필드                               |
| email        | 메일 주소를 입력할 수 있는 필드 생성                         |
| number       | 숫자를 조절할 수 있는 화살표 생성(숫자만 입력 가능)          |
| range        | 숫자를 조절할 수 있는 슬라이드 막대 생성                     |
| button       | 버튼생성                                                     |
| submit       | form태그의 action에 해당하는 서버 URI로 전송시킬 버튼 생성   |
| file         | 파일을 첨부할 수 있는 버튼 생성                              |
| reset        | 리셋 버튼 생성                                               |
| image        | 이미지 버튼 생성                                             |
| checkbox     | 체크박스 생성, 다중 선택 가능                                |
| radio        | 라디오 버튼 생성, 단일 선택 가능(다중 선택 불가)             |
| color        | 색상 표 생성                                                 |
| datetime     | 국제 표준시로 설정된 날짜 및 시간(연, 월, 일, 시, 분, 초, 분할초) 생성 |
| datetime-loc | 사용자 지역 기준 날짜 및 시간(연,월,일,시,분,초,분할초)생성  |
| date         | 사용자 지역 기준 날짜(연, 월, 일)생성                        |
| month        | 사용자 지역 기준 날짜(연, 월)생성                            |
| week         | 사용자 지역 기준 날짜(연, 주)생성                            |
| time         | 사용자 지역 기준 시간(시, 분, 초, 분할초)생성                |

</br>

## input 태그 속성

#### [input태그 type,속성 정리](https://m.blog.naver.com/PostView.nhn?blogId=heartflow89&logNo=221161705731&proxyReferer=https:%2F%2Fwww.google.com%2F)

#### `disabled`속성 

- ```html
    <input type="text" name="department" disabled><br>
    ```

- 해당 i**nput요소가 비활성화 됨**을 명시한다.

- disabled속성이 명시되면 클릭할 수도 없고 폼 데이터가 제출될 때도 disabled속성이 명시된 input 요소의 데이터는 제출되지 않는다

- disabled속성은 boolean속성**으로 명시하지 않으면 false 명시하면 true값이 된다.

#### `readonly`속성

- ```html
    <input type="text" name="department" value="컴퓨터공학과" readonly><br>
    ```

- input요소의 **입력 필드가 읽기 전용임**을 명시한다 

- readonly로 설정된 입력필드는 수정할 수는 없지만, 해당 내용을 하이라이트 하거나 복사할 수는 있다.

- readonly속성은 boolean속성**으로 명시하지 않으면 false 명시하면 true값이 된다.

#### `autofocus`속성

- ```html
    <input type="text" name="st_id" autofocus><br>
    ```

- 페이지가 로드될 때 **자동으로 포커스가 input요소로 이동됨**을 명시한다.

- **autofocus속성은 boolean속성**으로 명시하지 않으면 false 명시하면 true값이 된다.

#### `autocomplete`속성

- ```html
    <input type="text" name="st_id"
           autocomplete="on"><br>
    <input type="text" name="department"				        autocomplete="off"><br>
    ```

- input요소에서 **자동 완성 기능을 사용**할지 여부를 명시하는 속성

- "on","off"값으로 결정한다

- autofocus를 on으로 명시하면, 브라우저는 사용자가 이전에 입력했던 값들을 기반으로 사용자가 입력한 값과 비슷한 값들을 드롭다운 옵션으로 보여준다

- **사용가능한 type**

    - `text, search, url, tel, email, password, datepickers, range, and color`

#### `required`속성

```html
<input type="text" name="st_name" required><br> <!-- true-->
```

- 폼 데이터(form data)가 서버로 제출되기 전 **반드시 채워져 있어야 하는 입력 필드를 명시**하도록 하는 속성
- required속성이 동작하는 input 요소의 타입
    - `text, search, url, tel, email, password, date pickers, number, checkbox, radio, and file`
- required속성은**boolean타입**으로 명시하지 않으면 false 명시하면 true값이 된다.

#### `max/min`속성

- ```html
    생년월일 : <input type="date" name="bday" min="1900-01-		01" max="2019-01-01"><br>
    학년 : <input type="number" name="grader" min="1" 		 max="4" ><br>
    ```

    

- input 요소의 최댓값/최솟값을 명시하는 속성

- max/min속성이 동작하는 input 요소의 type속성

    - date , datetime , datetime-local , month , number , range , time , week

</br>



## select태그 

- ### 기타설명

    - 기본값으로 가장 위의 option의 값이 사용된다 
        - optgroup태그를 사용해도 기본값으로는 사용할 수 없다

- ### 속성

    - **`multiple`속성**

        - 사용자가 한 번에 두 개 이상의 옵션을 선택할 수 있음을 명시함
        - **boolean속성 값**으로 명시하지않으면 false명시하면 true가된다.

    - ##### `size`속성

        - 드롭다운 리스트에서 한 번에 보일 옵션의 개수를 명시함

    - ```html
        <select name="food" size="7" multiple>
        ```

- ### option태그

    - select값의 종류를 나열하는 태그 

- ### optgroup태그

    - option태그를 분류해주는 태그 , 선택할 수 없는 **굵은 글씨로 표현**된다

    - **`label`속성** : optgroup태그로 표현할 분류명

        ```html
        <optgroup label="나라">
        <option>한국</option>
        <option>미국</option>
        </optgroup>
        ```

</br>

## textarea태그

- **`cols`** : 텍스트 영역이 보이는 **너비(width)**, 기본값 :20

- **`rows`** : 텍스트 영역에서 보이는 **줄의 개수** , 기본값:2

- **`maxlength`**

    - **`textarea`**요소에 입력할 수 있는 **최대 문자수**를 명시하는 속성

    - ```html
        <textarea name="opinion" cols="30" rows="5" maxlength="50"></textarea><br>
        ```

- **`wrap`** 

    - **wrap="hard"**  :폼 데이터가 **서버로 제출될 때** 입력된 **텍스트를 줄바꿈함** 단,hard속성값을 사용할 경우에는 반드시 cols속성이 명시되어 있어야한다.
    - **wrap="soft"**  : 폼데이터가 **서버로 제출될 때** 입력된 **텍스트를 줄바꿈하지 않음** **(기본값)**

- **textarea사이즈 고정하는법**

    - **textarea**{   **`resize:none`**;   }
    - **both**: 가로/세로 조절가능
    - **`horizontal`** : 가로 조절만 가능
    - **`vertical`** : 세로 조절만 가능

