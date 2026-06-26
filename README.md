# GrayZone Reminder Prompt

<p align="center">
  <kbd><a href="#en">EN</a></kbd>
  |
  <kbd><a href="#kr">KR</a></kbd>
</p>

<a id="en"></a>

## English

Daily Todo Reminder is a reusable prompt package for generating an evidence-based daily todo list and a local HTML dashboard.

The prompt is written in Korean because the original workflow is Korean-first. It is designed to be copied into Codex, ChatGPT, Claude, or another agent runner that can read local project files.

### What It Does

- Reads configured work logs, daily summaries, work records, task lists, and repository status.
- Produces today's todo text from explicit evidence only.
- Creates or updates `TodoList (YYYY-MM-DD).html`.
- Provides a local HTTP preview link when the runner supports serving local files.
- Runs a first-run setup flow before creating files or registering automation.

### What It Does Not Do

- It does not edit source work logs, task lists, project documents, code, assets, scenes, Notion pages, or version-control state.
- It does not invent tasks when there is no evidence.
- It does not assume missing paths or permissions.

### Files

- `prompt.md`: the transfer prompt to paste into your agent or automation.
- `Templates/PROGRAMMER_DAILY_TODO_TEMPLATE.html`: default programmer-oriented HTML template.
- `Templates/ART_DAILY_TODO_TEMPLATE.html`: art-pipeline-oriented HTML template.
- `Templates/README.md`: template notes.

### Quick Start

1. Open `prompt.md`.
2. Fill the environment block near the top.
3. Set paths you do not use to `없음`.
4. Paste the prompt into your agent or scheduled automation.
5. On the first run, answer the setup questions one at a time.

The prompt intentionally asks for confirmation before writing setup state, creating folders, starting a local server, or registering recurring automation.

### Suggested Output Layout

```text
your-workspace/
  Daily Todo/
    TodoList (2026-06-26).html
    onboarding-state.json
```

You can choose any output path during first-run setup.

### Version

This repository starts from the V1.4 package.

### License

MIT License.

<a id="kr"></a>

## 한국어

Daily Todo Reminder는 명시적인 근거를 바탕으로 하루 할 일을 정리하고, 로컬 HTML 대시보드를 생성하는 재사용 가능한 프롬프트 패키지입니다.

프롬프트 본문은 한국어로 작성되어 있습니다. Codex, ChatGPT, Claude처럼 로컬 프로젝트 파일을 읽을 수 있는 에이전트 또는 자동화 실행기에 복사해서 사용하는 것을 기준으로 합니다.

### 하는 일

- 설정된 작업 로그, 일일 요약, 업무 기록, 작업 목록, 저장소 상태를 읽습니다.
- 명시적인 근거가 있는 오늘의 할 일만 정리합니다.
- `TodoList (YYYY-MM-DD).html`을 생성하거나 갱신합니다.
- 실행 환경이 지원하면 로컬 HTTP 미리보기 링크를 제공합니다.
- 파일 생성 또는 자동화 등록 전에 초회차 설정 흐름을 먼저 실행합니다.

### 하지 않는 일

- 원본 작업 로그, 작업 목록, 프로젝트 문서, 코드, 에셋, 씬, Notion 페이지, 버전 관리 상태를 수정하지 않습니다.
- 근거가 없는 작업을 만들어내지 않습니다.
- 누락된 경로나 권한을 임의로 추측하지 않습니다.

### 파일 구성

- `prompt.md`: 에이전트나 자동화에 붙여 넣는 전달용 프롬프트입니다.
- `Templates/PROGRAMMER_DAILY_TODO_TEMPLATE.html`: 프로그래머 업무 흐름용 기본 HTML 템플릿입니다.
- `Templates/ART_DAILY_TODO_TEMPLATE.html`: 아트 파이프라인 업무 흐름용 HTML 템플릿입니다.
- `Templates/README.md`: 템플릿 설명입니다.

### 빠른 시작

1. `prompt.md`를 엽니다.
2. 상단의 환경 설정 블록을 채웁니다.
3. 사용하지 않는 경로는 `없음`으로 둡니다.
4. 프롬프트를 에이전트나 예약 자동화에 붙여 넣습니다.
5. 첫 실행 때는 설정 질문에 하나씩 답합니다.

이 프롬프트는 설정 상태 저장, 폴더 생성, 로컬 서버 시작, 반복 자동화 등록 전에 의도적으로 확인 질문을 합니다.

### 권장 출력 구조

```text
your-workspace/
  Daily Todo/
    TodoList (2026-06-26).html
    onboarding-state.json
```

초회차 설정 중 원하는 출력 경로를 선택할 수 있습니다.

### 버전

이 저장소는 V1.4 패키지에서 시작합니다.

### 라이선스

MIT License.
