2 텍스트 관련 태그들
=======================
## 1. 텍스트를 묶어주는 태그
### 1. **텍스트를 묶어주는 태그**
    1. < hn> 태그- 제목표시
        - 기본형 : < hn> 제목 < /hn>
        - 각 웹 콘텐츠 영역에서 제목을 표시할 때 사용하는 태그
        - ex) < h1> ~ < /h1>
        - h1 > h2 > h3 > h4 > h5 >h6
        - 6 까지 있다.
    2. < p> 태그- 텍스트 단락
        - 기본형 < p> 텍스트 < /p>
        - 입력한 내용 앞뒤로 빈 줄이 생기면서 텍스트 단락이 만들어 진다.
    3. < br> 태그- 줄 바꾸기
        - 너무 글이 길어지면 줄 바꾸기
        - 닫는 태그가 없다
    4. < blockquote> 태그- 인용문 넣기
        - 기본형 < blockquote> 인용 내용 < /blockquote>
        - 다른 텍스트보다 안으로 들여 써진다.
    5. < hr>
        - 기본형 < hr>
        - 주제가 바뀔 때 분위기 전환.
        - 수평 줄 생긴다.
    6. < pre>태그- 입력한 그대로 표시
        - 기본형 < pre> 텍스트 < /pre>
        - 소스에 표시한 공백이 그대로 표시됨
        - 프로그램 소스를 표시할 때 유용함.
        - 들여쓰기같은거 
### 2. **텍스트를 한 줄로 표시하는 태그**
    1. < strong>, < b> - 굵게 표시
        - < strong> : 중요한 내용이라서 강조해야 할 때
        - < b> : 단순히 굵게 표시할 때
    2. < em>, < i> - 이탤릭체로 표시하기
    3. < q> 태그 - 인용내용 표시
    4. < mark> 태그 - 형광펜 효과
    5. < span>, < div> 태그 - 영역 묶기
        - < span> : 줄 안에서 한 줄 묶기
        - < div> : 줄 바꿔 단락으로 묶기
        - 나중에 css 로 이 부분만 (특정 부분만) 바꿔 주기 위해서
    6. < ruby> 
        - 동아시아 글자에 주석 표시
        - < rt> 태그 이용
        - ex) 
### 3. **목록을 만드는 태그**
    1. < ul>, < li> - 순서 없는 목록
        - unordered list
        - 리스트 각 목록 앞에 점이 붙는다.
        - < ul> < li>list1< /li>  < li>list2< /li>  < /ul>
    2. < ol>, < li> - 순서 목록
        - ordered list 
        - 리스트 각 목록 앞에 순서 나타내는 숫자 붙는다
        - < ol> < li>list1< /li>  < li>list2< /li>  < /ol>
    3. < dl>, < dt>, < dd> - 설명 목록
        - 제목과 그에 대한 설명으로 이루어진 목록
        - < dl>
        - < dt> 제목1 < /dt>
        - < dd> 설명1 < /dd>
        - < dt> 제목2 < /dt>
        - < dd> 설명2 < /dd>
### 4. **표를 만드는 태그**
    1. 표를 만드는 태그
        - < table>~< /table> : 표의 시작과 끝
        - < tr>~< /tr> : 행
        - < td>~< /td> : 셀, < th>~< /th> 제목 셀

    2. 표 합치기
        - colspan : col 합치기
            - ex) < td colspan="3">< /td> -> 3개 합치기
        - rowspan : row 합치기
    3. 표 제목
        1. < caption> - 표 위 중앙에 표 제목
            - ex) 
            
            < table> 
            
            < caption> Title < /caption> 
            
            < /table>
        2. < figure>, < figcaption> : 표 제목 위 아래 위치 가능
            - ex) 
            
            < figure>
            
            < figcaption> Title < /figcaption>
            
            < table> Table < /table>  
            
            < /figure>
    4. 표의 구조
        - < thead> , < tbody> , < tfoot> 
    5. col 특징
        - col 끼리 묶어서 색깔을 변화시킨다거나 하기.
        - ex

          < colgroup>
          
          < col span = "2" style ="background-color:blue;">
          
          < /colgroup>