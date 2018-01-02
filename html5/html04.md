4 폼과 input 태그
==================
1. 폼 만들기
    * 웹에서 만나는 폼 : 사용자가 웹 사이트로 정보를 보낼 수 있는 요소들
    * 정보를 저장하거나 검색하거나 수정하는 일들
    * < form> 태그
        * 기본형 : < form [속성="속성 값"]> 여러 폼 요소 < /form>
        * form 태그에서 사용 하는 속성들
            1. method : 사용자가 입력한 내용들을 서버 쪽 프로그램으로 어떻게 넘겨줄지 지정.

            속성 값

                1. get : 
                    * 넘길 수 있는 글자 수의 제한이 있다.
                    * 주소 표시 줄에 사용자가 입력한 내용 그대로 드러난다.->보안약함
                    * 검색 창
                2. post : 
                    * 대부분 이 방식을 사용
                    * 로그인 창
            2. action
                * 서버로 값을 넘겼을 때 그 정보를 처리해 줄 서버 프로그램 지정
            3. name
            4. target
        * < label> 태그
            * 폼 요소에 레이블(텍스트) 를 붙이는 태그
            * 예를 들어 체크 박스에서 글씨 클릭해도 체크박스에 체크가 되는 것
            * 기본형
                1. < label [속성="속성값"]> 레이블 < input></ label>
                    - ex) < label> 아이디 < input> </ label >
                2. < label for="id 이름">

                    < input id="id 이름" [속성="속성 값"]>

                    < /label>
                    - ex)

                        < label for="user-id">아이디(6자 이상)< /label>
                        < input type="text" id="user-id">
                        
                        <label for="user-id">아이디(6자 이상)</label>
                        <input type="text" id="user-id">

        * < fieldset> 태그, < legend> 태그
            1. < fieldset> : 폼 요소들을 그룹으로 묶는다
            2. < legend> : 그룹으로 묶는 구역에 제목을 붙인다.
        * < input> 태그
            * 기본형 < input type="유형" [속성="속성값"]>
            * type 종류 : hidden, text, search ,tel, url,email,password,등
                - hidden: <input type="hidden">
                - password : <input type = "password">
                - search : <input type = "search">
                - date : <input type = "date">
                - tel : <input type = "tel">
                - checkbox : <input type="checkbox" name="" value="">
                    - < input type="checkbox" name="" value="">
                        -> name과 value 속성 지정해 줘야한다.
                    - 여러 항목 중 둘 이상을 선택할 때
                - radio : <input type="radio">
                    - name 과 value 속성 지정해 줘야한다.
                    - 여러 항목 중 하나만 선택할 때
                - submit : <input type="submit">
                    - 사용자 입력 냉용 전부 서버로 전송
                - reset : <input type="reset">
                    - 사용자 입력 내용 전부 삭제
                - image : <input type="image">
                    - submit 버튼 대신 이미지 삽임
                    - 예쁜 버튼 만들 때 쓰일 듯

* * *
3. < input> 태그의 다양한 속성
    1. autofocus
        - 페이지를 불러오자마자 원하는 폼 요소에 마우스 커서 표시
        - 깜빡깜빡하게
        - ex) < input type="text" autofocus>
    2. placehorder
        - 입력란에 표시하는 힌트로, 필드를 클릭하면 사라짐
        - ex) < input type="text" placehorder="하이폰없이 입력">
    3. readonly
        - 내용을 보기만 하고 입력하지 못하게 함.
        - <input type="text" reandonly value="gigi">
    4. required
        - 필수 필드 체크
        - 속성 값없이 required 라고만 입력
        - 형식 까지 체크해줌
        - < input type="" required>
    5. min,max,step
        - min,max : 해당 필드의 최솟값, 최댓값
        - step : 허용된 범위 내의 숫자 간격
        - type 이 date, datetime, datetime-local, month, week, timee, range, number 인 경우에만 사용
        - <input type="number" min="3" max="7" step=2>
        - type=num min=3 max=7 step=2
    6. size, minlength, maxlength
        - size: 텍스트 관련 필드에서 화면에 몇 글자까지 보이게 ㅏㄹ지 결정
        - maxlength : 입력 가능 최대 글자
        - minlength : 입력해야 할 최소 글자
        - <input type="text" minlength="3" maxlength="7">
        - type=text minlength=3 maxlength=7
* * *
## 4. 여러 데이터 나열해 보여주기
* < select>, < optgroup>, < option>
    - 여러 옵션 중에서 선택 - 드롭다운 목록
    - 공간을 최소한으로 사용하면서 어려 옵션 표시 가능
    - 기본형

        < select 속성="속성값">
            < option value="값" [속성="속성값"]> 내용1 < /option>
            
            < option value="값" [속성="속성값"]> 내용2 < /option>
            
            < option value="값" [속성="속성값"]> 내용3 < /option>
            
            < option value="값" [속성="속성값"]> 내용4 < /option>
            
            ...
        < /select> 
    - select 태그의 속성
        1. size : 화면에 표시될 드롭다운 메뉴의 항목 개수 지정
        2. multiple : Ctrl 눌러서 여러개 선택가능
    - option 태그의 속성
        1. value : 옵션 선택 시 서버로 넘겨질 값을 지정
        2. selected : 화면에 표시될 때 기본으로 선택되어 있는 옵션 지정
    -< optgroup> 태그
* < textarea>
    - 텍스트 영역- 여러 줄의 텍스트 입력
    - 게시판의 게시물 입력 창, 회원 가입 양식의 약관 등
    - 속성
        - name : 다른 폼 요소와 구분하기 위해 텍스트 영역의 이름을 지정
        - cols : 텍스트 영역의 가로 너비를 문자 단위로 지정
        - rows : 텍스트 영역의 세로 길이를 줄 단위로 지정, 지정 숫자보다 줄 개수가 많아 지면 스크롤 막대 생긴다.
*< button> 태그
    - 다양한 형태의 버튼 삽입
    - css 이용해 꾸미기 가능
    - 기본형
        - < button [속성="속성값"]> 내용 < /button>
    - 속성
        - submit
        - reset
        - button
* < output>
* < progress>
    - 진행상태
    - <label>진행상태</label> <progress value="50" max="60">
* < meter>
    - 결과상태
    - <meter value="0.8">
    - 속성
        - optimal
        - low high 등 이영