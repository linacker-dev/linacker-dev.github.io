# Linacker 의 발코딩 (linacker.dev)

> "이제는 AI Agentic Coding 을 주로 다룹니다."

Astro와 GitHub Pages로 구축된 기술 블로그입니다. 가비아에서 등록한 커스텀 도메인 `linacker.dev`에 연결되어 배포됩니다.

---

## 🚀 빠른 시작 (로컬 개발)

### 1. 의존성 설치
```bash
npm install
```

### 2. 로컬 개발 서버 실행
```bash
npm run dev
```
브라우저에서 `http://localhost:4321`에 접속하여 실시간으로 확인합니다.

### 3. 사이트 빌드
```bash
npm run build
```

---

## ✍️ 새 글 작성 방법

`src/content/blog/` 디렉토리에 마크다운(`.md`) 파일을 생성합니다.

```markdown
---
title: "게시글 제목"
description: "게시글 요약 설명"
pubDate: 2026-09-06
tags: ["태그1", "태그2"]
---

여기에 본문 내용을 마크다운으로 작성하세요.
```

파일을 저장하고 GitHub `main` 브랜치에 `git push`하면 GitHub Actions에 의해 자동으로 배포됩니다!

---

## 🌐 도메인 연결 정보

* **Custom Domain:** `linacker.dev` (또는 `www.linacker.dev`)
* **GitHub Pages Repo:** `linacker-dev/linacker-dev.github.io`
* **배포 엔진:** GitHub Actions (`.github/workflows/deploy.yml`)
