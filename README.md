<h1 align="center">Nitiphum Hongson</h1>

<p align="center">
  <b>Software Engineering student · Mae Fah Luang University, Thailand</b><br>
  I build backends, APIs, and the tests that keep them honest.
</p>

<p align="center">
  <a href="https://arumaosogi-sudo.github.io/portfolio/">
    <img src="https://img.shields.io/badge/Portfolio-arumaosogi--sudo.github.io-c9a961?style=flat-square&logo=googlechrome&logoColor=white&labelColor=0a192f" alt="Portfolio">
  </a>
  <a href="mailto:aruma.osogi@gmail.com">
    <img src="https://img.shields.io/badge/Email-aruma.osogi%40gmail.com-64ffda?style=flat-square&logo=gmail&logoColor=white&labelColor=0a192f" alt="Email">
  </a>
  <a href="tel:+66661097439">
    <img src="https://img.shields.io/badge/Phone-066--109--7439-8892b0?style=flat-square&logo=phone&logoColor=white&labelColor=0a192f" alt="Phone">
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

#### 🗂️ [Task Board](https://github.com/arumaosogi-sudo/task-board) — real-time collaborative editing
**[Live demo](https://taskboard-aruma-web.onrender.com)** · sign in with `demo@task-board.app` / `demo-task-board-2026`
Solo project, built end to end. Several people edit the same document at once and see each other's
cursors, powered by **Yjs CRDTs over WebSocket**. Bilingual Thai/English, exports to Word.

- A **65-endpoint REST API across 13 NestJS modules**, over 15 Prisma models and 10 migrations
- JWT access tokens with a rotating refresh token in an httpOnly cookie, plus Google OAuth
- Owner / Editor / Viewer roles enforced **server-side on every action** — not by hiding buttons
- **386 test cases** behind CI that also runs integration tests against a real PostgreSQL instance
- Deployed from the project's own Dockerfile; migrations apply on boot from the image entrypoint

`NestJS` `Prisma` `PostgreSQL` `React` `TypeScript` `Yjs` `Docker` `Playwright`

> The free instance sleeps when idle, so the first request after a quiet spell takes about half a minute.

#### 🏦 [Classroom Savings Bank](https://github.com/arumaosogi-sudo/classroom-savings-bank) — web + Android, LINE integration
**[Live demo](https://kid-savings-bank.vercel.app)** · solo project
Thai primary schools run a classroom savings bank out of a paper passbook. This replaces the book and
sends each parent a weekly balance card inside **LINE** — the app their family already has, so there is
nothing to install.

- Each teacher connects their own LINE Official Account: the app validates the token, registers the
  webhook automatically, and can repair a misrouted one from the settings page
- Channel keys encrypted at rest with **AES-256-GCM**; every webhook verified by HMAC signature
- Built for audit — deposits pass a confirm step showing the balance before and after, and reversals
  are recorded as visible entries instead of deletions
- 11 PostgreSQL tables over 6 migrations, Excel export, and an Android build of the same app

`Next.js 16` `React 19` `TypeScript` `PostgreSQL` `Drizzle ORM` `LINE Messaging API` `PWA`

#### 💪 [Digital Muscle](https://github.com/arumaosogi-sudo/digital-muscle) — learning platform for a university course
**[Live demo](https://digital-muscle.medicsync.workers.dev)** · team of 2 — **my role: the whole platform**
Built from a lecturer's muscle-physiology textbook. Students join a section by scanning its QR code;
instructors build the exams and read the results. I built authentication, the API, the database, the
instructor dashboard and the 3D module; my teammate built the games.

- A Hono REST API of about **54 endpoints across 12 route modules** on Cloudflare Workers, over 9 D1 migrations
- Google sign-in restricted to the university domain for students; a hashed password login for
  instructors that locks out after 5 failed attempts in 15 minutes
- Instructor dashboard with QR section management, a Google-Forms-style exam builder and Excel export
- A 3D explorer built with three.js — meshopt-compressed models, step-through animations, clickable parts

`Cloudflare Workers` `Hono` `Cloudflare D1` `React` `TypeScript` `three.js` `Vitest`

#### 🛒 [SAGA](https://github.com/nitiphum01/saga-marketplace) — student marketplace with in-app chat
Solo Flutter project. **12 screens across 5 feature modules** (~7,400 lines of Dart), organised
feature-first with the service layer kept separate from the UI.

- Full Firebase stack — Auth with Google Sign-In, Firestore, Storage and Cloud Messaging
- A **TypeScript Cloud Function** fires on a new chat document and multicasts a push notification to
  the recipient's devices, so delivery doesn't depend on the app being open
- Bilingual Thai / English from the start, routed with `go_router`, state through `Provider`

`Flutter` `Dart` `Firebase` `Cloud Functions` `Provider` `go_router`

---

### Currently learning

Kubernetes basics · deeper automated test coverage · system design at scale

### How I use AI tooling

I design first, use Claude Code / ChatGPT / Gemini to draft and review, then read and test everything
myself before it ships. If I can't explain a piece of code, it doesn't go in.

---

<p align="center">
  <b>Open to part-time and freelance work while I finish my degree.</b><br>
  🌐 <a href="https://arumaosogi-sudo.github.io/portfolio/">arumaosogi-sudo.github.io/portfolio</a><br>
  📧 <a href="mailto:aruma.osogi@gmail.com">aruma.osogi@gmail.com</a> &nbsp;·&nbsp; 📱 <a href="tel:+66661097439">066-109-7439</a><br>
  📄 <a href="https://github.com/arumaosogi-sudo/portfolio/raw/main/Nitiphum-Hongson-CV-EN.pdf">Download my CV (PDF)</a>
</p>
