---
title: "GitHub Pages와 커스텀 도메인(linacker.dev)으로 기술 블로그 구축하기"
description: "가비아에서 등록한 linacker.dev 도메인을 GitHub Pages와 Astro 모던 블로그에 연결한 과정과 설정 가이드"
pubDate: 2026-09-06
tags: ["GitHubPages", "Astro", "가비아", "도메인연결"]
---

## 블로그 구축 배경

개인 도메인(`linacker.dev`)을 가비아에서 구매한 뒤, 이를 GitHub Pages와 연동하여 유지보수가 간편하면서도 성능과 디자인이 뛰어난 블로그를 만들기로 결정했습니다.

옵션 B인 **Astro 프레임워크**를 선택한 이유는 다음과 같습니다:
* **Zero JS by default:** 필요한 부분만 자바스크립트를 로드하여 로딩 속도가 압도적으로 빠름
* **마크다운(Markdown) 네이티브 지원:** `src/content/blog` 폴더에 `.md` 파일만 작성하면 자동으로 포스팅
* **GitHub Actions 자동 배포:** Git commit & push만으로 전 세계 CDN에 즉각 배포

---

## 도메인 연결 3단계 요약

가비아에서 구매한 도메인을 GitHub Pages에 연결하는 절차는 크게 세 단계로 이루어집니다.

### 1. GitHub 저장소에 CNAME 파일 추가
블로그의 `public/` 디렉토리에 다음과 같이 내용이 단 한 줄인 `CNAME` 파일을 둡니다.

```text
linacker.dev
```

### 2. 가비아(Gabia) DNS 레코드 설정
가비아 My가비아 > DNS 관리툴에서 다음 레코드들을 등록합니다:

* **루트 도메인 (A 레코드 4개)**:
  * 타입: `A`, 호스트: `@`, 값: `185.199.108.153`
  * 타입: `A`, 호스트: `@`, 값: `185.199.109.153`
  * 타입: `A`, 호스트: `@`, 값: `185.199.110.153`
  * 타입: `A`, 호스트: `@`, 값: `185.199.111.153`
* **서브도메인 (CNAME 레코드 1개)**:
  * 타입: `CNAME`, 호스트: `www`, 값: `linacker-dev.github.io.`

### 3. GitHub Pages 설정에서 Enforce HTTPS 활성화
GitHub 저장소의 `Settings` -> `Pages` 메뉴에서 Custom domain이 `linacker.dev`로 잡혀 있는지 확인하고, DNS 전파 후 **Enforce HTTPS** 옵션을 켭니다.

이제 누구나 안전한 HTTPS 프로토콜로 `https://linacker.dev`에 접속할 수 있게 됩니다!
