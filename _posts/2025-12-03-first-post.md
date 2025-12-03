---
layout: post
title: "GitHub Pages 게시 가이드"
date: 2025-12-03 09:00:00 +0900
categories: [guide, github-pages]
tags: [github, jekyll, minimal-mistakes]
---

아래는 GitHub Pages에 게시하는 기본 가이드입니다. 순서대로 따라하세요.
1) 계정 생성 → 2) _config.yml + Minimal Mistakes 적용 → 3) _posts에 글 추가 순으로 진행하면 됩니다.

추가 팁:
- 사이트 미리보기: 로컬에서 bundle exec jekyll serve 로 확인하세요.
- 커스텀 도메인: CNAME 파일을 루트에 추가하고 DNS를 설정하세요.
- 테마 설정 세부 옵션은 Minimal Mistakes 문서를 참고하세요: https://mmistakes.github.io/minimal-mistakes/

# 1) GitHub Pages 계정 생성

- GitHub 계정 만들기: https://github.com 에서 회원가입합니다.
- 퍼블릭 사용자/조직 사이트 만들기(선택): 리포지토리 이름을 "<your-username>.github.io"로 생성하면 기본 사용자 페이지가 됩니다.
  - 예: 내 사용자명이 jwleepro면 리포지토리 이름은 jwleepro.github.io
- 리포지토리 생성 후 Settings > Pages 에서 브랜치(main 또는 gh-pages)를 선택하고 저장하여 Pages를 활성화합니다.

# 2) _config.yml 파일 생성 후 Minimal Mistakes 테마 적용

- 권장 방법(간단): remote_theme 사용
  1. 루트에 _config.yml 파일을 생성합니다. 예시:

     title: "사이트 제목"
     description: "사이트 설명"
     baseurl: "" # GitHub Pages 사용자 사이트는 빈 문자열
     url: "https://<your-username>.github.io"
     remote_theme: "mmistakes/minimal-mistakes"
     plugins:
       - jekyll-remote-theme

  2. (로컬에서 빌드할 경우) Gemfile에 jekyll 및 jekyll-remote-theme 추가하고 bundle install 실행.

- 대안(테마를 직접 설치하여 사용): Gem 기반 설치
  1. Gemfile에 gem "minimal-mistakes-jekyll" 추가
  2. _config.yml에 theme: "minimal-mistakes-jekyll" 및 필요한 설정 추가
  3. 로컬에서 bundle install 및 bundle exec jekyll serve

- 주의사항:
  - GitHub README(리포지토리 설명)가 아닌 실제 사이트를 만드려면 리포지토리 루트에 index.html 또는 Jekyll 구조가 필요합니다.
  - remote_theme를 쓰면 테마를 별도로 복제할 필요 없이 바로 적용 가능합니다.

# 3) _posts/YYYY-MM-DD-제목.md 형태로 파일 생성

- Jekyll 글은 _posts 디렉터리에 아래 형식으로 저장합니다.
  - 파일명 예: _posts/2025-12-03-first-post.md

- 예시 파일 내용(이미 이 파일은 _posts/2025-12-03-first-post.md로 생성되어 있음):
