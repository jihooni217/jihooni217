<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=220&section=header&text=Jihoon%20Lee&fontSize=64&fontColor=ffffff&fontAlignY=38&desc=AI%20%C2%B7%20Backend%20Developer&descSize=22&descAlignY=60&animation=fadeIn" width="100%" alt="Jihoon Lee" />

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3200&pause=900&color=60A5FA&center=true&vCenter=true&width=640&lines=LLM+Agents+that+get+verified+before+they+ship;FastAPI+%C2%B7+SSE+%C2%B7+Structured+Outputs+%C2%B7+Guardrail;Built+an+Upstage+Solar+Pro+4+demo" alt="LLM Agents that get verified before they ship" /></a>
</p>

<p align="center">
  <b>AI가 낸 답을 그대로 쓰지 않고, 검사를 통과한 것만 적용하는 시스템을 만듭니다.</b><br>
  LLM Agent · FastAPI · SSE · OpenCV · YOLO
</p>

<p align="center">
  <a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/FlowLight-Live%20Demo-f97316?style=flat-square&logo=googlechrome&logoColor=white" alt="FlowLight Live Demo" /></a>
  <a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/%EC%95%8C%EB%B0%94%EA%B0%80%EB%93%9C-Live%20App-1d4ed8?style=flat-square&logo=googlechrome&logoColor=white" alt="알바가드 Live App" /></a>
  <a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-%EC%86%8C%EA%B0%9C%20%EA%B8%80-7c3aed?style=flat-square" alt="Upstage Blog 소개 글" /></a>
  <img src="https://img.shields.io/badge/Daegu%20University-Software-0f172a?style=flat-square" alt="Daegu University" />
</p>

<br>

## 📌 한눈에 보기

| 프로젝트 | 무엇 | 내 자리 | 바로 보기 |
|---|---|---|---|
| 🚦 [FlowLight](https://github.com/jihooni217/FlowLight-AI-Traffic-Signal) | LLM Agent 3개가 교차로 신호를 계획하는 데모 | 레포 주인 | [Live Demo](https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/) |
| 🚗 [Raspbot 자율주행](https://github.com/jihooni217/raspbot-pbl-3team) | 카메라 한 대로 트랙을 도는 소형 자율주행차 | PBL 3조 조장 | [코드·영상](https://github.com/jihooni217/raspbot-pbl-3team) |
| 🛡️ [알바가드](https://github.com/jihooni217/albaguard) | 못 받은 알바비를 기록으로 찾는 모바일 웹앱 | 레포 주인 | [앱 열기](https://jihooni217.github.io/albaguard/) |
| 🎁 [KeepCon](https://github.com/Jiwonang/KeepCon) | 기프티콘을 모아 가족·친구와 함께 쓰는 앱 | 팀 프로젝트 참여 | [저장소](https://github.com/Jiwonang/KeepCon) |

<br>

## 🚦 FlowLight

**Upstage Solar Pro 4** 로 교차로 신호를 분석 · 계획 · 평가하는 Multi-Agent 데모입니다.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://raw.githubusercontent.com/jihooni217/FlowLight-AI-Traffic-Signal/main/docs/flowlight_live_demo.gif" width="640" alt="FlowLight 데모 화면: Agent가 신호 계획을 단계별로 보여 줌" /></a>

**내 역할**
- Agent 세 개의 프롬프트와 JSON Schema를 정했습니다.
- FastAPI 서버와 SSE 스트리밍, Guardrail을 만들었습니다.
- 시드 10개 비교를 설계해 돌리고, 발표했습니다.

**어떻게**
- Agent 출력은 **JSON Schema** 로 형식을 고정합니다.
- 규칙 기반 **Guardrail** 을 통과한 계획만 신호에 적용합니다.
- **FastAPI + SSE** 로 판단 과정을 단계별로 보여 줍니다.
- 서울시 실측 교통량(숭례문 일대 하루치)을 두 번째 프로파일로 넣었습니다.
- 설치 없이 브라우저에서 바로 체험합니다. 녹화된 실제 응답을 재생합니다.

**결과**
- 보행자 없는 교차로, 시드 10개 평균: 통과 차량 +11%, 정지 차량 −16%.
- 비교 대상은 사람이 없어도 매 주기 보행 신호를 주는 고정 시간표입니다.
- 차이의 대부분은 빈 보행 신호 시간을 차량에 돌려준 몫입니다. 레포에 근거와 한계를 함께 적었습니다.
- 테스트 286개.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/Live%20Demo-f97316?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Demo" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>
<a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-7c3aed?style=for-the-badge" alt="Upstage Blog" /></a>

<br><br>

## 🚗 Raspbot 자율주행

카메라 한 대로 트랙 한 바퀴를 스스로 달리는 소형 자율주행차입니다. **Raspberry Pi 5**, 대구대 PBL 3조.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://raw.githubusercontent.com/jihooni217/raspbot-pbl-3team/main/docs/media/outer_lap_4x.gif" width="640" alt="Raspbot이 트랙 바깥 큰길을 한 바퀴 도는 모습 (4배속)" /></a>

**내 역할** (조장 · 주도)
- 기능마다 지시서(목표, 규칙표, 숫자 성공 기준, 안전 규칙)를 직접 썼습니다.
- 발표 시연 코드를 한 프로그램으로 합치고, 실제 트랙에서 7판 모두 완주할 때까지 맞췄습니다.
- 주행 기록과 카메라 영상을 나란히 놓고 원인을 찾았습니다. 큰길 주행 기록만 60판이 넘습니다.

**어떻게**
- OpenCV로 차선을 따라가고, 바닥 색에 따라 빨라지거나 느려집니다.
- YOLO로 사람·STOP 표지를 보면 멈춥니다. START 선에서도 스스로 멈춥니다.
- **지시서 주도 AI 협업**: 제가 규칙과 숫자 성공 기준을 쓰고, Codex가 코드를 씁니다.
- 바퀴를 돌리기 전에 사진 시험·가짜 장치 시험으로 먼저 검증합니다.
- 글 명령은 AI가 정해진 동작 11개 중 하나만 고르는 Guardrail 구조입니다.

**결과**
- 실제 트랙 큰길 7판 모두 완주 (발표일, 37~44초).
- 사진 시험에서 차선 모서리 판단 28% → 81%.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/raspbot-pbl-3team/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>

<br><br>

## 🛡️ 알바가드

시급제 알바생이 혼자 출퇴근을 기록하고, 덜 받은 급여를 찾아 요청하는 모바일 웹앱입니다.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://raw.githubusercontent.com/jihooni217/albaguard/main/public/og.png" width="640" alt="알바가드: 못 받은 알바비, 기록으로 찾는 앱" /></a>

- 기록 → 실제 입금액과 비교 → 정산 요청 문구까지 이어집니다.
- 기록을 고치거나 지우면 전후 시각과 사유가 남습니다.
- 기록마다 **SHA-256** 확인 번호와 서버 등록 시각을 남깁니다 (**Supabase**).
- 누구나 확인 페이지에서 확인 번호로 등록 시각을 볼 수 있습니다.
- 서버에는 확인 번호만 갑니다. 근무지·시각·금액은 폰 밖으로 나가지 않습니다.
- 근무 기록·수정 이력·계산 근거를 증빙 PDF 한 묶음으로 저장합니다.
- **React + Vite**, GitHub Actions로 GitHub Pages에 자동 배포합니다.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/%EC%95%B1%20%EC%97%B4%EA%B8%B0-1d4ed8?style=for-the-badge&logo=googlechrome&logoColor=white" alt="앱 열기" /></a>
<a href="https://github.com/jihooni217/albaguard"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://jihooni217.github.io/albaguard/verify.html"><img src="https://img.shields.io/badge/%ED%99%95%EC%9D%B8%20%ED%8E%98%EC%9D%B4%EC%A7%80-0f766e?style=for-the-badge" alt="확인 페이지" /></a>

<br><br>

## 🎁 KeepCon <sub>팀 프로젝트 참여</sub>

여러 앱에 흩어진 기프티콘을 한 곳에서 관리하고, 그룹 공유로 가족·친구가 함께 쓰는 **Flutter** 앱입니다.

- 원본 저장소는 [Jiwonang/KeepCon](https://github.com/Jiwonang/KeepCon)이고, 저는 팀원으로 참여했습니다.
- 4개 페이지(홈 · 스캔·추가 · 공유 · 로그인/설정)를 담당자별로 나눠 함께 개발했습니다.
- 공유 모델은 `lib/shared` 한 곳에만 둡니다. CI의 SSOT guard가 재정의를 막습니다.
- `main`·`develop`에는 직접 push하지 않고, PR과 CI를 통과해야 합칩니다.
- 기술: Flutter(Dart) · Riverpod · Firebase(Auth, Firestore)

<a href="https://github.com/Jiwonang/KeepCon"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>

<br><br>

## 🧭 일하는 방식

- **AI 출력은 검사하고 적용한다**: 형식을 고정하고, Guardrail을 통과한 것만 쓴다.
- **움직이기 전에 시험한다**: 실제 로봇·실제 서비스 전에 가짜 장치와 테스트로 먼저 확인한다.
- **AI에게는 지시서로 맡긴다**: 규칙과 숫자 성공 기준은 사람이 쓰고, 코드는 AI가 쓴다.
- **바로 볼 수 있게 낸다**: 설치 없이 브라우저에서 열리는 데모와 앱으로 공개한다.

## Stack

<p align="center">
  <a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=python,fastapi,opencv,raspberrypi,js,react,vite,supabase,html,unity,cs,git,github&perline=13" alt="Python, FastAPI, OpenCV, Raspberry Pi, JavaScript, React, Vite, Supabase, HTML, Unity, C#, Git, GitHub" /></a>
</p>

## 🔧 Recent

- 2026-11 · Raspbot 자율주행: 대구대 PBL 조장, 실제 트랙 한 바퀴 자율주행 시연
- 2026-10 · [Upstage Education 블로그](https://edu.upstage.ai/blog/daegu-bootcamp-flowlight)에 FlowLight 소개 글 게재
- FlowLight · 알바가드: 설치 없이 쓰는 공개 데모와 웹앱 배포

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=120&section=footer" width="100%" alt="" />
