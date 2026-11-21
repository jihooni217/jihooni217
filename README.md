<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=220&section=header&text=Jihoon%20Lee&fontSize=64&fontColor=ffffff&fontAlignY=38&desc=AI%20%C2%B7%20Backend%20Developer&descSize=22&descAlignY=60&animation=fadeIn" width="100%" alt="Jihoon Lee" />

<p align="center">
  대구대학교 소프트웨어학과에서 AI와 백엔드를 공부하고 있습니다.<br>
  LLM을 붙인 서버와, 누구나 바로 열어 볼 수 있는 데모를 주로 만듭니다.
</p>

<p align="center">
  <a href="README.en.md"><img src="https://img.shields.io/badge/English-README-0f172a?style=flat-square" alt="English README" /></a>
  <a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/FlowLight-Live%20Demo-f97316?style=flat-square&logo=googlechrome&logoColor=white" alt="FlowLight Live Demo" /></a>
  <a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/%EC%95%8C%EB%B0%94%EA%B0%80%EB%93%9C-Live%20App-1d4ed8?style=flat-square&logo=googlechrome&logoColor=white" alt="알바가드 Live App" /></a>
  <a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-%EC%86%8C%EA%B0%9C%20%EA%B8%80-7c3aed?style=flat-square" alt="Upstage Blog 소개 글" /></a>
  <img src="https://img.shields.io/badge/Daegu%20University-Software-0f172a?style=flat-square" alt="Daegu University" />
</p>

<br>

## 📌 한눈에 보기

| 프로젝트 | 무엇 | 역할 | 바로 보기 |
|---|---|---|---|
| 🚦 [FlowLight](https://github.com/jihooni217/FlowLight-AI-Traffic-Signal) | LLM Agent 3개가 교차로 신호를 짜는 데모 | 개인 프로젝트 | [Live Demo](https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/) |
| 🎁 [KeepCon](https://github.com/Jiwonang/KeepCon) | 기프티콘을 모아 가족·친구와 나눠 쓰는 앱 | 팀원 | [저장소](https://github.com/Jiwonang/KeepCon) |
| 🛡️ [알바가드](https://github.com/jihooni217/albaguard) | 못 받은 알바비를 기록으로 찾는 모바일 웹앱 | 개인 프로젝트 | [앱 열기](https://jihooni217.github.io/albaguard/) |
| 🚗 [Raspbot 자율주행](https://github.com/jihooni217/raspbot-pbl-3team) | 카메라 한 대로 트랙을 도는 작은 자율주행차 | PBL 3조 조장 | [코드·영상](https://github.com/jihooni217/raspbot-pbl-3team) |

<br>

## 🚦 FlowLight

Upstage Solar Pro 4로 교차로 신호를 짜는 Multi-Agent 데모입니다. 횡단보도에 사람이 없으면 보행 신호를 건너뛰고, 어린이나 휠체어 이용자가 건널 때는 시간을 늘려 주자는 생각에서 시작했습니다.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://raw.githubusercontent.com/jihooni217/FlowLight-AI-Traffic-Signal/main/docs/flowlight_live_demo.gif" width="640" alt="FlowLight 데모 화면: Agent가 신호 계획을 단계별로 보여 줌" /></a>

Agent 세 개가 차례로 교통 상황을 분석하고, 신호 시간을 계획하고, 그 계획을 다시 평가합니다. 출력은 JSON Schema로 형식을 묶어 두고, 규칙 기반 Guardrail(최소 녹색 시간, 주기 합계)을 통과한 계획만 시뮬레이터에 넣습니다. 판단 과정은 FastAPI와 SSE로 한 단계씩 화면에 보여 줍니다.

프롬프트와 Schema 설계, 서버와 Guardrail, 시뮬레이터 연결, 비교 실험, 발표까지 직접 했습니다.

- 보행자가 없는 교차로에서 시드 10개 평균으로 통과 차량은 11% 늘고 정지 차량은 16% 줄었습니다. 사람이 없어도 매번 보행 신호를 주는 고정 시간표와 비교한 결과입니다.
- 다만 이 차이는 대부분 비어 있던 보행 시간을 차에 돌려준 덕분이었습니다. LLM이 두 방향 시간을 다시 나눈 효과는 오차 범위 안이었습니다.
- 서울 숭례문 일대에서 실제로 센 교통량(하루치)도 넣어 두었고, 테스트는 286개입니다.
- 공개 데모는 서버 없이 돌아가도록, 미리 받아 둔 실제 응답을 재생합니다.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/Live%20Demo-f97316?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Demo" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>
<a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-7c3aed?style=for-the-badge" alt="Upstage Blog" /></a>

<br><br>

## 🎁 KeepCon <sub>팀 프로젝트</sub>

여러 앱에 흩어진 기프티콘을 한곳에 모으고, 가족이나 친구와 그룹으로 나눠 쓰는 Flutter 앱입니다. 원본 저장소는 [Jiwonang/KeepCon](https://github.com/Jiwonang/KeepCon)이고, 저는 팀원으로 참여했습니다.

홈, 스캔·추가, 공유, 로그인/설정 네 페이지를 담당자별로 나눠 동시에 만들었습니다. 여러 페이지가 같이 쓰는 모델은 `lib/shared` 한곳에만 두고 CI가 중복 정의를 막았습니다. `main`과 `develop`에는 PR을 열고 CI를 통과해야만 합칠 수 있었습니다.

Flutter(Dart), Riverpod, Firebase(Auth, Firestore)를 썼습니다.

<a href="https://github.com/Jiwonang/KeepCon"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>

<br><br>

## 🛡️ 알바가드

시급제로 일하는 대학생이 출퇴근을 직접 기록해 두고, 덜 받은 알바비를 찾아 요청할 수 있게 돕는 모바일 웹앱입니다.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://raw.githubusercontent.com/jihooni217/albaguard/main/public/og.png" width="640" alt="알바가드: 못 받은 알바비, 기록으로 찾는 앱" /></a>

- 기록과 실제 입금액을 비교해 차액을 찾고, 사장에게 보낼 정산 요청 문구까지 만들어 줍니다.
- 기록을 고치거나 지우면 언제, 왜 바꿨는지가 남습니다.
- 기록마다 SHA-256으로 확인 번호를 만들어 Supabase에 등록 시각과 함께 남깁니다. 누구나 확인 페이지에서 그 시각을 조회할 수 있습니다.
- 서버로 가는 건 확인 번호, 기록 번호, 무작위 기기 번호뿐입니다. 근무지와 시각, 금액은 폰에만 남습니다.
- 근무 기록, 수정 이력, 계산 근거를 PDF 한 묶음으로 뽑을 수 있습니다.
- React와 Vite로 만들었고, GitHub Actions로 GitHub Pages에 배포합니다.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/%EC%95%B1%20%EC%97%B4%EA%B8%B0-1d4ed8?style=for-the-badge&logo=googlechrome&logoColor=white" alt="앱 열기" /></a>
<a href="https://github.com/jihooni217/albaguard"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://jihooni217.github.io/albaguard/verify.html"><img src="https://img.shields.io/badge/%ED%99%95%EC%9D%B8%20%ED%8E%98%EC%9D%B4%EC%A7%80-0f766e?style=for-the-badge" alt="확인 페이지" /></a>

<br><br>

## 🚗 Raspbot 자율주행

카메라 한 대로 트랙을 스스로 한 바퀴 도는 작은 자율주행차입니다. Raspberry Pi 5를 썼고, 대구대 PBL 3조 조장으로 참여했습니다.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://raw.githubusercontent.com/jihooni217/raspbot-pbl-3team/main/docs/media/outer_lap_4x.gif" width="640" alt="Raspbot이 트랙 바깥 큰길을 한 바퀴 도는 모습 (4배속)" /></a>

OpenCV로 차선을 따라가면서 바닥 색에 따라 속도를 바꾸고, YOLO로 사람이나 STOP 표지를 보면 멈춥니다. START 선에 돌아오면 스스로 섭니다.

코드는 Codex가 썼고, 저는 기능마다 지시서(목표, 규칙표, 숫자로 된 성공 기준, 안전 규칙)를 쓰는 쪽이었습니다. 바퀴를 돌리기 전에는 사진과 가짜 장치로 먼저 시험했고, 잘못 달리면 주행 기록과 카메라 영상을 나란히 놓고 원인을 찾았습니다. 큰길 주행 기록만 60판이 넘습니다. 발표 시연 코드는 이 기능들을 한 프로그램으로 합쳐 완성했습니다.

- 발표 날 실제 트랙 큰길 7판을 모두 완주했습니다 (37~44초).
- 사진 시험에서 모서리 판단이 28%에서 81%로 올랐습니다.
- 글로 명령하면 AI가 정해진 동작 11개 중 하나만 고르고, 그 밖의 요청은 거절합니다.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/raspbot-pbl-3team/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>

<br><br>

## Stack

<p align="center">
  <a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=python,fastapi,opencv,raspberrypi,js,react,vite,supabase,html,unity,cs,git,github&perline=13" alt="Python, FastAPI, OpenCV, Raspberry Pi, JavaScript, React, Vite, Supabase, HTML, Unity, C#, Git, GitHub" /></a>
</p>

## 🔧 Recent

- 2026-11 · 대구대 PBL에서 Raspbot 자율주행 시연 (3조 조장)
- 2026-10 · [Upstage Education 블로그](https://edu.upstage.ai/blog/daegu-bootcamp-flowlight)에 FlowLight 소개 글이 실렸습니다

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=120&section=footer" width="100%" alt="" />
