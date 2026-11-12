# 포트폴리오 사이트

## 파일
- index.html : 사이트 본체
- data.json : 처음 보여줄 내용 (관리자가 한 번 저장하면 그 뒤로는 Firebase에 저장된 내용이 보입니다)
- firebase-config.js : Firebase 연결 설정 (직접 채워야 함)
- firestore.rules : Firestore 보안 규칙 (Firebase 콘솔에 붙여넣기)

## 1. Firebase 준비 (처음 한 번)
1. https://console.firebase.google.com 에서 프로젝트를 만들거나 기존 프로젝트를 엽니다.
2. 빌드 > Firestore Database > 데이터베이스 만들기 (위치는 asia-northeast3 서울 추천)
3. Firestore Database > 규칙 탭에 firestore.rules 내용을 그대로 붙여넣고 게시합니다.
4. 빌드 > Authentication > 시작하기 > 로그인 방법에서 "이메일/비밀번호"를 사용 설정합니다.
5. Authentication > 사용자 > 사용자 추가
   - 이메일: mannnyang00@gmail.com (firebase-config.js의 ADMIN_EMAIL과 같아야 함)
   - 비밀번호: ggumi_00  ← 이게 관리자 키입니다
6. Authentication > 설정 > 승인된 도메인에 GitHub 주소(예: mannnyang00.github.io)를 추가합니다.
7. 프로젝트 설정(톱니바퀴) > 일반 > 내 앱 > 웹 앱(</>) 추가 > 표시되는 firebaseConfig 값을 firebase-config.js에 붙여넣습니다.

## 2. GitHub에 올리기
1. 새 저장소를 만들고 이 폴더의 파일을 모두 업로드합니다.
2. Settings > Pages > Branch: main / (root) > Save
3. 1~2분 뒤 표시되는 주소로 접속합니다.

## 3. 수정하는 방법
- 사이트 우측 상단 "관리자" > 관리자 키 입력 > 편집 > 저장하기
- 저장하는 즉시 사이트를 열어둔 모든 사람 화면에 바로 바뀝니다 (새로고침 필요 없음).
- 관리자 키를 바꾸려면 Firebase Authentication에서 해당 사용자의 비밀번호를 바꾸면 됩니다.
