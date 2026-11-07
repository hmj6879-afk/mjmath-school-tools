# mjmath-school-tools

낙생고 수학 교사용 웹 도구 모음 「낙생 스마트 수학 포털 (Minjae Math Studio)」.
빌드 과정 없이 순수 HTML/CSS/JS 정적 페이지로 만든다.

## 구조
- `index.html` — 포털 로비. 교사용·학생용 앱을 카드로 연결한다.
- `teacher/saenggibu.html` — 생기부 AI 매니저 (세특·행발 초안 생성). **아직 빈 파일**
- `teacher/signature.html` — 전자 서명부 (동의서·서명 취합). **아직 빈 파일**
- `student/math-high-low.html` — 수식 하이로우 멀티플레이 (낙수터 & 인테그랄 동아리용 수식 배팅 게임)
  - 수식 입력: MathLive (unpkg CDN)
  - 서버/데이터: Google Apps Script 웹앱 (`GAS_URL`)에 fetch로 연결
- `student/n-saat.html` — N-SAAT 캠퍼스 매핑 (학교 공간 수학적 모델링 시뮬레이터). **아직 빈 파일**

## 별도 저장소에 있는 앱
- **Vector Strike (수학 FPS)** — 이 저장소가 아니라 `hmj6879-afk/vector-strike`에 있다.
  - 배포 주소: https://hmj6879-afk.github.io/vector-strike/ (포털 `index.html`에 카드로 연결됨)
  - 작업하려면 이 폴더 옆에 `gh repo clone hmj6879-afk/vector-strike` 로 받는다.
  - 기획서(PRD), 결정 사항, 진행 상황은 그 저장소의 `CLAUDE.md`에 있다.

## 작업 규칙
- 모든 UI 문구와 주석은 한국어로 쓴다.
- 디자인은 `index.html`의 톤을 따른다: Pretendard 폰트, `:root` CSS 변수
  (`--primary: #2563eb`, `--bg-color: #f8fafc`, `--border: #e2e8f0` 등), 둥근 카드형 미니멀 UI.
- 각 앱은 HTML 파일 하나에 CSS와 JS를 함께 담는다. 외부 라이브러리는 CDN으로만 불러온다.
- 새 앱을 추가하면 `index.html`에 카드를 함께 추가한다.

## 여러 컴퓨터에서 작업하기
- 두 대 이상의 컴퓨터에서 GitHub(`hmj6879-afk/mjmath-school-tools`)로 동기화한다.
- 작업을 시작할 때 `git pull`, 마칠 때 commit 후 `git push`.
- Claude의 대화 기록과 메모리는 컴퓨터마다 따로 저장된다. 다른 컴퓨터에서도 알아야 할
  결정 사항이나 진행 상황은 이 파일의 「진행 상황」에 적어 두고 push한다.

## 진행 상황
- 포털 로비(`index.html`) 완성.
- 수식 하이로우 게임 구현됨.
- 생기부 매니저, 전자 서명부, N-SAAT는 파일만 만들어 둔 상태.
- 2026-11-08: Vector Strike(수학 FPS)를 별도 저장소로 완성·배포하고, 포털에 카드를 추가함.
