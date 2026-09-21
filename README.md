# 우리반 온라인 프롭 헌트

최대 25명이 크롬북으로 같은 방에 들어와 플레이하는 학교 배경 사물 숨바꼭질 게임입니다.

## 게임 방식
- 선생님이 방 만들기 → 6자리 코드 생성
- 학생은 별명 + 방 코드로 참가
- 12명 이상이면 술래 2명, 그보다 적으면 술래 1명
- 숨는 시간 25초
- 술래 화면/이동/조사는 숨는 시간 동안 잠김
- 숨는 사람은 E로 주변 사물과 똑같이 변신 가능
- 변신 후에도 이동 가능
- 술래는 Space로 가까운 사물을 조사
- 술래 1명당 탐색 15회
- 찾기 시간 3분
- 매 라운드 같은 seed를 모든 플레이어에게 공유해 가구/꽃 랜덤 배치가 모두 동일하게 보임

## 개인정보
학생 로그인/이메일/학번은 받지 않습니다. Firebase Anonymous Authentication을 사용하며, 학생은 수업용 별명만 입력합니다.

## Firebase 1회 설정
1. Firebase에서 새 프로젝트 생성
2. Authentication → Sign-in method → Anonymous 사용
3. Realtime Database 생성
4. Realtime Database Rules에 `firebase.rules.json` 내용 붙여넣고 Publish
5. Project settings → Your apps → Web app 추가
6. Firebase SDK config를 복사해 `config.js`의 `window.FIREBASE_CONFIG`에 입력
7. databaseURL 항목이 반드시 포함되어야 함
8. GitHub Pages 새 버전 반영 후 크롬북 2대로 먼저 접속 테스트

## 중요
Firebase 웹 config는 브라우저 앱에서 공개되는 설정값입니다. 서비스 계정 키, 관리자 비밀번호, private key는 GitHub에 절대 올리지 마세요.
