# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 언어 및 커뮤니케이션 규칙

이 리포지토리에서의 모든 작업은 다음의 언어 규칙을 따릅니다:

- **기본 응답 언어**: 한국어 — Claude Code의 모든 응답과 피드백은 한국어로 작성
- **코드 주석**: 한국어 — 모든 코드 주석은 한국어로 작성
- **커밋 메시지**: 한국어 — Git 커밋 메시지는 한국어로 작성
- **문서화**: 한국어 — README.md, ROADMAP.md 등 모든 문서는 한국어로 작성
- **변수명/함수명**: 영어 — JavaScript, HTML, CSS 코드에서는 영어 명명 규칙 준수 (국제 표준)

**예시:**
```javascript
// ✅ 올바른 방식
function getUserProfile() {
  // 사용자 프로필 데이터를 가져오는 함수
  return userData;
}

// ❌피하기
function get사용자Profile() {
  // 혼합 언어 사용 금지
  return userData;
}
```

---

## 프로젝트 개요

**개발자 웹 포트폴리오** — 개발자의 기술, 경력, 프로젝트를 채용담당자와 협력자에게 선보이는 단일 페이지 반응형 포트폴리오 웹사이트입니다.

- **기술 스택**: HTML5 (시맨틱 마크업), CSS3 + Tailwind CSS, Vanilla JavaScript
- **프로젝트 유형**: 정적 웹사이트 (Tailwind CDN 또는 빌드 도구 활용)
- **현재 상태**: 계획 수립 완료 (ROADMAP.md 작성됨, Phase 1 초기 설정 진행 중)

## 프로젝트 구조

```
claude-code-mastery/
├── ROADMAP.md              # 상세 개발 로드맵 및 단계별 계획
├── CLAUDE.md               # Claude Code 가이드 문서 (현재 파일)
├── index.html              # 메인 HTML 엔트리 포인트
├── css/
│   └── styles.css          # 커스텀 CSS + Tailwind 빌드 산출물 (빌드 도구 사용 시)
├── js/
│   └── main.js             # JavaScript 인터랙션 (스무스 스크롤, 다크모드 등)
├── assets/
│   ├── images/             # 프로필 이미지, 프로젝트 스크린샷
│   └── icons/              # SVG 아이콘 또는 아이콘 에셋
└── README.md               # 배포 및 사용 가이드
```

## 아키텍처 및 핵심 설계 결정사항

### 레이아웃 전략
- **단일 페이지 설계**: 모든 콘텐츠를 하나의 스크롤 가능한 `index.html` 파일에 포함하여 단순성과 빠른 로딩 속도 실현
- **시맨틱 HTML5**: `<header>`, `<main>`, `<section>`, `<footer>`, `<nav>` 등을 활용하여 접근성과 SEO 최적화
- **모바일 우선 CSS**: Tailwind 브레이크포인트 (`sm`, `md`, `lg`)를 활용한 모든 디바이스의 반응형 설계

### Tailwind CSS 통합
- **접근법**: 개발 편의성을 위해 **CDN** (`tailwindcss.com/play`) 방식으로 시작, 필요 시 **빌드 도구** (PostCSS)로 마이그레이션하여 최적화
- **커스텀 설정** (빌드 도구 사용 시): `tailwind.config.js`에서 커스텀 색상, 폰트, 브레이크포인트 정의 가능
- **유틸리티 우선 철학**: Tailwind 유틸리티 클래스를 최대한 활용하고 커스텀 CSS 최소화

### JavaScript 범위
- **Vanilla JavaScript만 사용** (초기 단계에서 React 등 프레임워크 불필요)
- **선택적 기능** (Phase 4): 스무스 스크롤 네비게이션, 다크/라이트 모드 토글, 모바일 햄버거 메뉴, 스크롤 애니메이션
- **외부 의존성 없음**: `main.js`를 경량으로 유지

### 접근성 및 성능
- **Alt 텍스트**: 모든 이미지에 필수 적용
- **색상 대비 비율**: WCAG AA 기준 충족
- **이미지 최적화**: WebP 등 최적화된 형식 사용, 적절한 파일 크기 유지
- **불필요한 JavaScript 제거**: CSS 애니메이션 선호

## 개발 워크플로우

### Phase 1: 초기 설정
```bash
# 폴더 구조 생성
mkdir -p css js assets/{images,icons}

# index.html에 Tailwind CDN 추가
<script src="https://cdn.tailwindcss.com"></script>
```

### Phase 2: HTML 마크업 작성
- 8개의 주요 섹션(Header, Hero, About, Skills, Experience, Projects, Education, Footer)으로 시맨틱 구조 구성
- 플레이스홀더 콘텐츠와 시맨틱 태그 활용
- 현 단계에서는 콘텐츠 계층 구조에 집중, 스타일링은 나중에

### Phase 3: Tailwind CSS 스타일링
- Tailwind 유틸리티를 활용한 색상, 타이포그래피, 간격 적용
- 반응형 브레이크포인트 구현 (모바일 우선)
- 선택사항: Tailwind의 `dark:` 접두사를 활용한 다크모드 추가

### Phase 4: JavaScript 기능 추가
- `js/main.js`에 선택적 인터랙션 추가
- 예: 스무스 스크롤 앵커, 테마 토글, 모바일 햄버거 메뉴
- 로직은 최소한으로 유지, CSS 활용 선호

### Phase 5: 테스트 및 최적화
- 모바일, 태블릿, 데스크톱에서 테스트 (브라우저 개발자 도구 활용)
- 접근성 점검: 키보드 네비게이션, 스크린 리더, 색상 대비
- 이미지 최적화, 사용하지 않는 CSS/JS 제거

### Phase 6: 배포
- GitHub 리포지토리에 푸시
- GitHub Pages 활성화 (또는 다른 정적 호스팅)
- 사용법 및 링크가 포함된 `README.md` 업데이트

## 자주 사용하는 작업

### 브라우저에서 보기
- **개발 중 (CDN 방식)**: `index.html`을 브라우저에서 직접 열기 (빌드 단계 불필요)
- **로컬 Tailwind 빌드 사용**: VS Code의 Live Server 확장 프로그램 또는 로컬 개발 서버 활용

### CDN에서 빌드 도구로 전환 (선택사항)
프로젝트 규모가 커져 CDN이 한계에 도달했을 때:
```bash
npm init -y
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
# tailwind.config.js에 추가: content: ["./*.html"]
npm run build  # css/styles.css에 최적화된 CSS 생성
```

### 반응형 디자인 확인
- 브라우저 개발자 도구 (F12) → 기기 도구 (Device Toolbar) 활용
- 뷰포트 크기 테스트: 320px (모바일), 768px (태블릿), 1024px 이상 (데스크톱)

### HTML 및 접근성 검증
- W3C HTML Validator로 마크업 정확성 확인
- WebAIM Contrast Checker로 색상 접근성 확인

## 작업별 수정 대상 파일

| 작업 | 주요 파일 |
|------|---|
| 새로운 섹션 추가 (About, Skills 등) | `index.html` |
| 색상, 간격, 폰트 조정 | `index.html` (Tailwind 클래스) 또는 `css/styles.css` |
| 인터랙션 추가 (다크모드, 메뉴) | `js/main.js` + `index.html` (토글 버튼) |
| 포트폴리오 콘텐츠 업데이트 (경력, 프로젝트) | `index.html` 콘텐츠 노드 |
| 프로덕션 최적화 | 모든 파일 (축소화, 이미지 압축) |

## 향후 개발 시 주의사항

- **빌드 단계 불필요 (초기)**: 프로젝트가 Tailwind CDN을 사용하므로 npm/webpack 설정이 필요 없음
- **CSS 우선 접근**: 커스텀 CSS 작성 전에 Tailwind 클래스 활용
- **JavaScript 경량 유지**: 이는 포트폴리오이지 애플리케이션이 아니므로 과도한 엔지니어링 피하기
- **실제 디바이스에서 테스트**: 개발자 도구의 에뮬레이션은 유용하지만 배포 전 실제 휴대폰/태블릿에서 테스트 필수
- **기본 SEO**: 시맨틱 HTML 사용, `<head>`에 메타 설명과 오픈그래프 태그 추가

## 참고 자료

- **ROADMAP.md**: 단계별 상세 개발 계획 및 체크리스트
- **Tailwind CSS 공식 문서**: https://tailwindcss.com/docs
- **HTML5 시맨틱 요소**: https://developer.mozilla.org/en-US/docs/Web/HTML/Element
- **반응형 디자인 패턴**: Tailwind의 모바일 우선 브레이크포인트: `sm:`, `md:`, `lg:`, `xl:`, `2xl:`
