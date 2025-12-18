# 👋 jwleepro.github.io

> 개인 포트폴리오 웹사이트 및 자동화된 이력서 관리 시스템

[![Build Resume](https://github.com/jwleepro/jwleepro.github.io/actions/workflows/resume.yml/badge.svg)](https://github.com/jwleepro/jwleepro.github.io/actions/workflows/resume.yml)

## 🌐 About

Jekyll 기반의 개인 포트폴리오 웹사이트입니다.

### 주요 기능

- 📝 **기술 블로그** - Jekyll을 활용한 정적 사이트
- 📄 **자동화된 이력서 관리** - 마크다운으로 작성하면 PDF/DOCX 자동 생성
- 🚀 **GitHub Pages 호스팅** - 무료 호스팅 및 자동 배포

---

## 📄 이력서 자동 생성

마크다운으로 이력서를 작성하면 GitHub Actions가 자동으로 **PDF**와 **DOCX**를 생성합니다.

**👉 [상세 가이드 보기](docs/resume-automation.md)** - 사용법, 설정 방법, 커스터마이징, FAQ

---

## 🚀 로컬에서 실행하기

### Jekyll 사이트 실행

```bash
# 의존성 설치
bundle install

# 로컬 서버 실행
bundle exec jekyll serve

# 브라우저에서 http://localhost:4000 접속
```

---

## 🛠️ 기술 스택

### 웹사이트
- **Jekyll** - 정적 사이트 생성기
- **GitHub Pages** - 호스팅
- **Markdown** - 콘텐츠 작성

### 이력서 자동화
- **GitHub Actions** - CI/CD 자동화
- **Pandoc** - 문서 변환 (MD → PDF/DOCX)
- **XeLaTeX** - PDF 생성 엔진

---

## 📁 프로젝트 구조

```
jwleepro.github.io/
├── _posts/                    # 블로그 포스트
├── _config.yml                # Jekyll 설정
├── docs/                      # 문서
│   └── resume-automation.md   # 이력서 자동화 가이드
├── resume/                    # 이력서 관련 파일
│   ├── resume.md              # 마크다운 이력서
│   └── resume-style.css       # 커스텀 스타일 (선택)
├── .github/
│   └── workflows/
│       └── resume.yml         # 이력서 자동 변환 워크플로우
└── README.md                  # 프로젝트 소개
```

---

## 📄 License

MIT License

---

## 📧 Contact

**GitHub**: [@jwleepro](https://github.com/jwleepro)