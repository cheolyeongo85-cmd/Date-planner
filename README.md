# 💑 우리의 데이트 플래너

## GitHub Pages로 올리기
1. GitHub에서 새 저장소(Repository) 생성 (예: `date-planner`)
2. `index.html` 파일을 업로드 (Add file → Upload files)
3. Settings → Pages → Branch: `main` / `(root)` → Save
4. 1~2분 뒤 `https://내아이디.github.io/date-planner/` 로 접속

## 둘이 실시간 공유하기 (Firebase, 무료)
GitHub Pages는 정적 호스팅이라 데이터 저장소가 따로 필요해요.
1. https://console.firebase.google.com → 프로젝트 만들기
2. 빌드 → Firestore Database → 데이터베이스 만들기 (테스트 모드로 시작)
3. 프로젝트 설정 → 일반 → 내 앱 → 웹(</>) 추가 → `firebaseConfig` 복사
4. `index.html` 상단의 `const FIREBASE_CONFIG=null;` 을 복사한 설정으로 교체
   예: `const FIREBASE_CONFIG={apiKey:"...",authDomain:"...",projectId:"...",appId:"..."};`
5. 다시 커밋/업로드 → 둘이 같은 주소로 접속하면 실시간 동기화

⚠️ 테스트 모드 규칙은 30일 뒤 만료되고 주소를 아는 사람은 누구나 수정할 수 있어요.
오래 쓰려면 Firestore 규칙을 직접 설정하세요. 링크는 둘만 아는 곳에 공유하세요.
