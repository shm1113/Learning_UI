# CSS 애니메이션



#### `transition`속성

- https://poiemaweb.com/css3-transition

- css속성을 변경할 때 애니메이션 속도를 조절하는 방법을 제공하는 속성

- transition은 자동으로 발동되지 않는다 

- **:hover와 같은 가상 클래스 선택자 또는 JavaScript의 부수적인 액션에 의해 발동한다**

- ```scss
    div{
    	transition: <property> <duration> <timing-function> <delay> ;
      // <트랜지션의 대상이되는 속성>
      // <트랜지션이 일어나는 지속시간(s:초단위,ms)> 
      //  <트랜지션 효과를 위한 수치함수를 지정> 
      //  <속성이 변화한 시점과 트랜지션이 실제로 시작하는 사이에 대기하는 시간을 초 단위(s)또는 밀리초 단위(ms)로 지정>
        
    }
    ```

```css
  
  

​```scss
 #tran{
        width:200px;
        height: 200px;
        background-color: red;
        color: white;
        font-size: 30pt;
        word-wrap: break-word;
        transition: width 0.5s, background 1.5s linear, transform 1.5s;
    }
    #tran:hover{
        width:800px;
        background-color: blue;
        transform: translate(300px,0px);
    }
    li{
        width:500px;
        background: gray;
        margin-bottom:3px;
        font-size: 30pt;
        font-weight: bold;
        list-style-type: none; /*??*/
        cursor: pointer ; 
        /*★마우스를 가져다 댔을 때 손가락이 등장 */
        transition: width 10s linear , color 1s linear, letter-spaccing 1s;
    }//1초동안 linear방식으로 변환
    li:hover{
        width: 800px;
        color: red;
        letter-spacing: 5px;
    }
```

#### `transform`속성

- 요소에 **회전,크기 조절, 기울이기, 이동 효과를** 부여할 수 있는 속성

- **`translate`** : 원래 위치에서 요소를 이동시킨다 

    - ```scss
        transfrom : translate(50px,50px); //원래 위치에서 50px이동한다.
        ```

- ##### **`rotate`**

    - 해당 요소를 회전시키는 속성

    - ```scss
            transform: rotate(30deg);//요소를30도 회전한다.
               -webkit-transform:ratate(30deg);
               -ms-transform:rotate(50deg);
               -o-transform: rotate(60deg);
        ```

- ##### **`scale`**

    - 요소의 크기를 변환한다

    - ```scss
        transform: scale( 0.6,0.6); //크기를 0.6배한다
        ```

- ##### **`skew`**

    - 요소를 비튼다 

    - ```scss
            transform: skew(20deg,20deg);
        //20도 만큼 앞으로 돌리고 ,20도만큼 옆으로 돌린다
        ```

</br>

## Animation

- https://webclub.tistory.com/621

- **`animation-name`** 

    -  애니메이션의 **중간 상태를 지정하기 위한 이름**을 정의한다, 중간상태는 
    -  중간상태는 **@keyframes을 이용**해서 기술한다

- **`animation-duration`** 

    -  한 싸이클의 애니메이션이 **얼마나 걸쳐 일어날지 지정**합니다 
    -  0또는 음수는 작동하지 않는다 
    -  **s초단위** 로 입력한다

- **`animation-delay`** 

    -  엘리먼트가 **로드되고 나서 언제 애니메이션이 시작될지** 지정합니다
    -  **0(기본값)** :바로시작 
    -  **now :** 0과 같다
    -  **숫자단위(s,ms) :** 설정한 시간이 지난뒤에 애니메이션을 시작한다
        - **숫자단위(음수) :** 바로 실행하지만 **지정한 시간이 지난 뒤의 장면부터 애니메이션을 재생**한다 

- **`animation-direction` **

    -  애니메이션이 종료되고 다시 처음부터 시작할지 역방향으로 진행할지 지정합니다.
        - **(기본값)`normal`** :지정된 방향으로 재생
    - **`reverse`** :반대 방향으로 재생
    - **`alternate`** : 지정된 방향,반대 방향 순으로 반복
        - **`alternate-reverse`**: 반대방향 , 지정된 방향 순으로 반복

- **`animation-iteration-count`** 

    - 애니메이션이 **몇번 반복**되는지 지정합니다 
    - **`infinite`**로 지정하면 무한반복
    - **숫자가 소수면 재생하는 도중에 멈춘다**
    - **기본값** : 1

- **`animation-play-state`**

    - 애니메이션을 멈추거나 다시 시작할 수 있다
    - **`running`** : 애니메이션을 재생한다(기본값)
    - **`paused`** : 애니메이션을 정지한다

- **`animation- timing -function`** : 중간 상태들의 전환을 어떤 시간 간격으로 진행할지 지정한다

- **`animation- fill -mode`** : 애니메이션이 시작되기 전이나 끝나고 난 후 어떤 값이 적용될지 지정한다

- **속기형** 

- ```css
    animation: name | duration | timing-function | delay | iteration-count | direction | fill-mode | play-state [,...];
    
    animation: mybox 2s infinite;
    ```

  

## @keyframes

- 개발자가 애니메이션 중간중간의 특정 지점들을 거칠 수 있는 키프레임들을 설정함으로써 CSS 애니메이션 과정의 중간 절차를 제어할 수 있게 한다
- 키프레임에서 !important 속성을 이용한 정의는 모두 무시된다
- **`0%` 와 `100%` 키 프레임 모두에 정의된 속성들만 애니메이션 동작을** 합니다. 이 둘 중 아무것도 포함되지 않은 속성은 애니메이션 연속을 지속하기 위한 시작 값으로 사용된다

```scss
@keyframes mybox{  //animation이름
            0%{width: 150px; height: 150px; backgorund: yellow; transform: 						translate(10px,10px);}
            25%{width:200px; height: 200px; background:blue; transform: 						translate(50px, 50px);}
            50%{ width: 250px; height: 250px; background: orange; transform: 					 translate(100px,100px);}
            75%{width: 300px; height:300px; background: pink; transform : 						translate(50px,50px);}            
            100%{width:200px;height: 200px; background: red; transform: 						translate(10px,10px);}
            
        }
```

## 