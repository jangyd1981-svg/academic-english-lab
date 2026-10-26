# Academic English Lab — iPhone 설치 안내

이 폴더는 **홈 화면에 설치할 수 있는 PWA(Progressive Web App)** 프로젝트입니다. 앱스토어에 등록된 네이티브 앱은 아니지만, iPhone Safari에서 웹사이트를 홈 화면에 추가하면 앱처럼 실행할 수 있습니다.

## 코드를 몰라도 배포하는 방법 (무료 옵션: GitHub Pages)

### 1. ZIP 압축 풀기
`academic_english_lab_pwa.zip` 파일을 컴퓨터에서 압축 해제합니다. `index.html`, `manifest.webmanifest`, `service-worker.js`, `icons` 폴더가 보여야 합니다.

### 2. GitHub 계정 만들기/로그인
컴퓨터에서 https://github.com 에 접속해 로그인하거나 무료 계정을 만듭니다.

### 3. 새 저장소(repository) 만들기
- 오른쪽 위 `+` → `New repository`
- 이름에 `academic-english-lab` 입력
- `Public` 선택
- `Add a README file`은 선택하지 않아도 됩니다.
- `Create repository` 클릭

### 4. 파일 업로드
- 새 저장소 화면에서 `uploading an existing file` 링크를 누르거나 `Add file` → `Upload files`
- 압축을 푼 **폴더 안의 파일과 폴더를 모두** 업로드합니다. `index.html`이 저장소 최상위에 있어야 합니다.
- 아래쪽 `Commit changes`를 누릅니다.

### 5. 사이트 게시하기
- 저장소의 `Settings` → 왼쪽 메뉴 `Pages`
- `Build and deployment`의 Source를 `Deploy from a branch`로 선택
- Branch를 `main`, 폴더를 `/(root)`로 선택한 뒤 `Save`
- 1~5분 정도 기다립니다. Pages 화면에 게시된 주소가 표시됩니다. 주소는 보통 `https://사용자이름.github.io/academic-english-lab/` 형태입니다.

### 6. iPhone에 설치하기
- iPhone에서 **Safari**를 열고 GitHub Pages 주소로 접속합니다. Chrome보다 Safari를 권장합니다.
- 하단의 공유 버튼(네모에서 위로 화살표)을 누릅니다.
- 메뉴에서 `홈 화면에 추가`를 선택합니다. 메뉴가 안 보이면 아래로 스크롤합니다.
- 이름을 `Academic English Lab`으로 확인하고 `추가`를 누릅니다.
- 홈 화면에 생긴 아이콘을 누르면 앱처럼 열립니다.

## 앱에서 제공하는 기능
- 하루 15개씩 단어 카드 학습
- IPA, 한국어 뜻, 예문과 해석, 유의어·반의어
- `알고 있어요` / `다시 복습` 평가
- 오답 복습 목록
- 전체 단어장 검색
- 날짜별 학습 진도
- JSON 백업 내보내기/가져오기
- 오프라인 사용을 위한 기본 캐시

## 저장과 주의사항
- 학습 기록은 해당 iPhone의 브라우저 저장소(localStorage)에 저장됩니다.
- 앱 아이콘으로 실행한 경우에도 같은 사이트 데이터가 유지되지만, Safari 웹사이트 데이터나 기기 데이터를 지우면 기록이 삭제될 수 있습니다.
- 다른 기기와 자동 동기화되지 않습니다. `학습 기록`에서 JSON 백업을 정기적으로 내보내 두세요.
- 기본 단어 데이터는 앱에 포함되어 있습니다. 현재 버전은 30개 이상의 단어를 포함하며, 일별 15개씩 묶어 보여줍니다. 이 버전은 자동으로 새로운 단어를 인터넷에서 받아오지는 않습니다.
- 단어가 추가되는 날짜 기준은 앱을 처음 실행한 날입니다. 브라우저 저장소가 초기화되면 Day 1로 다시 시작할 수 있습니다.
- GitHub Pages 주소는 공개 웹사이트입니다. 학습 기록은 서버로 전송되지 않지만, 개인 정보를 입력하는 기능은 없습니다.

## 문제가 생겼을 때
- 주소가 404라면 `index.html`이 저장소 최상위에 있는지, Pages 설정의 branch가 `main`이고 폴더가 `/(root)`인지 확인합니다.
- 설치 메뉴가 안 보이면 iPhone Safari에서 사이트를 열고 공유 메뉴를 다시 확인합니다.
- 변경한 파일이 바로 보이지 않으면 사이트를 새로고침하거나 잠시 기다립니다.
