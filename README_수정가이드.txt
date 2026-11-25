심재정 졸업전시 아카이브 · 사용 & 수정 가이드
================================================

■ 실행 방법 (인터넷 없이도 동작)
1. 이 폴더를 노트북 아무 곳에 통째로 복사합니다. (폴더 구조는 그대로 두세요)
2. index.html 을 더블클릭 → 브라우저(크롬 권장)로 열립니다.
3. 전시용 전체화면
   - Mac: 크롬에서 Control + Command + F
   - Windows: F11
   - 아예 키오스크 모드로 띄우려면 (Mac 터미널):
     open -a "Google Chrome" --args --kiosk "file:///폴더경로/index.html"

※ 폰트: 영문은 Helvetica Neue(맥 기본 폰트), 한글은 맥이면 Apple SD Gothic Neo가 자동으로 쓰입니다.
  인터넷이 연결돼 있으면 Noto Sans KR도 불러옵니다. 맥 노트북을 쓰면 오프라인에서도 똑같이 보입니다.


■ 파일 구성
index.html       메인 (히어로 영상 + 작품 카드 2개 + 전시 정보/크레딧/연락처)
i-key.html       I-KEY 상세
sorok.html       SOROK 상세 (UI 체험 포함)
designer.html    디자이너 소개
index-en.html / i-key-en.html / sorok-en.html / designer-en.html   영문 버전
                 (상단 메뉴 오른쪽 KO / EN 으로 전환)
assets/          모든 이미지 · 영상 (한글·영문 버전이 같이 씀)


■ 글자 수정
1. 수정할 .html 파일을 메모장/텍스트편집기/VS Code로 엽니다.
2. Ctrl(⌘)+F 로 바꾸고 싶은 문장을 검색해서 그 부분만 고치고 저장합니다.
3. 브라우저에서 새로고침(⌘R / F5) 하면 반영됩니다.
   ※ < > 로 둘러싸인 태그나 style="..." 부분은 건드리지 말고, 그 사이 글자만 바꾸세요.


■ 한글을 고치면 영문 버전(-en.html)도 같은 자리를 같이 고쳐 주세요.

■ 아직 채워야 하는 곳 (대괄호 [ ] 로 표시됨)
index.html · index-en.html 하단 푸터
  - 기간 [YYYY.MM.DD – MM.DD], 시간 [10:00 – 18:00], 장소 [전시 장소 · 부스 번호]
  - 팀 크레딧 [역할] · [이름], [지도교수] · [이름]
  - 연락처 [이메일] [Instagram] [Behance]
→ 파일에서 "[" 로 검색하면 전부 찾을 수 있습니다.
→ 연락처를 실제 링크로 만들려면 해당 줄의 href="#contact" 를 실제 주소로 바꾸세요.
   예) href="https://instagram.com/아이디"   /   href="mailto:메일주소"


■ 이미지 · 영상 교체 (가장 쉬운 방법)
assets 폴더 안 파일을 "같은 파일 이름"으로 덮어쓰기 하면 끝입니다.

  hero-video.mp4          메인 배경 영상 (블러 처리된 영상)
  hero-poster.jpg         영상 로딩 전 잠깐 보이는 이미지
  logo-dark.png           로고 (검정)
  ikey-door.jpg           I-KEY 대표 이미지 (메인 카드 + I-KEY 상단)
  ikey-slider.jpg         I-KEY 슬라이딩 디테일
  ikey-top.jpg            I-KEY 상단 거치부
  ikey-use.jpg            I-KEY 사용 장면
  sorok-angle.jpg         SOROK 대표 이미지 (메인 카드 + SOROK 상단)
  sorok-back.jpg / sorok-lens.jpg / sorok-side.jpg   SOROK 기능 이미지 3장
  sorok-use.jpg           SOROK 사용 장면
  sorok-ui-1~4-*.jpg      SOROK UI 체험 화면 4장 (스캔→정보→먹이·습성→방어 수단)
  designer-profile.jpg    프로필 사진

※ 비율이 다른 이미지를 넣으면 자동으로 틀에 맞게 잘립니다. 원본과 비슷한 비율을 권장합니다.


■ SOROK UI 체험 단계 수정
sorok.html 에서 "단계 01" 로 검색하면 4개 단계가 나옵니다.
  - data-img="..."  : 그 단계에서 보여줄 이미지 경로
  - demo-label      : 단계 이름
  - demo-desc       : 설명 문장
단계를 추가하려면 <button ...> ~ </button> 한 덩어리를 복사해서 아래에 붙여넣으면 자동으로 늘어납니다.


■ 문제가 생기면
- 이미지가 안 나오면: assets 폴더가 html 파일들과 같은 위치에 있는지, 파일 이름 철자가 같은지 확인
- 수정하다 망가지면: 이 zip을 다시 풀어서 원본부터 다시 시작
