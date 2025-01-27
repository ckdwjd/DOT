<div align="center"> 
  <img src="DOT/src/main/webapp/resources/images/dot_logo.png" width="400">
</div>
<br>
<h1>DOT.</h1>
<p>한줄 소개 : SNS 플랫폼</p>
<p>개발 기간 : 2023.07 ~ 2023.09</p>
<br>
<div>
  <h2>🛠  사용 기술 및 라이브러리</h4>
  <ul>
    <li>Java, HTML5, CSS, JS</li>
    <li>MyBatis, Spring Boot</li>
    <li>Bootstrap, jQuery, Stomp, SockJS</li>
    <li>Oracle</li>
  </ul>
</div>
<br>
<div>
  <h2>🛠  담당 역할</h4>
  <ul>
    <li>프로젝트 주제 선정, 기능 기획</li>
    <li>유스케이스 및 DB설계</li>
    <li>전반적인 UI 기획 / 설계 (소개 페이지, 메인 피드, 상세 피드, 채팅방 등)</li>
    <li>스크립트를 통한 스크롤 애니메이션 구현</li>
  </ul>
</div>
<br>
<div>
  <h2>💡 참여 소감</h2> 
  이번 프로젝트인 'DOT'를 통해 채팅 부분을 주로 맡아 실시간 기능을 구현하는 과정은 많은 도전과 성취를 경험했습니다. 처음에는 웹 소켓에 대한 기본적인 이해가 부족해서 초기 연결에 3일이나 소요되었고, 이 기간 동안 여러 가지 시행착오가 있었습니다. 특히, 웹 소켓에서 중요한 개념인 '구독'에 대한 이해가 부족했기 때문에 참고 자료를 통해 학습하고, SockJS와 Stomp 라이브러리를 활용하여 웹 소켓 연결을 구현하게 되었습니다.
프로젝트를 진행하면서 단순히 기능을 구현하는 것 이상으로 디테일한 부분에 신경을 쓰고자 노력했습니다. 예를 들어, 데이터베이스(DB)에 저장된 값과 현재 시간을 비교하여 시간이 얼마나 흐른 지를 계산하고, 이미지 첨부 및 피드 공유와 같은 다양한 기능을 추가했습니다. 이러한 과정에서 DB 설계도 컬럼을 추가하거나 제거하는 작업도 필요했고, 기존의 목적을 가지던 테이블을 다른 목적으로 수정하는 일도 있었습니다. 이를 통해 소프트웨어 설계의 중요성을 더욱 깨달았습니다.
물론, 2달이라는 시간 동안 모든 원하던 기능을 구현하지 못한 점은 아쉬웠습니다. 그러나, 노력과 열정을 쏟아부어 다양한 세부 기능을 프로젝트에 추가할 수 있었고, 결과물을 만족스럽게 완성할 수 있었습니다. 이 경험을 통해 웹 소켓과 웹 개발에 대한 이해와 기술력을 크게 향상하게 되었으며, 향후 프로젝트에서도 더 나은 개발자로 성장해 나갈 것입니다.
</div>
<br><br>
<h2>구현 내용</h2>
<div>
  <h4>1. 소개 페이지(페이지 로딩 시)</h4>
  <img src="DOT Git img/Untitled.png" width="600"/>
  <p>
    <h4>구현기능설명</h4>
    <ul>
      <li>화면 로딩 시 setTimeout()함수를 통해 일정한 간격을 두고 순차적으로 글이 나타나고 마지막엔 글은 화면에 고정이 되고 배경이 사라지게 구현</li>
      <li>스크롤을 내릴 시 특정 영역을 넘어갈 경우 글이 자연스럽게 사라지도록 구현</li>
    </ul>
  </p>
  <br>
  <h4>2. 소개 페이지1</h4>
  <img src="DOT Git img/Untitled (1).png" width="600"/>
  <p>
    <h4>구현기능설명</h4>
    <ul>
      <li>스크롤을 내릴 시 우측에 존재하는 이미지에 맞춰 좌측의 설명글이 변함</li>
      <li>해당 구역을 벗어날 시 그 sticky를 이용하여 가장 하단에 붙게 설정하고 스크롤을 위로 올릴 시 해당 영역에 고정되도록 구현</li>
    </ul>
  </p>
  <br>
  <h4>3. 소개 페이지2</h4>
  <img src="DOT Git img/Untitled (2).png" width="600"/>
  <p>
    <h4>구현기능설명</h4>
    <ul>
      <li>스크롤 위치에 따라 해당 영역의 높이가 변하게 설정</li>
      <li>스크롤 위치가 해당 영역의 제목부분에 도달 시 컨텐츠가 제 자리에 위치함</li>
      <li>컨텐츠를 호버 시 프로젝트 참여자들의 이름이 나오게 구현</li>
    </ul>
  </p>
  <br>
  <h4>4. 상세 피드</h4>
  <img src="DOT Git img/Untitled (3).png" width="600"/>
  <p>
    <h4>구현기능설명</h4>
    좋아요 기능
  
  - 클릭 시 하트의 색이 붉은색으로 변경되고 ajax를 통해 좋아요 테이블에 해당 사용자 번호와 피드 번호 값이 담김
  - 페이지 로딩 시에도 적용되어 기존에 좋아요를 누른 피드일 시 붉은색 하트로 출력
  - 알림 테이블에도 INSERT하여 웹소켓을 통해 해당 피드 사용자에게 알람이 가도록 구현
  
  스토어(찜하기) 기능
  
  - 클릭 시 배경이 흰색으로 꽉차고 ajax를 통해 스토어 테이블에 해당 사용자 번호와 피드 번호 값이 담김
  - 페이지 로딩 시에도 적용되어 기존에 스토어를 활성화 한 피드일 시 배경이 흰색인 아이콘으로 출력
  - 알림 테이블에도 INSERT하여 웹소켓을 통해 해당 피드 사용자에게 알람이 가도록 구현
  
  댓글 기능
  
  - 댓글을 입력하는 인풋에 값을 넣고 엔터를 치거나 답글 버튼을 클릭하면 사용자가 입력한 댓글이 ajax를 통해 댓글 테이블에 해당 댓글을 INSERT하고 댓글 리스트 최상단에 출력
  - 또한 상세 뿐만 아니라 기본 피드에도 사용자가 입력한 댓글로 변경
  - 알림 테이블에도 INSERT하여 웹소켓을 통해 해당 피드 사용자에게 알람이 가도록 구현
  
  공유하기 기능
  
  - 해당 피드를 공유하면 팔로우와 채팅방을 선택하여 공유할 수 있도록 구현, 만약 팔로우를 선택했다면 채팅방을 새로 생성하고 해당 피드 썸네일의 이미지를 공유하고 채팅으로 “사용자님께서 게시물을 공유하였습니다" 출력
  - 해당 썸네일을 클릭 시 그 피드에 대한 상세 내용이 모달로 출력되도록 구현
  - 내부 기능은 위 설명들과 마찬가지로 구현
</p>
<br>
<h4>5. 공유하기</h4>
<p>5-1. 공유 대상 선택</p>
<img src="DOT Git img/Untitled (4-1).png" width="300"/>
<img src="DOT Git img/Untitled (4).png" width="300"/>
<p>5-2. 검색 기능</p>
<img src="DOT Git img/Untitled (5).png" width="600"/>
<p>5-3. 공유 후 채팅방</p>
<img src="DOT Git img/Untitled (6).png" width="600"/>
<p>
  <h4>구현기능설명</h4>
  
  <공유 대상 선택>
- 공유하기 아이콘을 클릭 시 위 화면처럼 현재 사용자와 관련된 팔로우와 채팅방 리스트를 볼 수 있는 화면이 모달창으로 나타남
- 체크박스를 통해 팔로우 및 채팅방으로 공유
- 중복 체크 가능하지만 팔로우에서 여러 선택을 할 시 각각 채팅방이 생성되는 것이 아니라 해당 인원을 묶어 그룹 채팅방을 생성 후 공유

<검색 기능>
- 팔로우에 대한 검색만 가능하도록 구현
- keyup 이벤트를 통해 사용자가 입력한 글짜마다 ajax를 호출하여 비동기로 DB에 존재하는 값을 비교해서 리스트를 출력
- 만약 해당 키워드를 포함하는 값이 없으면 ‘존재하는 팔로우가 없습니다’를 출력
  
<공유 후 채팅방>
- 팔로우 및 채팅방을 선택 후 공유하게 된다면 좌측의 이미지처럼 게시물을 공유했다는 내용과 해당 시간이 나타나도록 출력
- SockJS와 Stomp 라이브러리를 이용하여 실시간 기능을 구현
- 공유된 이미지를 클릭 시 메인 피드에서 보았던 상세 피드화면처럼 모달창으로 나타나게 구현
</p>
<br>
<h4>6. 채팅방</h4>
<p>6-1. 검색 기능</p>
<img src="DOT Git img/Untitled (8).png" width="600"/>
<p>6-2. 채팅방 생성</p>
<img src="DOT Git img/Untitled (9).png" width="600"/>
<p>6-3. 채팅방 나가기</p>
<img src="DOT Git img/Untitled (10).png" width="600"/>
<p>
  <h4>구현기능설명</h4>
  
  **<검색>**

- 채팅방을 검색할 수 있도록 구현
- keyup 이벤트를 통해 사용자가 입력한 글짜마다 ajax를 호출하여 비동기로 DB에 존재하는 값을 비교해서 리스트를 출력
- 만약 해당 키워드를 포함하는 값이 없으면 ‘조회된 채팅방이 없습니다’를 출력

**<생성>**

- 채팅방 생성 기능을 구현
- keyup 이벤트를 통해 사용자가 입력한 글짜마다 ajax를 호출하여 비동기로 DB에 존재하는 값을 비교해서 리스트를 출력
- 만약 해당 키워드를 포함하는 값이 없으면 ‘존재하는 팔로우가 없습니다’를 출력
- 생성하기 버튼을 클릭 시 체크박스에 담긴 회원 번호를 가지고 채팅방을 생성, 체크박스가 활성화 된 회원 번호를 가지고 그룹 채팅방을 생성
- 생성된 채팅방은 ‘현재 대화내용이 존재하지 않습니다.”라는 메세지가 담긴 상태로 출력

**<나가기>**

- 채팅방 나가기 기능을 구현
- 채팅방 나가기 버튼을 클릭 시 나가기 버튼과 채팅방 좌측에 체크박스를 생성
- 체크박스를 활성화 후 삭제하기 버튼을 클릭 시 선택된 채팅방은 DB에서 DELETE 후 채팅방 리스트를 다시 출력
</p>
<br>
<h4>7. 채팅 기능</h4>
<p>7-1. 일반 채팅</p>
<img src="DOT Git img/Untitled (11).png" width="600"/>
<p>7-2. 이미지 첨부</p>
<img src="DOT Git img/Untitled (12).png" width="600"/>
<p>
  <h4>구현기능설명</h4>
  
 <일반 채팅>

- 웹소켓 통신을 위해 SockJS, Stomp 라이브러리를 이용하여 실시간 채팅 기능 구현
- 채팅을 보낼 시 웹소켓을 거쳐 채팅방 내에 존재하는 사용자들의 채팅방 리스트에 메세지와 보낸 시간 정보를 가지고 최상단에 출력
- 시간은 DB에 담긴 데이터와 현재 시간을 비교 후 SimpleDateFormat을 이용하여 출력

(채팅방 기준 : 1분 전 == 방금전, 1시간 전 == 분 단위, 24시간 전 == 시간 단위, 그 외 일 단위로 출력)

(채팅 기준 : 24시를 기준 하루가 지나기 전 오전/오후 00시 00분, 이후 00월 00일 출력)

<이미지 첨부>

- 이미지 첨부 아이콘을 클릭 시 파일을 첨부할 수 있는 창이 나타나고 해당 이미지 파일을 전송할 수 있도록 구현
- 이미지 전송과 동시에 해당 이미지는 ajax를 호출하여 MultipartFile 객체로 받아와 DB에 정보를 INSERT하고

그 이미지 경로를 메세지에 담아서 반환(채팅과 마찬가지로 웹 소켓으로 구현)
</p>
<br>
</div>
