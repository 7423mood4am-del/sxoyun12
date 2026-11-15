# 후드 펫 모바일 버전

Android와 iPhone에서 같은 화면으로 사용할 수 있는 설치형 웹앱(PWA)입니다. 모바일용 캐릭터와 걷기/멈추기, 저장한 웹사이트, 공식 공연 일정 바로가기, Spotify 앱 열기/검색 기능을 포함합니다.

## 설치 안내

앱을 홈 화면에 설치하려면 이 폴더를 HTTPS를 지원하는 웹 호스팅에 게시해야 합니다. 이 프로젝트에는 GitHub Pages용 Actions workflow가 포함되어 있습니다. 저장소에 올리면 `main` 브랜치 업데이트 때 사이트를 자동 게시합니다. 처음에는 저장소의 **Settings → Pages → Build and deployment → Source**를 **GitHub Actions**로 설정해야 합니다. 압축 파일을 휴대폰에 복사해 `index.html`을 여는 것만으로는 PWA 설치가 되지 않습니다.

- Android: Chrome에서 게시된 주소를 열고 메뉴에서 **앱 설치** 또는 **홈 화면에 추가**를 선택합니다.
- iPhone: Safari에서 게시된 주소를 열고 공유 메뉴에서 **홈 화면에 추가**를 선택합니다.

GitHub Pages에 공개 게시하면 웹앱 파일과 캐릭터 이미지가 공개 URL에서 누구나 볼 수 있습니다. 이 PWA에는 개인 로그인 정보나 비밀 키를 넣지 않습니다.

## 휴대폰 버전의 동작

휴대폰 OS는 Windows 바탕화면 위의 항상 위 오버레이 펫을 허용하지 않습니다. 모바일 버전에서는 앱을 열어둔 화면 안에서 캐릭터가 움직입니다. 저장한 웹사이트는 브라우저 로컬 저장소에 보관됩니다. Spotify는 휴대폰의 Spotify 앱으로 연결되며, 앱 설치와 계정 로그인이 필요합니다.

## 파일

- `index.html`: 모바일 화면 및 상호작용
- `manifest.webmanifest`: 홈 화면 설치 정보
- `service-worker.js`: 오프라인 캐시
- ``: 캐릭터 PNG, Gaegu 글꼴, 아이콘
- `Gaegu-OFL.txt`: 글꼴 라이선스
