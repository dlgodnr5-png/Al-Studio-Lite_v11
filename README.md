<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>왕초보도 할 수 있는 API 키 발급 방법</title>
<style>
  body {
    font-family: 'Apple SD Gothic Neo', 'Malgun Gothic', sans-serif;
    line-height: 1.6;
    color: #333;
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f9f9f9;
  }
  h1 {
    color: #d93025; /* 구글 레드 */
    text-align: center;
    border-bottom: 3px solid #d93025;
    padding-bottom: 15px;
  }
  .step-box {
    background: white;
    border: 1px solid #ddd;
    border-radius: 15px;
    padding: 25px;
    margin-bottom: 30px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  }
  .step-title {
    font-size: 1.3rem;
    font-weight: bold;
    color: #1a73e8; /* 구글 블루 */
    margin-bottom: 15px;
    display: flex;
    align-items: center;
  }
  .step-number {
    background: #1a73e8;
    color: white;
    width: 35px;
    height: 35px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 10px;
    font-size: 1.1rem;
  }
  .highlight {
    background-color: #fff4e5;
    color: #d93025;
    font-weight: bold;
    padding: 2px 5px;
    border-radius: 4px;
  }
  .tip-box {
    background-color: #e8f0fe;
    border-left: 5px solid #1a73e8;
    padding: 15px;
    margin-top: 15px;
    font-size: 0.95rem;
  }
  a.btn {
    display: inline-block;
    background-color: #1a73e8;
    color: white;
    padding: 10px 20px;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    margin: 10px 0;
  }
  a.btn:hover { background-color: #1558b0; }
  img {
    max-width: 100%;
    border: 1px solid #ccc;
    border-radius: 8px;
    margin: 10px 0;
  }
</style>
</head>
<body>

  <h1>🔑 유튜브 API 키 발급받기 (따라해 보세요)</h1>
  <p style="text-align: center; font-size: 1.1rem;">천천히 하나씩 따라 하시면 5분 안에 끝납니다!</p>

  <div class="step-box">
    <div class="step-title">
      <span class="step-number">1</span>
      구글 클라우드 사이트 접속하기
    </div>
    <p>API 키를 받으려면 구글의 개발자 사이트로 가야 합니다. 아래 파란 버튼을 눌러주세요.</p>
    <a href="https://console.cloud.google.com/" target="_blank" class="btn">👉 구글 클라우드 콘솔 바로가기</a>
    <p>※ 구글 아이디로 로그인이 필요합니다. (평소 쓰시는 Gmail 아이디면 됩니다.)</p>
  </div>

  <div class="step-box">
    <div class="step-title">
      <span class="step-number">2</span>
      새 프로젝트(작업 공간) 만들기
    </div>
    <p>처음 접속하면 화면 상단에 <strong>[프로젝트 선택]</strong>이라는 글자가 보입니다.</p>
    <ol>
      <li>상단 메뉴바의 <strong>[프로젝트 선택]</strong> 클릭</li>
      <li>나오는 창 오른쪽 위의 <strong>[새 프로젝트]</strong> 클릭</li>
      <li>프로젝트 이름에 <code>유튜브분석도구</code>라고 적고 <strong>[만들기]</strong> 버튼 클릭</li>
    </ol>
    <div class="tip-box">
      💡 <strong>잠깐!</strong> 만들기를 누르고 10초 정도 기다리면 알림이 뜹니다. 그 후 다시 상단에서 방금 만든 <strong>'유튜브분석도구'</strong>를 선택해 주세요.
    </div>
  </div>

  <div class="step-box">
    <div class="step-title">
      <span class="step-number">3</span>
      YouTube Data API v3 찾아서 켜기
    </div>
    <p>이제 유튜브 데이터를 가져오는 기능을 켜야 합니다.</p>
    <ol>
      <li>화면 왼쪽 위에 있는 <strong>[줄 3개 메뉴(≡)]</strong>를 누르세요.</li>
      <li>메뉴에서 <strong>[API 및 서비스]</strong>에 마우스를 대고, 옆에 나오는 <strong>[라이브러리]</strong>를 클릭하세요.</li>
      <li>검색창에 영어로 <code>youtube</code>라고 치고 엔터를 누르세요.</li>
      <li>목록에서 <strong>[YouTube Data API v3]</strong>가 보이면 클릭하세요.</li>
      <li>파란색 <strong>[사용]</strong> 버튼을 꾹 누르세요.</li>
    </ol>
  </div>

  <div class="step-box">
    <div class="step-title">
      <span class="step-number">4</span>
      대망의 API 키 생성하기
    </div>
    <p>거의 다 왔습니다! 열쇠(Key)를 발급받을 차례입니다.</p>
    <ol>
      <li>'사용' 버튼을 누르고 화면이 바뀌면, 오른쪽 위의 <strong>[사용자 인증 정보 만들기]</strong> 버튼을 누르세요.</li>
      <li><strong>"어떤 API를 사용하시나요?"</strong>라고 물으면 <strong>[YouTube Data API v3]</strong>를 선택하세요.</li>
      <li><strong>"어떤 플랫폼에서..."</strong> 질문에는 <strong>[웹 브라우저(자바스크립트)]</strong>를 선택하세요.</li>
      <li><strong>"데이터 종류"</strong>는 <strong>[공개 데이터]</strong>를 선택하세요.</li>
      <li>마지막으로 파란색 <strong>[완료]</strong> 버튼을 누르면...</li>
      <li>화면에 <span class="highlight">AIza...</span> 로 시작하는 긴 영어+숫자 코드가 나옵니다. 이게 바로 <strong>API 키</strong>입니다!</li>
    </ol>
    <div class="tip-box">
      📋 <strong>복사하기:</strong> 키 옆에 있는 '네모 두 개 겹친 아이콘(복사)'을 누르면 복사가 됩니다.
    </div>
  </div>

  <div class="step-box">
    <div class="step-title">
      <span class="step-number">5</span>
      앱에 키 입력하고 사용하기
    </div>
    <ol>
      <li>다시 우리 <strong>[AI Studio Lite]</strong> 앱으로 돌아오세요.</li>
      <li>오른쪽 상단 <strong>[⚙️ 설정]</strong> 버튼을 누르세요.</li>
      <li>방금 복사한 키를 붙여넣기(Ctrl + V) 하세요.</li>
      <li><strong>[저장]</strong> 버튼을 누르면 끝! 이제 검색창에 키워드를 넣고 검색해 보세요.</li>
    </ol>
  </div>

  <div class="step-box">
    <div class="step-title">
      <span class="step-number">❓</span>
      자주 묻는 질문 (하루 이용량 등)
    </div>
    <h3>Q. 이거 돈 드나요?</h3>
    <p><strong>아니요, 무료입니다!</strong> 구글은 개인 개발자에게 하루 <strong>10,000 포인트(Quota)</strong>를 공짜로 줍니다.</p>
    <ul>
      <li>검색 1번 할 때: 약 100 포인트 차감</li>
      <li>즉, 하루에 <strong>약 100번 정도 검색</strong>할 수 있습니다.</li>
      <li>매일 오후 5시(한국시간 기준)에 포인트가 다시 10,000으로 꽉 찹니다. 마음껏 쓰세요!</li>
    </ul>

    <h3>Q. 'AI Studio' 키랑 같이 써도 되나요?</h3>
    <p>네, 가능합니다! 하지만 <strong>구분해서 쓰는 게 관리하기 편합니다.</strong></p>
    <p>방금 만든 프로젝트(유튜브분석도구)에서 'Gemini API(AI Studio용)'도 같이 발급받을 수 있지만, 초보자분들은 헷갈릴 수 있으니 <strong>각각 따로 발급받아 두시는 걸 추천</strong>합니다.</p>
  </div>

  <div style="text-align: center; margin-top: 50px; color: #666;">
    <p>지금 바로 시작해서 나만의 유튜브 대박 아이템을 찾아보세요! 🎉</p>
  </div>

</body>
</html>
