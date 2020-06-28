# CSS선택자

</br>

## `!important`CSS강제적용 

```css
/*규칙을 무시하고 가장먼저 우선순위를 부여한다,되도록사용하지X*/
선택자{속성: 속성값 !important;}
```

</br>

## 선택자 

- 스타일을 적용시킬 범위를 선택하기 위한 표현식

</br>

#### 태그선택자

- 태그의 이름을 지정하여 CSS를 선언하는 선택자
- **,(콤마)로 구분**하여 **여러 요소를 선택**할 수 있다.

</br>

#### id선택자(#)

- 유일하게 적용되는 스타일일 경우 사용한다  
- 똑같은 id를 **여러개 주면 html에서는 어느정도 동작할지라도 javascript같은 곳에서는 하나만 작동**한다 

</br>

#### class선택자(.)

- 한번에 여러 개를 바꿀 때 사용하는 것이 좋다 .
- **class명에 공백이들어가면 공백을 기준으로 나누어진 class가 생성된다** 

</br>

#### 자식선택자(>)

- 부모요소>자식 요소

    - 부모요소의 **직속자식만 적용한다**

    - ```scss
        #at>p{	// 아아디 at인 요소의 직계자손중 p태그에 적용
            color:gold;
        }
        #at>div>p{	//아이디at인 요소의 직계자손div의 직계자손p태그에적용
            color:silver;
        }
        ```

</br>

#### 하위선택자(  )

- 부모요소 자식요소{ } 
    - 부모요소 밑에 존재하는 **모든 자식 요소**에게 적용한다

</br>

#### 인접선택자(+,~)

- 같은 부모를 가지는 요소를 형제 관계라고 한다
- **(인접형제 선택자)A+B** : A요소 바로뒤에 있는 B요소를 선택(<u>**중간에 다른요소가 있으면 X**</u>)
- **(일반형제 선택자)A~B** : A요소를 뒤따르는 모든 B요소

```scss
h3+b{
    color: navy;
} //h3다음에나오는 b
b+span{
    background-color:black;
    color: white;
}//b다음에 span
b~span{	//b다음에나오는 
//    스타일
}
```

</br>

#### 속성 선택자( [  ] )

```scss
/* 속성 선택자 */
p[title]{	//p태그 중에 title속성이있는것
    color: orange;
}
p[title="b"]{	//p태그중에 title속성이 b인것
    background-color: gray;
}
```

- **`[attribute]`** : attribute라는 속성을 가지고 있는 요소들을 선택
- **`[attribute=value]`** : 속성값과 일치하는 요소들을 선택 
- **`[attribute~=value]`** : 속성값이  "value" 단어를 포함하는 요소선택,앞 뒤에 공백 있어도 선택
- **`[attribute |= value]`** : 속성값이 정확하게 "value"이거나 "value-"로 시작하는 요소선택
- **`[attribute ^= value]`** : 속성값이 "value"로 **시작****하는** 요소들을 선택 
- **`[attribute $= value]`** : 속성값이 "value"로 **끝****나는** 요소 선택
- **`[attribute *= value]`** : **속성값을 포함하고 있으면 선택** (위치 상관 없음)

</br>

#### 가상 클래스 선택자

- 특정 이벤트가 발생한 태그 선택

- **`: link`** - 방문한 적이 없는 링크

- **`: visited`** - 방문한 적이 있는 링크

- **`: hover`** - 마우스를 롤오버 했을 때

- **`: active`** - 마우스를 클릭했을 때

- **`: focus`** - 포커스 되었을 때(input태그등)

-  **`: checked`** - 선택했거나 on상태인 라디오 , 체크박스 ,옵션 요소를 나타낸다

- **`: first`** - 첫번째 요소

- **`: last`** - 마지막 요소

- **`: first-child`** -첫번째 자식

- **`: last-child`** - 마지막 자식

- **`: nth-child(2n+1)`** -홀수 번째 자식

    - **`odd:`**홀수
    - **`even`:** 짝수

- 선택자 뒤에 다른 요소를 놓으면  결과를 해당 요소에 반영한다

- ```scss
    a:link{  //방문하지 않은 링크
        color: green;
        font-size: 25px;
    }
    a:visited{	//방문한 링크 
        color : red;
        font-size: 15px;
    }
    a:hover{	//마우스가 올라갔을 때
        background-color: fuchsia;
        font-family: fantasy;
        font-size: 35pt;
        color: blue;
    }
    a:active{ 	//마우스가 클릭됐을 때
        background-color: fuchsia;
        font-family: fantasy;
        font-size: 35pt;
        color: blue;
    }
    a:focus{ //요소에 포커스가 머물러 있는 동안 선택
        //스타일
    }
    input :checked{		//체크박스를 체크했을경우 발동
        width : 100px;
        height: 100px;
    }
    
    
    ```

</br>

#### 종속 선택자

- 타입,id,class 선택자가 결합된 상태

- ```scss
    li.scls01{  //li태그이면서 scls01클래스
    background-color: green;
    }
    li.scls02#sidul{		//li태그이면서 scls02클래스이면서 sidul아이디
    font-size: 20px; 
    }
    ```

</br>

#### 그룹선택자

- 한번에 여러가지 태그들을 선택하는 선택자

- ```scss
    /* 그룹 선택자 */ 
    p,pre,strong{ //p태그pre태그strong태그를 선택
        color: #18dcff;
    }
    ```

</br>

#### 선택자 우선순위

- 적용방법이 같다면 선택자의 종류와 수에 따라 우선순위가 결정된다

- **선택자 우선순위**

    1. **!important**
    2. 인라인 스타일
    3. 아이디 선택자
    4. 클래스/속성/가상선택자
    5. 태그선택자
    6. 전체선택자

- ##### 삽입 위치에 따른 우선 순위

    1.  < head > 요소 안의 임베디드 방식으로 적용(style태그)
    2.  < style > 요소안의 @import문
    3.  < link > 요소로 연결된 CSS파일
    4.  < link >요소로 연결된 CSS파일 안의 @import문
    5.  브라우저의 기본 스타일 시트

</br>

- 