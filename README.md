<h1 align="center">Nitiphum Hongson</h1>

<p align="center">
  <b>Software Engineering student · Mae Fah Luang University, Thailand</b><br>
  I build backends, APIs, and the tests that keep them honest.
</p>

<p align="center">
  <a href="mailto:aruma.osogi@gmail.com">
    <img src="https://img.shields.io/badge/Email-aruma.osogi%40gmail.com-64ffda?style=flat-square&logo=gmail&logoColor=white&labelColor=0a192f" alt="Email">
  </a>
  <img src="https://img.shields.io/badge/Based%20in-Chiang%20Rai,%20Thailand-8892b0?style=flat-square&labelColor=0a192f" alt="Location">
  <img src="https://img.shields.io/badge/Open%20to-Part--time%20%26%20Freelance-64ffda?style=flat-square&labelColor=0a192f" alt="Open to work">
</p>

---

### About

Third-year Software Engineering student. Most of what I know came from building things that had to
actually run, not from lectures.

My main project is a **real-time collaborative editing app** — several people edit the same document
at once and see each other's cursors. I built all of it: the NestJS API, the PostgreSQL schema,
authentication, the React front end, Docker, CI, and the tests. It taught me that the interesting
part of software isn't the happy path — it's what happens when two people type in the same paragraph,
when a token expires mid-request, or when someone sends a field the API never expected.

So that's what I pay attention to: **validate the input, name every failure, and test it before
calling it done.**

---

### Tech I work with

**Backend**
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Hono](https://img.shields.io/badge/Hono-E36002?style=flat-square&logo=hono&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**Database**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Mobile**
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)

**DevOps & testing**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)

**Cloud**
![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat-square&logo=cloudflareworkers&logoColor=white)
![Google Cloud](https://img.shields.io/badge/Google_Cloud_Vision-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

---

### Projects

#### 🗂️ [Task Board](https://github.com/arumaosogi-sudo/Project_task_borad_appvs01) — real-time collaborative editing
Solo project, built end to end. Several people edit the same document at once and see each other's
cursors, powered by **Yjs CRDTs over WebSocket**. Bilingual Thai/English, exports to Word.

- JWT access tokens with a rotating refresh token in an httpOnly cookie, plus Google OAuth
- Owner / Editor / Viewer roles enforced **server-side on every action** — not by hiding buttons
- Turborepo monorepo · 15+ Prisma tables · Docker for dev/test/prod · CI on GitHub Actions
- Tested at three levels: unit, integration, and end-to-end with Playwright

`NestJS` `Prisma` `PostgreSQL` `React` `TypeScript` `Yjs` `Docker` `Playwright`

#### 📊 [Koalytics](https://github.com/arumaosogi-sudo/koalytics-frontend) — emotion-driven UX evaluation
Team of 6 (Thai and international teammates) — **my role: front-end**. A platform that reads a
participant's facial emotion through their webcam during a usability test and reports it as charts.

- 13 pages sharing one design system and navigation shell
- Analytics dashboard built with Highcharts — emotion as gauges and time-based charts
- A five-step test-session flow, from setup through to results

`HTML` `Tailwind CSS` `JavaScript` `Highcharts`

#### 💸 [Expense Tracker API](https://github.com/arumaosogi-sudo/worky3-api) — serverless REST API
Solo project on Cloudflare's edge.

- Six REST endpoints with every business rule enforced **twice** — at the API and again in the database
- Machine-readable error codes for each failure path, so callers never have to parse a message
- 21 test scenarios passing in local and production

`TypeScript` `Hono` `Cloudflare Workers` `Cloudflare D1`

#### 🛒 [SAGA](https://github.com/nitiphum01/SAGA-test) — student marketplace app
Solo Flutter project. Ten core screens — listings, chat, profile, settings — organised feature-first,
with the service layer kept separate from the UI so it can move to a real API without touching a screen.

`Flutter` `Dart` `Provider` `go_router`

---

### Currently learning

Kubernetes basics · deeper automated test coverage · system design at scale

### How I use AI tooling

I design first, use Claude Code / ChatGPT / Gemini to draft and review, then read and test everything
myself before it ships. If I can't explain a piece of code, it doesn't go in.

---

<p align="center">
  <b>Open to part-time and freelance work while I finish my degree.</b><br>
  📧 <a href="mailto:aruma.osogi@gmail.com">aruma.osogi@gmail.com</a><br>
  📄 <a href="https://github.com/arumaosogi-sudo/portfolio/raw/main/Nitiphum-Hongson-CV-EN.pdf">Download my CV (PDF)</a>
</p>
