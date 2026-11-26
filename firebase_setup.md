# 🌐 무료 온라인 실시간 스코어보드 연결 가이드 (3분 컷)

별도의 서버나 비용 없이 무료 **Firebase Realtime Database** 주소 1줄만 넣으면 친구들과 실시간 실명 정답률 랭킹전이 가능합니다.

## 1단계: 무료 Firebase DB 만들기
1. https://console.firebase.google.com 접속 후 구글 로그인 → **프로젝트 추가**
2. 좌측 메뉴 **빌드 → Realtime Database → 데이터베이스 만들기** 클릭
3. 위치 선택(싱가포르 추천) → 보안 규칙은 **테스트 모드에서 시작** 선택 후 완료
4. 화면 상단에 표시되는 DB 주소 복사 (예: `https://my-poker-quiz-default-rtdb.asia-southeast1.firebasedatabase.app`)

## 2단계: index.html에 주소 1줄 붙여넣기
1. 메모장이나 VS Code로 `index.html`을 엽니다.
2. `FIREBASE_DB_URL`을 검색(Ctrl+F)합니다.
3. 아래 줄의 따옴표 안에 방금 복사한 주소를 붙여넣고 저장합니다:
   ```js
   const FIREBASE_DB_URL = "https://my-poker-quiz-default-rtdb.asia-southeast1.firebasedatabase.app";
   ```

## 3단계: 배포 후 친구에게 링크 공유
- 수정된 `index.html`을 [Vercel](https://vercel.com), [Netlify](https://www.netlify.com), 또는 [GitHub Pages](https://pages.github.com)에 업로드하면 끝!
- 각자 기기에서 처음 접속할 때 실명을 등록하면(기기당 1회 고정 🔒), 플레이할 때마다 실시간으로 스코어보드에 정답률과 스트릭이 자동 반영됩니다.
