<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=220&section=header&text=Jihoon%20Lee&fontSize=64&fontColor=ffffff&fontAlignY=38&desc=AI%20%C2%B7%20Backend%20Developer&descSize=22&descAlignY=60&animation=fadeIn" width="100%" alt="Jihoon Lee" />

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3200&pause=900&color=60A5FA&center=true&vCenter=true&width=640&lines=LLM+Agents+that+get+verified+before+they+ship;FastAPI+%C2%B7+SSE+%C2%B7+Structured+Outputs+%C2%B7+Guardrail;Built+an+Upstage+Solar+Pro+4+demo" alt="LLM Agents that get verified before they ship" /></a>
</p>

<p align="center">
  <b>I build systems that never use an AI's answer as-is: only output that passes a check gets applied.</b><br>
  LLM Agent · FastAPI · SSE · OpenCV · YOLO
</p>

<p align="center">
  <a href="README.md"><img src="https://img.shields.io/badge/%ED%95%9C%EA%B5%AD%EC%96%B4-README-0f172a?style=flat-square" alt="Korean README" /></a>
  <a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/FlowLight-Live%20Demo-f97316?style=flat-square&logo=googlechrome&logoColor=white" alt="FlowLight Live Demo" /></a>
  <a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/AlbaGuard-Live%20App-1d4ed8?style=flat-square&logo=googlechrome&logoColor=white" alt="AlbaGuard Live App" /></a>
  <a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-Feature-7c3aed?style=flat-square" alt="Upstage Blog feature" /></a>
  <img src="https://img.shields.io/badge/Daegu%20University-Software-0f172a?style=flat-square" alt="Daegu University" />
</p>

<br>

## 📌 At a Glance

| Project | What | My role | Try it |
|---|---|---|---|
| 🚦 [FlowLight](https://github.com/jihooni217/FlowLight-AI-Traffic-Signal) | Three LLM Agents plan intersection traffic signals | Repo owner | [Live Demo](https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/) |
| 🎁 [KeepCon](https://github.com/Jiwonang/KeepCon) | Collect gift vouchers and share them with family and friends | Team member | [Repository](https://github.com/Jiwonang/KeepCon) |
| 🛡️ [AlbaGuard](https://github.com/jihooni217/albaguard) | Mobile web app that finds unpaid part-time wages from your own records | Repo owner | [Open app](https://jihooni217.github.io/albaguard/) |
| 🚗 [Raspbot](https://github.com/jihooni217/raspbot-pbl-3team) | Small self-driving car that laps a track with one camera | Team 3 leader (PBL) | [Code · video](https://github.com/jihooni217/raspbot-pbl-3team) |

<br>

## 🚦 FlowLight

A Multi-Agent demo that analyzes, plans and evaluates intersection signals with **Upstage Solar Pro 4**.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://raw.githubusercontent.com/jihooni217/FlowLight-AI-Traffic-Signal/main/docs/flowlight_live_demo.gif" width="640" alt="FlowLight demo: the Agents show the signal plan step by step" /></a>

**My role**
- Defined the prompts and JSON Schema for the three Agents.
- Built the FastAPI server, SSE streaming and the Guardrail.
- Designed and ran the 10-seed comparison, and presented the project.

**How**
- Agent output is locked to a **JSON Schema**.
- Only plans that pass a rule-based **Guardrail** reach the signal.
- **FastAPI + SSE** streams each reasoning step to the browser.
- Real Seoul traffic counts (one day around Sungnyemun) ship as a second profile.
- Runs in the browser with no install, by replaying recorded real responses.

**Results**
- Intersection with no pedestrians, average of 10 seeds: +11% cars through, −16% stopped cars.
- The baseline is a fixed schedule that gives a walk signal every cycle, even with nobody waiting.
- Most of the gain is that unused walk time handed back to cars. The repo states the evidence and the limits.
- 286 tests.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/Live%20Demo-f97316?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Demo" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>
<a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-7c3aed?style=for-the-badge" alt="Upstage Blog" /></a>

<br><br>

## 🎁 KeepCon <sub>team project</sub>

A **Flutter** app that gathers gift vouchers scattered across apps in one place, with group sharing for family and friends.

- The original repository is [Jiwonang/KeepCon](https://github.com/Jiwonang/KeepCon). I took part as a team member.
- The team split four pages (Home · Scan/Add · Share · Login/Settings) by owner and built them in parallel.
- Shared models live only in `lib/shared`. A CI SSOT guard blocks redefinitions.
- No direct pushes to `main` or `develop`. Changes merge only through a PR that passes CI.
- Tech: Flutter (Dart) · Riverpod · Firebase (Auth, Firestore)

<a href="https://github.com/Jiwonang/KeepCon"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>

<br><br>

## 🛡️ AlbaGuard

A mobile web app for hourly part-time workers: log your own shifts, then find and request wages you were underpaid.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://raw.githubusercontent.com/jihooni217/albaguard/main/public/og.png" width="640" alt="AlbaGuard: find unpaid wages with your own records" /></a>

- One flow: log shifts → compare with what was actually paid → draft a settlement request.
- Editing or deleting a record keeps the before/after time and the reason.
- Each record gets a **SHA-256** receipt number and a server registration time (**Supabase**).
- Anyone can look up the registration time by receipt number on the verify page.
- Only the receipt number, record number and a random device ID go to the server. Workplace, times and amounts stay on the phone.
- Records, edit history and the pay calculation export as one evidence PDF.
- **React + Vite**, auto-deployed to GitHub Pages with GitHub Actions.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/Open%20App-1d4ed8?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Open App" /></a>
<a href="https://github.com/jihooni217/albaguard"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://jihooni217.github.io/albaguard/verify.html"><img src="https://img.shields.io/badge/Verify%20Page-0f766e?style=for-the-badge" alt="Verify Page" /></a>

<br><br>

## 🚗 Raspbot Self-Driving Car

A small self-driving car that laps a track on its own with a single camera. **Raspberry Pi 5**, Daegu University PBL Team 3.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://raw.githubusercontent.com/jihooni217/raspbot-pbl-3team/main/docs/media/outer_lap_4x.gif" width="640" alt="Raspbot lapping the outer loop of the track (4x speed)" /></a>

**My role** (team leader · led the work)
- Wrote a spec for every feature myself: goal, rule table, numeric success criteria, safety rules.
- Merged the demo code into one program and tuned it on the real track until all 7 runs finished.
- Found causes by putting run logs next to the robot's camera video. The outer-loop logs alone pass 60 runs.

**How**
- OpenCV follows the lane, and the car speeds up or slows down by floor color.
- YOLO stops the car for a person or a STOP sign. It also stops by itself at the START line.
- **Spec-driven AI pair programming**: I write the rules and numeric success criteria, and Codex writes the code.
- Every change is tested on photos and a fake device before the wheels turn.
- Text commands use a Guardrail: the AI may pick only one of 11 fixed actions.

**Results**
- All 7 runs on the real track's outer loop finished (demo day, 37–44 s).
- Lane corner decisions in the photo test: 28% → 81%.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/raspbot-pbl-3team/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>

<br><br>

## 🧭 How I Work

- **Check AI output before applying it**: lock the format, and use only what passes the Guardrail.
- **Test before anything moves**: try fake devices and tests before the real robot or real service.
- **Hand AI a spec**: people write the rules and numeric success criteria, and the AI writes the code.
- **Ship something you can open**: publish demos and apps that run in the browser with no install.

## Stack

<p align="center">
  <a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=python,fastapi,opencv,raspberrypi,js,react,vite,supabase,html,unity,cs,git,github&perline=13" alt="Python, FastAPI, OpenCV, Raspberry Pi, JavaScript, React, Vite, Supabase, HTML, Unity, C#, Git, GitHub" /></a>
</p>

## 🔧 Recent

- 2026-11 · Raspbot self-driving: Daegu University PBL team leader, live demo of a full autonomous lap
- 2026-10 · FlowLight featured on the [Upstage Education blog](https://edu.upstage.ai/blog/daegu-bootcamp-flowlight)
- FlowLight · AlbaGuard: public demo and web app you can use with no install

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=120&section=footer" width="100%" alt="" />
