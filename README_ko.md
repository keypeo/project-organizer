# 🗂️ 프로젝트 오거나이저 Skill

[English](README.md) | [中文](README_zh.md) | [日本語](README_ja.md)

> 모든 프로젝트에서 AI 어시스턴트가 자동으로 구조화된 파일 관리를 수행하는 Skill입니다.

## 기능

설치하면 AI 어시스턴트가 모든 프로젝트에서 **능동적으로 파일을 정리**합니다. 긴 작업 세션 후에 폴더가 어지러워지는 일은 더 이상 없습니다.

| 트리거 | 동작 |
|--------|------|
| 새 프로젝트 시작 | 표준화된 폴더 구조를 제안하고 생성 |
| 작업 중 파일 생성 | 각 파일을 올바른 폴더에 자동 배치 |
| "정리해줘", "깔끔하게" 지시 | 프로젝트 폴더 전체를 스캔하고 재구성 |
| 3~5회 파일 작업마다 | 정리 체크포인트 실행 |

## 핵심 규칙

### 📁 표준 프로젝트 구조

```
project-name/
├── README.md        — 프로젝트 설명, 상태, 규칙
├── drafts/          — 작업 초안, 반복 버전
├── figures/         — 이미지, 차트, 다이어그램
├── scripts/         — 출력을 생성하는 코드
├── references/      — 참고 자료, 템플릿
├── output/          — 최종 산출물만
└── archive/         — 대체된 이전 버전 (삭제가 아닌 이동)
```

### 📝 명명 규칙

| ✅ 올바름 | ❌ 잘못됨 |
|----------|----------|
| `report_v1.docx` | `report_final.docx` |
| `report_v2.docx` | `report_new.docx` |
| `submission_20260226.docx` | `report_final_FINAL.docx` |

### 🏗️ 도메인별 템플릿

다음 템플릿이 내장되어 있습니다:
- **학술 논문** — drafts / figures / scripts / references / output / archive
- **웹 애플리케이션** — src / public / scripts / docs / dist
- **데이터 분석** — data / notebooks / scripts / figures / output

## 설치

`project-organizer/` 폴더를 skills 디렉토리에 배치하세요:

```
~/.gemini/antigravity/skills/project-organizer/
```

모든 새 대화에서 자동으로 활성화됩니다.

## 라이선스

MIT
