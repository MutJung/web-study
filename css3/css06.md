6 텍스트 스타일
=====================
**(1) 글꼴 관련 스타일**
---------------------
* font-family 속성
    - 기본형

          font-family:<글꼴 이름>[,<글꼴 이름>, <글꼴 이름>]
          ex)
          body {
               font family:"맑은고딕",돋움,굴림
          }
          // 웹 문서 전체에 맑은 고딕 이라는 글꼴 적용
          // 만일 맑은 고딕 글꼴 없다면 돋움 글꼴 적용 그것도 없다면 굴림 글꼴 적용
    - 지정한 글꼴이 없을 경우에 대비해 두 번째, 세 번째 글꼴까지 지정
    - font-family 속성은 상속되기 떄문에 < body> 태그 스타일에서 한 번 정의하면 문서 전체에 적용되고 문서 안의 모든 자식 요소에 같은 글꼴이 사용됨.
* @font-face 속성
    - 웹 폰트 : 웹 문서 안에 글꼴 정보도 함께 저장했다가 사용자가 웹 문서에서 접속하면 글꼴을 사용자 시스템으로 다운로드시켜 사용하는 글꼴.
    - 사용자 시스템에 없는 글꼴이더라도 웹 제작자가 의도한 대로 텍스트를 표시할 수 있다.
    - <img src="image/웹폰트파일사용법.png">
* font-size 속성
    - 글자 크기를 조절하는 속성
    - 사용할 수 있는 값: 절대 크기, 상대 크기, 숫자, 백분율
    - 기본 값은 상대 크기인 medium
    - font size 속성은 상속된다.
    - 기본형
    
          font-size: <절대크기>|<상대크기>|<크기>|<백분율>
    
    - 속성 값
        1. <절대 크기> : 브라우저에서 지정한 글자 크기
            - xx-small/small/medium/large/x-large/xx-large
        2. <상대 크기> : 부모 요소의 글자 크기를 기준으로 더 크게 또는 더 작게 표시
            - larger/smaller
        3. <크기> : 브라우저와 상관 없이 글자 크기를 직접 지정한다.
        4. <백분율> : 부모 요소의 글자 크기를 기준으로 해당하는 %를 계산해 표시
* font-weight
    - 굵기
    - 0~700??
* font-style
    - font-style:italic; // 이탈릭체
* * *
**(2) 텍스트 스타일**
-----------------------
* color 속성
    - 글자 색 지정
    - 16진수 값이나 rgb 값, hsl 값, 색상 이름 중에서 사용
    - 기본형

          color:<색상>
    -16진수
        - ex) color:#ff0000
        1. 앞에 숫자 두개 -> 빨강의 양
        2. 중간 숫자 두개 -> 초록의 양
        3. 마지막 숫자 두개 -> 파랑으 양
* text-decoration 속성
    - 텍스트에 밑줄을 긋거나 가로지르는 줄 표시
    - 텍스트 링크의 밑줄을 없앨 때도 사용
    - 속성
        1. none : 밑줄 없앨 때 사용
        2. underline
        3. overline
        4. lint-through
* text-shadow 속성
    - 텍스트에 그림자 효과를 추가하는 속성
    - 기본형

          text-shadow: none;
    - 속성 값
        1. <가로거리>
        2. <세로거리>
        3. <번짐 정도>
        4. <색상>
* white-space 속성
    - 공백 처리 방법 지정
    - 속성
        1. normal
        2. nowrap : 스페이스 다 적용 x /  자동 줄바꿈 x
        3. pre : 스페이스 다 적용 o/  자동 줄바꿈 x
        4. pre-line : 스페이스 다 적용 x/  자동 줄바꿈 o
        5. pre-wrap : 스페이스 다 적용 o/  자동 줄바꿈 o
* letter-spacing, word-spacing
    - 글자간 간격, 단어간 간격(띄워 쓰기)


* * *
**(3) 문단 스타일**
-------------------------------
* text-indent 속성
    - 문단의 첫 글자를 얼마나 들여 쓸지 지정
    - 기본형

          text-indent: <크기>|<백분율>
    - 속성
        1. 크기
        2. 백분율 : 부모 요소의 너비를 기준으로 상대적 크기를 지정
* line-height 속성
    - 문단의 줄 간격 지정
    - 속성 <숫자>,<백분율> 은 부모 요소를 기준으로 몇 배인지 지정
    - 보통 글자 크기의 1.5~2배면 적당
* * *
**(4) 목록과 링크 스타일**
---------------
* list-style-type 속성
    - 기본형

          list-style-type: none|<순서없는 목록의 불릿>|<순서 목록의 불릿>
    1. 순서 없는 목록의 불릿 없애기
        - none
    2. 순서 없는 목록의 불릿 바꾸기
        - disc
        - circle
        - square
        - none
    3. 순서 목록의 숫자 바꾸기
        - decimal
        - decimal-leading-zero : 01 02 03 04
        - lower-roman
        - upper-roman
        - lower-alpha : a b c d
        - upper-alpha : A B C D
* list-style-image 속성
    - 순서 없는 목록의 불릿을 이미지로 바꾸는 속성
    - 기본형

          llist-style-image:<이미지>|none
          <이미지> = url(이미지 파일 경로)
    - 속성값
        1. none : 이미지 사용 안하고 list-style-type 속성에서 지정한 형태로 표시
        2. <이미지> : url("images.jpg") 처럼 ur() 키워드 아나에 이미지 파일 경로를 지정
* list-style-position 속성
    - 불릿이나 번호를 들여쓰거나 내어쓸 수 있음

* list-style 속성
    - type,position,image 를 한꺼번에 쓴다
    - <img src="image/list-style.png">