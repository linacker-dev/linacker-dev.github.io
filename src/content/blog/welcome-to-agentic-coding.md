---
title: "AI Agentic Coding의 시대가 열리다"
description: "단순한 코드 생성을 넘어, 자율적으로 문제를 정의하고 도구를 활용하는 AI Agentic Coding에 대한 이야기"
pubDate: 2026-09-06
tags: ["AI", "AgenticCoding", "LLM", "개발일기"]
---

## 발코딩에서 Agentic Coding으로

과거에는 수많은 문서를 뒤지고, 오타 하나 때문에 몇 시간 동안 디버깅하던 시절이 있었습니다. 일명 '발코딩'이라 자조하며 밤을 새우던 날들이 이제는 새로운 패러다임을 맞이하고 있습니다.

지금 우리는 **AI Agentic Coding**의 시대에 살고 있습니다.

### 자율 에이전트(Autonomous Agents)의 등장

기존의 단순 프롬프트 기반 코드 생성과 에이전틱 코딩의 가장 큰 차이는 무엇일까요?

1. **컨텍스트 이해(Deep Context):** 프로젝트 전체 구조와 의존성을 파악합니다.
2. **도구 활용(Tool Calling):** 터미널 명령어 실행, 파일 읽기/쓰기, 브라우저 검색 등을 능동적으로 수행합니다.
3. **계획 및 검증(Planning & Verification):** 문제를 해결하기 전 계획을 수립하고, 실행 후 테스트를 통해 결과를 검증합니다.

```typescript
// AI Agentic Workflow Example
interface AgentAction {
  plan: string[];
  tool: "run_command" | "write_file" | "verify";
  status: "executing" | "completed";
}

const runAgentTask = async (task: string): Promise<void> => {
  console.log(`Starting autonomous task: ${task}`);
  // 에이전트가 자율적으로 계획을 수립하고 실행합니다.
};
```

### 앞으로 이 블로그에서 다룰 이야기

* 자율 AI 에이전트와 함께하는 개발 워크플로우
* 최신 LLM 도구 및 IDE 활용 팁
* 실전 프로젝트 개발기 및 아키텍처 고민

AI와 함께 더 높고 멀리 도약하는 여정을 이 블로그에 기록해 나가겠습니다.
