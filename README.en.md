<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=220&section=header&text=Jihoon%20Lee&fontSize=64&fontColor=ffffff&fontAlignY=38&desc=AI%20%C2%B7%20Backend%20Developer&descSize=22&descAlignY=60&animation=fadeIn" width="100%" alt="Jihoon Lee" />

<p align="center">
  I study AI and backend development in the Software department at Daegu University.<br>
  I mostly build servers with an LLM inside, and demos anyone can open right away.
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

| Project | What | Role | Try it |
|---|---|---|---|
| 🚦 [FlowLight](https://github.com/jihooni217/FlowLight-AI-Traffic-Signal) | Three LLM Agents plan intersection signals | Personal project | [Live Demo](https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/) |
| 🎁 [KeepCon](https://github.com/Jiwonang/KeepCon) | Collect gift vouchers and share them with family and friends | Team member | [Repository](https://github.com/Jiwonang/KeepCon) |
| 🛡️ [AlbaGuard](https://github.com/jihooni217/albaguard) | Mobile web app for finding unpaid part-time wages from your own records | Personal project | [Open app](https://jihooni217.github.io/albaguard/) |
| 🚗 [Raspbot](https://github.com/jihooni217/raspbot-pbl-3team) | Small self-driving car that laps a track with one camera | Team 3 leader (PBL) | [Code · video](https://github.com/jihooni217/raspbot-pbl-3team) |

<br>

## 🚦 FlowLight

A Multi-Agent demo that plans intersection signals with Upstage Solar Pro 4. It started from a simple idea: skip the walk signal when nobody is at the crosswalk, and give more time when a child or a wheelchair user is crossing.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://raw.githubusercontent.com/jihooni217/FlowLight-AI-Traffic-Signal/main/docs/flowlight_live_demo.gif" width="640" alt="FlowLight demo: the Agents show the signal plan step by step" /></a>

Three Agents take turns: one reads the traffic, one plans the signal times, and one reviews the plan. Their output is held to a JSON Schema, and only plans that pass a rule-based Guardrail (minimum green time, cycle total) go into the simulator. FastAPI and SSE stream each step to the screen as it happens.

I did the prompts and Schema, the server and Guardrail, the simulator hookup, the comparison runs, and the presentation.

- At an intersection with no pedestrians, averaged over 10 seeds, 11% more cars got through and 16% fewer were stopped. The baseline is a fixed schedule that gives a walk signal every cycle, even when nobody is there.
- Most of that gain came from handing the empty walk time back to cars. The effect of the LLM re-splitting time between the two directions stayed inside the margin of error.
- It also ships one day of real traffic counts from around Sungnyemun in Seoul, and has 286 tests.
- The public demo runs without a server by replaying real responses recorded earlier.

<a href="https://jihooni217.github.io/FlowLight-AI-Traffic-Signal/"><img src="https://img.shields.io/badge/Live%20Demo-f97316?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Live Demo" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/FlowLight-AI-Traffic-Signal/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>
<a href="https://edu.upstage.ai/blog/daegu-bootcamp-flowlight"><img src="https://img.shields.io/badge/Upstage%20Blog-7c3aed?style=for-the-badge" alt="Upstage Blog" /></a>

<br><br>

## 🎁 KeepCon <sub>team project</sub>

A Flutter app that pulls gift vouchers scattered across different apps into one place, so family or friends can share them as a group. The original repository is [Jiwonang/KeepCon](https://github.com/Jiwonang/KeepCon), and I joined as a team member.

We split four pages (Home, Scan/Add, Share, Login/Settings) by owner and built them at the same time. Models used by more than one page lived only in `lib/shared`, and CI blocked duplicate definitions. Nothing went into `main` or `develop` without a PR that passed CI.

Built with Flutter (Dart), Riverpod, and Firebase (Auth, Firestore).

<a href="https://github.com/Jiwonang/KeepCon"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>

<br><br>

## 🛡️ AlbaGuard

A mobile web app that helps college students on hourly part-time jobs log their own shifts, then find and ask for wages they were underpaid.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://raw.githubusercontent.com/jihooni217/albaguard/main/public/og.png" width="640" alt="AlbaGuard: find unpaid wages with your own records" /></a>

- It compares your records with what was actually paid, finds the gap, and drafts the message to send to your employer.
- If you edit or delete a record, it keeps when and why.
- Each record gets a SHA-256 receipt number, stored in Supabase with a registration time. Anyone can look that time up on the verify page.
- Only the receipt number, record number and a random device ID go to the server. Workplace, times and amounts stay on the phone.
- Records, edit history and the pay calculation export as a single PDF.
- Built with React and Vite, and deployed to GitHub Pages with GitHub Actions.

<a href="https://jihooni217.github.io/albaguard/"><img src="https://img.shields.io/badge/Open%20App-1d4ed8?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Open App" /></a>
<a href="https://github.com/jihooni217/albaguard"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://jihooni217.github.io/albaguard/verify.html"><img src="https://img.shields.io/badge/Verify%20Page-0f766e?style=for-the-badge" alt="Verify Page" /></a>

<br><br>

## 🚗 Raspbot Self-Driving Car

A small self-driving car that laps a track on its own with a single camera. It runs on a Raspberry Pi 5, and I led Team 3 in the Daegu University PBL course.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://raw.githubusercontent.com/jihooni217/raspbot-pbl-3team/main/docs/media/outer_lap_4x.gif" width="640" alt="Raspbot lapping the outer loop of the track (4x speed)" /></a>

It follows the lane with OpenCV and changes speed by floor color. YOLO makes it stop for a person or a STOP sign, and it pulls up on its own when it gets back to the START line.

Codex wrote the code. My side was writing a spec for each feature: goal, rule table, numeric success criteria, and safety rules. Before the wheels turned, every change was tested on photos and a fake device. When a run went wrong, I put the run log next to the camera video to find the cause. The outer-loop logs alone pass 60 runs. For the demo, I merged these features into one program.

- On demo day, all 7 runs on the real track's outer loop finished (37–44 s).
- In the photo test, corner decisions went from 28% to 81%.
- For text commands, the AI may pick only one of 11 fixed actions and turns down anything else.

<a href="https://github.com/jihooni217/raspbot-pbl-3team"><img src="https://img.shields.io/badge/Repository-0f172a?style=for-the-badge&logo=github&logoColor=white" alt="Repository" /></a>
<a href="https://github.com/jihooni217/raspbot-pbl-3team/blob/main/README.en.md"><img src="https://img.shields.io/badge/English%20README-1d4ed8?style=for-the-badge" alt="English README" /></a>

<br><br>

## Stack

<p align="center">
  <a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=python,fastapi,opencv,raspberrypi,js,react,vite,supabase,html,unity,cs,git,github&perline=13" alt="Python, FastAPI, OpenCV, Raspberry Pi, JavaScript, React, Vite, Supabase, HTML, Unity, C#, Git, GitHub" /></a>
</p>

## 🔧 Recent

- 2026-11 · Raspbot self-driving demo at the Daegu University PBL (Team 3 leader)
- 2026-10 · FlowLight was featured on the [Upstage Education blog](https://edu.upstage.ai/blog/daegu-bootcamp-flowlight)

<br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1d4ed8,100:f97316&height=120&section=footer" width="100%" alt="" />
