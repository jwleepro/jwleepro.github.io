---
layout: post
title:  "이력서 자동 생성 시스템 구축하기"
date:   2025-12-18 13:30:00 +0900
categories: [Automation, GitHub Actions]
---

> 마크다운으로 이력서를 작성하면 GitHub Actions가 자동으로 PDF와 DOCX를 생성합니다.

[![Build Resume](https://github.com/jwleepro/jwleepro.github.io/actions/workflows/resume.yml/badge.svg)](https://github.com/jwleepro/jwleepro.github.io/actions/workflows/resume.yml)

## 📑 목차

- [개요](#개요)
- [주요 기능](#주요-기능)
- [사용 방법](#사용-방법)
- [설정 가이드](#설정-가이드)
- [커스터마이징](#커스터마이징)
- [자주 묻는 질문](#자주-묻는-질문)
- [문제 해결](#문제-해결)

---

## 개요

이 시스템은 마크다운으로 작성한 이력서를 GitHub Actions를 통해 자동으로 **PDF**와 **DOCX** 파일로 변환합니다.

### 왜 마크다운으로 이력서를 작성할까요?

- ✅ **버전 관리**: Git으로 이력서 변경 이력 추적
- ✅ **자동화**: Push만 하면 PDF/DOCX 자동 생성
- ✅ **텍스트 기반**: 어디서든 수정 가능 (IDE, GitHub 웹, 모바일 앱)
- ✅ **재현 가능**: 동일한 소스에서 항상 동일한 결과물
- ✅ **무료**: GitHub Actions 무료 티어 활용

---

## 주요 기능

- 📝 **마크다운으로 편리하게 작성** - Git으로 버전 관리
- 🤖 **자동 변환** - Push하면 PDF/DOCX 자동 생성
- 🎨 **커스터마이징 가능** - CSS로 스타일 수정 가능
- 🌏 **한글 완벽 지원** - Noto Sans KR 폰트 사용
- 📦 **다운로드 간편** - GitHub Actions Artifacts에서 다운로드
- 🔄 **Release 자동 배포** - 태그 생성 시 자동으로 Release 첨부

---

## 🚀 사용 방법

### 1️⃣ 이력서 작성

`resume/resume.md` 파일을 생성하고 마크다운으로 이력서를 작성합니다:

```markdown
# 홍길동

**Backend Developer** | Seoul, Korea  
📧 email@example.com | 📱 010-1234-5678  
🔗 [GitHub](https://github.com/username) | [LinkedIn](https://linkedin.com/in/username)

---

## 👨‍💻 경력

### ABC 테크 | Senior Backend Developer
*2023.01 - 현재 (1년)*

- MSA 아키텍처 기반 주문 시스템 설계 및 개발 (Go, gRPC)
- Kafka를 활용한 이벤트 드리븐 아키텍처 구축으로 처리량 300% 향상
- CI/CD 파이프라인 구축 (GitHub Actions, ArgoCD)
- 팀 코드 리뷰 문화 정착 및 주니어 개발자 멘토링

### XYZ 스타트업 | Backend Developer
*2021.03 - 2022.12 (1년 9개월)*

- RESTful API 설계 및 개발 (Python, FastAPI)
- PostgreSQL 쿼리 최적화로 평균 응답 속도 50% 개선
- Redis 캐싱 전략 수립 및 적용
- Docker 기반 개발 환경 표준화

---

## 🛠️ 기술 스택

### Language
Go, Python, JavaScript/TypeScript

### Framework & Library
Echo, Gin, FastAPI, React

### Database
PostgreSQL, MySQL, MongoDB, Redis

### DevOps & Tools
Docker, Kubernetes, GitHub Actions, AWS (EC2, RDS, S3)

### Collaboration
Git, GitHub, Jira, Confluence, Slack

---

## 🚀 프로젝트

### 대규모 이커머스 주문 처리 시스템
*2023.06 - 2023.12*

**기술 스택**: Go, gRPC, Kafka, PostgreSQL, Redis, Kubernetes

- 일 평균 10만 건 이상의 주문 처리 시스템 설계 및 개발
- 이벤트 소싱 패턴 적용으로 데이터 정합성 보장
- 성능: 평균 응답 시간 100ms 이하, 99th percentile 300ms

**성과**
- 주문 처리 용량 3배 증가
- 시스템 장애 시간 월 평균 99.9% 가용성 달성

---

## 📚 학력

### 서울대학교 | 컴퓨터공학과
*2017.03 - 2021.02 | 학사*

- GPA: 3.8/4.5
- 주요 과목: 자료구조, 알고리즘, 데이터베이스, 운영체제, 컴퓨터 네트워크

---

## 🏆 자격증 & 수상

- **정보처리기사** | 한국산업인력공단 | 2020.08
- **AWS Certified Solutions Architect - Associate** | Amazon Web Services | 2022.05
- **해커톤 대상** | ABC 해커톤 | 2021.11

---

## 📝 기술 블로그 & 오픈소스

- **기술 블로그**: [blog.example.com](https://blog.example.com) - 월 평균 방문자 5,000명
- **GitHub**: 오픈소스 기여 - Kubernetes, Echo 등 다수 PR 머지
- **Speaker**: GopherCon Korea 2023 - "Go에서의 동시성 패턴" 발표

---

## 💬 자기소개

효율적이고 확장 가능한 백엔드 시스템 설계에 관심이 많은 개발자입니다. 
문제를 정의하고 기술적으로 해결하는 과정을 즐기며, 팀과 함께 성장하는 것을 중요하게 생각합니다.
```

### 2️⃣ GitHub에 Push

```bash
git add resume/resume.md
git commit -m "docs: 이력서 업데이트"
git push origin main
```

### 3️⃣ 자동 생성 확인

1. GitHub 저장소의 **Actions** 탭으로 이동
2. 워크플로우 실행 완료 대기 (보통 1-2분)
3. **Artifacts** 섹션에서 `resume` 다운로드
4. 압축 해제 후 `resume.pdf`와 `resume.docx` 확인

![GitHub Actions Artifacts](https://docs.github.com/assets/cb-61024/images/help/repository/artifact-drop-down-updated.png)

---

## ⚙️ 설정 가이드

### Prerequisites

1. GitHub 저장소 생성
2. GitHub Actions 활성화 (기본적으로 활성화됨)

### Step 1: GitHub Actions 워크플로우 생성

`.github/workflows/resume.yml` 파일을 생성합니다.

#### 옵션 A: Pandoc 방식 (추천) ✅

**장점**: PDF와 DOCX 모두 생성, 한글 지원 우수, 커스터마이징 가능

```yaml
name: Build Resume

on:
  push:
    branches: [ main ]
    paths:
      - 'resume/resume.md'
      - 'resume/resume-style.css'
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
      
      - name: Convert MD to PDF
        uses: docker://pandoc/latex:latest
        with:
          args: >-
            resume/resume.md
            -o resume.pdf
            --pdf-engine=xelatex
            -V CJKmainfont="Noto Sans KR"
            -V geometry:margin=2cm
            --metadata title="이력서"
      
      - name: Convert MD to DOCX
        uses: docker://pandoc/latex:latest
        with:
          args: >-
            resume/resume.md
            -o resume.docx
            --reference-doc=resume/custom-reference.docx
      
      - name: Upload artifacts
        uses: actions/upload-artifact@v3
        with:
          name: resume
          path: |
            resume.pdf
            resume.docx
          retention-days: 90
```

#### 옵션 B: md-to-pdf 방식 (간단)

**장점**: 설정 간단, Node.js 기반

```yaml
name: Build Resume

on:
  push:
    branches: [ main ]
    paths:
      - 'resume/resume.md'
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
      
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      
      - name: Install md-to-pdf
        run: npm install -g md-to-pdf
      
      - name: Convert to PDF
        run: md-to-pdf resume/resume.md --config-file resume/pdf-config.json
      
      - name: Upload PDF
        uses: actions/upload-artifact@v3
        with:
          name: resume-pdf
          path: resume/resume.pdf
          retention-days: 90
```

### Step 2: 워크플로우 권한 설정

1. GitHub 저장소 > **Settings** > **Actions** > **General**
2. **Workflow permissions** 섹션에서:
   - ✅ Read and write permissions 선택
   - ✅ Allow GitHub Actions to create and approve pull requests 체크

---

## 🎨 커스터마이징

### PDF 스타일 커스터마이징 (Pandoc)

`resume/resume-style.css` 파일 생성:

```css
/* 전체 레이아웃 */
body {
  font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, sans-serif;
  font-size: 11pt;
  line-height: 1.6;
  color: #333;
  max-width: 210mm;
  margin: 0 auto;
  padding: 20mm;
}

/* 제목 스타일 */
h1 {
  color: #2c3e50;
  font-size: 2.5em;
  font-weight: 700;
  margin-bottom: 0.2em;
  border-bottom: 4px solid #3498db;
  padding-bottom: 0.3em;
}

h2 {
  color: #34495e;
  font-size: 1.5em;
  font-weight: 600;
  margin-top: 1.5em;
  margin-bottom: 0.5em;
  border-bottom: 2px solid #ecf0f1;
  padding-bottom: 0.2em;
}

h3 {
  color: #555;
  font-size: 1.2em;
  font-weight: 600;
  margin-top: 1em;
  margin-bottom: 0.3em;
}

/* 링크 스타일 */
a {
  color: #3498db;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

/* 리스트 스타일 */
ul, ol {
  margin-left: 1.5em;
  margin-bottom: 1em;
}

li {
  margin-bottom: 0.3em;
}

/* 강조 텍스트 */
strong {
  color: #2c3e50;
  font-weight: 600;
}

em {
  color: #7f8c8d;
  font-style: italic;
}

/* 코드 블록 */
code {
  background-color: #f8f9fa;
  padding: 0.2em 0.4em;
  border-radius: 3px;
  font-family: 'Consolas', 'Monaco', monospace;
  font-size: 0.9em;
}

/* 구분선 */
hr {
  border: none;
  border-top: 2px solid #ecf0f1;
  margin: 2em 0;
}

/* 페이지 브레이크 */
@media print {
  h2 {
    page-break-after: avoid;
  }
  
  h3 {
    page-break-after: avoid;
  }
}
```

워크플로우에서 CSS 적용:

```yaml
- name: Convert MD to PDF
  uses: docker://pandoc/latex:latest
  with:
    args: >-
      resume/resume.md
      -o resume.pdf
      --pdf-engine=xelatex
      -V CJKmainfont="Noto Sans KR"
      --css=resume/resume-style.css
      --metadata title="이력서"
```

### DOCX 스타일 커스터마이징 (Pandoc)

1. DOCX 템플릿 파일 생성:

```bash
pandoc -o custom-reference.docx --print-default-data-file reference.docx
```

2. Word로 `custom-reference.docx` 열고 스타일 편집
3. `resume/` 디렉토리에 저장
4. 워크플로우에서 참조:

```yaml
- name: Convert MD to DOCX
  uses: docker://pandoc/latex:latest
  with:
    args: >-
      resume/resume.md
      -o resume.docx
      --reference-doc=resume/custom-reference.docx
```

### md-to-pdf 설정 파일

`resume/pdf-config.json`:

```json
{
  "stylesheet": "resume/resume-style.css",
  "body_class": "markdown-body",
  "css": "body { font-family: 'Noto Sans KR', sans-serif; }",
  "pdf_options": {
    "format": "A4",
    "margin": {
      "top": "20mm",
      "right": "20mm",
      "bottom": "20mm",
      "left": "20mm"
    },
    "printBackground": true
  }
}
```

---

## 📌 고급 기능

### 1. GitHub Release 자동 배포

태그를 생성하면 자동으로 Release에 PDF/DOCX를 첨부합니다.

워크플로우에 추가:

```yaml
- name: Create Release
  uses: softprops/action-gh-release@v1
  if: startsWith(github.ref, 'refs/tags/')
  with:
    files: |
      resume.pdf
      resume.docx
    body: |
      ## 📄 이력서
      
      자동 생성된 이력서입니다.
      
      - `resume.pdf` - PDF 버전
      - `resume.docx` - Word 버전
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

사용법:

```bash
git tag v1.0.0 -m "2024년 1월 이력서"
git push origin v1.0.0
```

### 2. 여러 버전의 이력서 관리

직무별로 다른 이력서를 관리:

```
resume/
├── resume-backend.md
├── resume-devops.md
└── resume-fullstack.md
```

워크플로우 수정:

```yaml
on:
  push:
    paths:
      - 'resume/*.md'

jobs:
  build:
    strategy:
      matrix:
        resume: [backend, devops, fullstack]
    
    steps:
      - name: Convert to PDF
        run: |
          pandoc resume/resume-${{ matrix.resume }}.md \
            -o resume-${{ matrix.resume }}.pdf
```

### 3. 이력서 미리보기 (Pull Request Comment)

PR에 PDF 미리보기 링크 자동 생성:

```yaml
- name: Comment PR
  uses: actions/github-script@v6
  if: github.event_name == 'pull_request'
  with:
    script: |
      github.rest.issues.createComment({
        issue_number: context.issue.number,
        owner: context.repo.owner,
        repo: context.repo.repo,
        body: '📄 이력서가 생성되었습니다! Artifacts에서 다운로드하세요.'
      })
```

---

## ❓ 자주 묻는 질문

### Q1. GitHub Actions 실행 비용이 궁금해요

**A**: GitHub Actions는 Public 저장소에서는 무료입니다. Private 저장소는 월 2,000분 무료 할당량이 있으며, 이력서 변환은 1-2분이면 완료되므로 충분합니다.

### Q2. 한글이 깨져요

**A**: Pandoc 방식에서 `-V CJKmainfont="Noto Sans KR"` 옵션이 제대로 포함되었는지 확인하세요. 또는 `Nanum Gothic` 등 다른 폰트로 변경해보세요.

### Q3. PDF 스타일을 더 예쁘게 만들고 싶어요

**A**: 
1. `resume-style.css` 파일로 CSS 커스터마이징
2. LaTeX 템플릿 사용 (고급)
3. 전문 이력서 템플릿 라이브러리 활용 (예: [jsonresume](https://jsonresume.org/))

### Q4. DOCX에서 스타일이 적용 안 돼요

**A**: `--reference-doc` 옵션으로 Word 템플릿을 지정해야 합니다. 위의 "DOCX 스타일 커스터마이징" 섹션을 참고하세요.

### Q5. Actions에서 파일을 찾을 수 없다고 나와요

**A**: 워크플로우의 `paths` 설정과 실제 파일 경로가 일치하는지 확인하세요. 상대 경로를 사용합니다.

### Q6. 매번 Artifacts에서 다운로드하기 번거로워요

**A**: GitHub Release 자동 배포를 설정하면 태그 생성 시 Release 페이지에서 바로 다운로드할 수 있습니다.

---

## 🔧 문제 해결

### 워크플로우가 실행되지 않아요

1. **Repository Settings 확인**
   - Settings > Actions > General
   - "Allow all actions and reusable workflows" 선택

2. **파일 경로 확인**
   ```yaml
   on:
     push:
       paths:
         - 'resume/resume.md'  # 실제 파일 경로와 일치해야 함
   ```

3. **브랜치 이름 확인**
   ```yaml
   on:
     push:
       branches: [ main ]  # 또는 master
   ```

### PDF 생성 시 한글이 깨져요

**해결 방법 1**: 폰트 변경

```yaml
-V CJKmainfont="Nanum Gothic"  # 또는 "Malgun Gothic"
```

**해결 방법 2**: XeLaTeX 대신 LuaLaTeX 사용

```yaml
--pdf-engine=lualatex
```

### Actions 실행 시간이 너무 길어요

**원인**: Docker 이미지 다운로드 시간

**해결책**: GitHub Actions 캐싱 사용

```yaml
- name: Cache Pandoc
  uses: actions/cache@v3
  with:
    path: ~/.pandoc
    key: ${{ runner.os }}-pandoc-${{ hashFiles('resume/*.md') }}
```

### Artifacts 다운로드가 안 돼요

1. **Workflow permissions 확인**
   - Settings > Actions > General
   - "Read and write permissions" 선택

2. **Artifact retention 확인**
   ```yaml
   - name: Upload artifacts
     uses: actions/upload-artifact@v3
     with:
       retention-days: 90  # 보관 기간 설정
   ```

---

## 🛠️ 기술 스택

### 문서 변환
- **Pandoc** - 범용 문서 변환 도구
- **XeLaTeX / LuaLaTeX** - PDF 생성 엔진
- **md-to-pdf** - Node.js 기반 MD to PDF 변환기

### CI/CD
- **GitHub Actions** - 자동화 워크플로우
- **Docker** - Pandoc 컨테이너 실행

### 폰트
- **Noto Sans KR** - Google Fonts, 한글 지원
- **Nanum Gothic** - 네이버, 한글 무료 폰트

---

## 📖 참고 자료

- [Pandoc 공식 문서](https://pandoc.org/MANUAL.html)
- [GitHub Actions 문서](https://docs.github.com/en/actions)
- [md-to-pdf](https://github.com/simonhaenisch/md-to-pdf)
- [JSON Resume](https://jsonresume.org/) - 이력서 표준 포맷
- [Awesome Resume](https://github.com/resumejob/awesome-resume) - 이력서 템플릿 모음

---

## 📝 License

MIT License

---

## 💬 피드백

이 가이드에 대한 피드백이나 개선 제안이 있으시면 [Issues](https://github.com/jwleepro/jwleepro.github.io/issues)에 남겨주세요!
