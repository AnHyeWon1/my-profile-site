# 개발자 웹 이력서 개발 로드맵

## 1. 프로젝트 개요

- **목표**: 개발자 개인 웹 이력서(단일 페이지) 제작
- **기술 스택**: HTML, CSS, JavaScript, Tailwind CSS (CDN 방식)
- **특징**: 정적 페이지, 반응형 디자인, 다크 모드 지원, 별도 빌드 과정 없음

## 2. 이력서 내용 (일반적인 샘플)

| 섹션 | 내용 |
| --- | --- |
| 소개 (Hero) | 이름, 직무(예: 프론트엔드 개발자), 한 줄 소개, 연락처 버튼 |
| 자기소개 (About) | 3~4문장의 간단한 소개 |
| 기술 스택 (Skills) | HTML, CSS, JavaScript, Tailwind CSS, Git 등 |
| 경력 (Experience) | 회사명, 직책, 기간, 주요 업무 2~3줄 |
| 프로젝트 (Projects) | 프로젝트명, 설명, 사용 기술, 링크 (카드 3개) |
| 학력 (Education) | 학교, 전공, 졸업 연도 |
| 연락처 (Contact) | 이메일, GitHub, 블로그 링크 |
| SNS | GitHub, YouTube, Instagram, LinkedIn 등 링크 |

> 모든 내용은 홍길동 등 더미 데이터로 작성한 뒤 본인 정보로 교체합니다.

## 3. 디렉터리 구조

```
claude-code-mastery/
├── index.html        # 메인 페이지 (모든 섹션)
├── css/
│   └── style.css     # Tailwind로 처리하기 어려운 커스텀 스타일
├── js/
│   └── main.js       # 다크 모드, 스크롤 이동, 모바일 메뉴
├── assets/
│   └── images/       # 프로필 사진, 프로젝트 이미지
└── ROADMAP.md
```

## 4. 개발 단계

### 1단계: 환경 설정
- [x] 폴더 및 파일 구조 생성
- [x] `index.html` 기본 골격(`<head>`, 메타 태그, 시맨틱 태그) 작성
- [x] Tailwind CSS CDN 연결 (`<script src="https://cdn.tailwindcss.com"></script>`)
- [x] 한글 웹 폰트 적용 (예: Pretendard)

### 2단계: 레이아웃 및 섹션 마크업
- [x] 상단 고정 네비게이션 바
- [x] Hero → About → Skills → Experience → Projects → Education → Contact → SNS 순서로 마크업
- [x] 푸터(Footer) 작성

### 3단계: 스타일링 (Tailwind)
- [x] 색상 및 타이포그래피 정리
- [x] 반응형 적용 (`sm:`, `md:`, `lg:` 브레이크포인트)
- [x] 카드, 버튼, 배지 컴포넌트 스타일
- [x] 다크 모드 스타일 (`dark:` 클래스)

### 4단계: JavaScript 기능
- [x] 다크/라이트 모드 토글 (`localStorage`에 설정 저장)
- [x] 네비게이션 클릭 시 부드러운 스크롤
- [x] 모바일 햄버거 메뉴 열기/닫기
- [x] 스크롤 시 섹션 등장 애니메이션 (`IntersectionObserver`)
- [x] 현재 섹션에 맞춰 네비게이션 활성 표시

### 5단계: 완성도 향상
- [ ] 접근성 점검 (alt 텍스트, 대비, 키보드 이동)
- [x] SEO 메타 태그 및 Open Graph 설정
- [x] 인쇄/PDF 저장용 스타일 (`@media print`)
- [ ] 크로스 브라우저 및 모바일 테스트
- [ ] Lighthouse 점검 (성능·접근성·SEO 90점 이상 목표)

### 6단계: 배포
- [ ] GitHub 저장소에 업로드
- [ ] GitHub Pages 또는 Netlify/Vercel로 배포
- [ ] 배포 URL을 이력서 및 SNS 프로필에 등록

## 5. 완료 기준

- 모바일/태블릿/데스크톱에서 레이아웃이 깨지지 않을 것
- 모든 섹션의 내용이 표시되고 링크가 정상 동작할 것
- 다크 모드 전환 시 설정이 유지될 것
- Lighthouse 주요 항목 90점 이상

## 6. 향후 확장 아이디어

- 한/영 다국어 전환
- 프로젝트 데이터를 JSON으로 분리해 동적 렌더링
- 방문자용 연락 폼 연동
- Tailwind CLI 도입으로 CDN 의존성 제거
