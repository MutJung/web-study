3 이미지와 하이퍼링크
========================
1. **이미지**
    * GIF, JPG , PNG 이 세개 사용가능
    * GIF : 색상 수 작아서 파일 크기 작다 -> 아이콧 불릿
    * JPG : 사진 찍기 위해 개발 된 형식, 색상 수 많다.
    * PNG : 사진 찍는 것 가능, 배경 투명 가능 -> 웹에서 많이 쓰인다
    * < img> 태그
        - 기본형 : < img src="경로">
        - src 속성 : 이미지 파일 경로 설정
            - 경로 설정이 잘못 되어 있으면 x 박스 뜬다
            - 현재 html 파일이 있는 디렉터리 기준인듯 하다.
        - alt 속성 : 이미지를 설명하는 대체 텍스트
            - 이미지를 표시 할 수 없는 상황일 때 대체 텍스트를 표시
        - width, height 속성 : 이미지의 크기를 조정
            - 사용 하지 않으면 원래 크기대로 표시
            - 사용하면 원하는 크기대로 이미지 표시
            - 이미지 용량은 변하지 않는다.
        - ex) <img src="hjw.png" alt="hanjungwoo" width="250" height"400">
        - < figure> < figcaption> - 이미지에 설명글 붙이기
            ex) 
            
            < figure>
            
            < img>
            
            < figcaption> 설명글 < /figcaption> 
            
            < /figure>

2. **링크 만들기**
    * 하이퍼링크
    1. < a> 태그, href 속성
        - 기본형

        **< a href="링크할 주소"  [속성] >** 텍스트 **< /a>**
        - < a> 태그에서 사용할 수 있는 속성
            1. href : 링크한 문서나 사이트의 주소를 입력한다.
            2. target : 링크한 내용이 표시될 위치가 새창인지 현재 탭인지 지정
            3. download : 링크한 내용을 보여주는 것이 아니라 다운로드
            4. rel : 현재와 링크한 문서의 관계를 알려준다.
            5. hreflang : 링크한 문서의 언어를 지정
            6. type 링크한 문서의 파일 알려준다.
        - target 속성 - 새 탭에서 링크 열기
            - target="_self" : 현재 창
            - target="_blank" : 새 창
            - parent, top -> i frame 에서 사용
    2. 한 페이지 안에서 점프하기 - 앵커
        - 문서가 길어서 원하는 위치로 보내주는
        - 기본형

             <태그 id="앵커 이름"> 텍스트 또는 이미지 </태그>

             < a href="#앵커 이름"> 텍스트 또는 이미지 < /a>
        - ex

            < h1 id="akname">  title < /h1>

            < a href="#akname"> 링크 버튼 < /a>
    3. < area> 태그, usemap 속성 - 이미지 맵
        - 기본형
        -        < map name ="맵이름">

                     < area>
              
                     < area>
              
                     ...
            
                  < /map>

                 < img src="이미지경로", usemap"#맵이름">
        - ex)
        
            < img src="naver,daum.png" id="ak2" usemap="#ndmap">

            < map name="ndmap">
            
                < area href="http://www.naver.com" target="_blank" shape="rect" coords="88,109,457,446">
            
                < area href="http://www.daum.net" target="_blank" shape="rect" coords="595,110,1023,443">
        
            < /map>

* * *
## 이미지 맵을 이용한 이벤트 메일 만들기

* < body>~< /body> 부분만을 메일 보내는 곳에 넣으면 된다.
* 이미지 파일은 웹 서버에 올라와 있어야 여러 사람이 볼 수 있게 된다.
ex)
            
            < img src="http://ajtwlswjddnv.dothome/naver,daum.png" id="ak2" usemap="#ndmap"> // 이렇게 서버에 있는 사진을 사용해야 한다.

            < map name="ndmap">
            
                < area href="http://www.naver.com" target="_blank" shape="rect" coords="88,109,457,446">
            
                < area href="http://www.daum.net" target="_blank" shape="rect" coords="595,110,1023,443">
        
            < /map>
* 그림판을 이용해 좌표를 알아낸다.