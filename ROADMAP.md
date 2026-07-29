# 개발자 웹 이력서 프로젝트 로드맵

## 📋 프로젝트 개요

정적 1페이지 개발자 포트폴리오 웹사이트를 구축하는 프로젝트입니다.
- **목적**: 개발자의 이력, 기술, 프로젝트를 시각적으로 전시하고 채용 담당자/협력자에게 소개
- **목표**: 반응형 디자인, 깔끔한 UI/UX, 빠른 로딩 속도를 갖춘 포트폴리오 완성

---

## 🛠️ 기술 스택

| 분류 | 기술 |
|------|------|
| **마크업** | HTML5 (시맨틱 태그) |
| **스타일** | CSS3 + Tailwind CSS (CDN 또는 빌드 방식) |
| **인터랙션** | Vanilla JavaScript (선택적 기능) |
| **배포** | GitHub Pages 또는 정적 호스팅 |

---

## 📁 프로젝트 폴더 구조

```
claude-code-mastery/
├── ROADMAP.md                 # 현재 문서
├── index.html                 # 메인 HTML 파일
├── css/
│   └── styles.css            # 커스텀 CSS (Tailwind 빌드 또는 CDN)
├── js/
│   └── main.js               # JavaScript 인터랙션
├── assets/
│   ├── images/               # 프로필 이미지 등
│   └── icons/                # SVG 또는 아이콘
└── README.md                 # 프로젝트 설명 및 배포 안내
```

---

## 🚀 개발 단계별 로드맵

### Phase 1: 프로젝트 초기 설정
- [ ] 프로젝트 폴더 구조 생성 (html, css, js, assets 디렉토리)
- [ ] `index.html` 파일 생성 (기본 HTML 템플릿)
- [ ] Tailwind CSS 연동 (CDN 방식 또는 빌드 환경 구성)
- [ ] 기본 `meta` 태그 설정 (viewport, charset, description)

### Phase 2: HTML 시맨틱 마크업 작성
- [ ] Header 섹션 (네비게이션, 로고)
- [ ] Hero 섹션 (프로필 이미지, 이름, 직함, 한줄 소개)
- [ ] About Me 섹션 (자기소개 텍스트)
- [ ] Skills 섹션 (기술 스택 목록)
- [ ] Experience 섹션 (경력 정보)
- [ ] Projects 섹션 (프로젝트 포트폴리오)
- [ ] Education 섹션 (학력 정보)
- [ ] Contact/Footer 섹션 (연락처, 소셜 링크)

### Phase 3: Tailwind CSS 스타일링
- [ ] 색상 스킴 정의 (주요 색, 배경색, 텍스트색)
- [ ] 타이포그래피 설정 (폰트, 크기, 줄 높이)
- [ ] 레이아웃 구성 (flexbox, grid)
- [ ] 섹션별 스타일 적용
- [ ] 다크모드 지원 (선택사항)
- [ ] 반응형 디자인 (모바일 우선)

### Phase 4: JavaScript 인터랙션 (선택적)
- [ ] 스무스 스크롤 네비게이션
- [ ] 다크모드/라이트모드 토글
- [ ] 모바일 메뉴 (햄버거 메뉴)
- [ ] 스크롤 애니메이션 (Fade-in 효과 등)

### Phase 5: 반응형/접근성/성능 점검
- [ ] 모바일/태블릿/데스크톱 반응형 테스트
- [ ] 웹 접근성 점검 (alt 텍스트, ARIA 속성)
- [ ] 페이지 로딩 속도 최적화
- [ ] 크로스 브라우저 호환성 테스트

### Phase 6: 배포
- [ ] GitHub 리포지토리 생성
- [ ] GitHub Pages 또는 다른 정적 호스팅 배포
- [ ] 커스텀 도메인 설정 (선택사항)
- [ ] README.md 작성 (사용법, 배포 가이드)

---

## 📄 이력서 콘텐츠 구조 (예시)

### 1️⃣ Header (헤더)
```
로고 또는 이름 | Home | About | Skills | Projects | Contact
```

### 2️⃣ Hero Section (주요 섹션)
```
👤 프로필 이미지
이름: 김개발
직함: Frontend Developer / Web Developer
한줄 소개: 사용자 중심의 웹 경험을 만드는 개발자입니다.
버튼: "이력서 보기" 또는 "연락하기"
```

### 3️⃣ About Me (자기소개)
```
안녕하세요! 저는 HTML, CSS, JavaScript를 활용하여 
반응형 웹사이트를 만드는 것을 즐깁니다. 
UI/UX를 개선하고 사용자 경험을 향상시키는 데 관심이 있습니다.
```

### 4️⃣ Skills (기술 스택)
```
Frontend:
  - HTML5, CSS3
  - JavaScript (ES6+)
  - Tailwind CSS
  - React (학습 중)

Tools & Others:
  - Git / GitHub
  - VS Code
  - Responsive Design
```

### 5️⃣ Experience (경력)
```
예시 1)
회사명: OO 회사
기간: 2023년 1월 ~ 현재
역할: Frontend Developer
내용: 웹 프로젝트 개발, UI 개선 담당

예시 2)
회사명: XX 스타트업
기간: 2022년 6월 ~ 2022년 12월
역할: Web Developer Intern
내용: 웹사이트 유지보수, 버그 수정
```

### 6️⃣ Projects (프로젝트 포트폴리오)
```
프로젝트 1: 날씨 앱
- 설명: 실시간 날씨 정보를 조회하는 웹 앱
- 기술: HTML, CSS, JavaScript, API
- 링크: https://github.com/username/weather-app

프로젝트 2: 포트폴리오 웹사이트
- 설명: 개인 포트폴리오 웹사이트
- 기술: HTML5, Tailwind CSS, JavaScript
- 링크: https://github.com/username/portfolio

프로젝트 3: Todo 앱
- 설명: 할일 관리 웹 애플리케이션
- 기술: HTML, CSS, Vanilla JavaScript
- 링크: https://github.com/username/todo-app
```

### 7️⃣ Education (학력)
```
학교명: OO 대학교
전공: 컴퓨터공학
졸업: 2023년 2월
```

### 8️⃣ Contact / Footer (연락처)
```
이메일: example@email.com
GitHub: https://github.com/username
LinkedIn: https://linkedin.com/in/username
Phone: 010-XXXX-XXXX

© 2024 Kim Developer. All rights reserved.
```

---

## 💡 개발 팁

1. **Tailwind CSS 활용**: 유틸리티 클래스를 최대한 활용하여 빠른 스타일링
2. **모바일 우선 접근**: `sm:`, `md:`, `lg:` 브레이크포인트로 반응형 구현
3. **시맨틱 HTML**: `<header>`, `<main>`, `<section>`, `<footer>` 등 활용
4. **접근성**: 컬러 대비, alt 텍스트, 키보드 네비게이션 고려
5. **성능**: 이미지 최적화, 불필요한 JavaScript 제거

---

## 📅 예상 개발 기간

| 단계 | 예상 소요시간 |
|------|--------------|
| Phase 1-2 (마크업) | 2-3시간 |
| Phase 3 (스타일링) | 4-6시간 |
| Phase 4 (JavaScript) | 2-3시간 (선택사항) |
| Phase 5 (테스트) | 1-2시간 |
| Phase 6 (배포) | 1시간 |
| **총합** | **10-15시간** |

---

## ✅ 체크리스트 (전체 진행도)

- [ ] ROADMAP.md 작성 완료
- [ ] Phase 1: 초기 설정
- [ ] Phase 2: HTML 마크업
- [ ] Phase 3: Tailwind 스타일링
- [ ] Phase 4: JavaScript 기능 추가
- [ ] Phase 5: 테스트 및 최적화
- [ ] Phase 6: 배포 및 README 작성
- [ ] 🎉 프로젝트 완료!

---

**작성일**: 2024년 7월 9일  
**상태**: 계획 수립 완료 - Phase 1 준비 중
