<h1 align="center">Hi 👋, I'm Muzaffar Xodjayev</h1>
<h3 align="center">Backend Engineer · DevOps · Python / Django Specialist</h3>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3500&pause=800&color=0E75B6&center=true&vCenter=true&width=620&lines=Building+enterprise+approval+workflows;Integrating+AI+services+(Gemini%2C+Anthropic)+into+Django;Bridging+backend+and+DevOps+with+Docker+%26+Nginx;Shipping+CI%2FCD+pipelines+with+auto-rollback+%26+Telegram+alerts;3%2B+years+shipping+production+software" alt="Typing SVG" />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=muzaffar-xodjayev&label=Profile%20views&color=0e75b6&style=flat" />
  <img src="https://img.shields.io/github/followers/muzaffar-xodjayev?label=Followers&style=social" />
</p>

---

## 🚀 About Me

I'm a Python Backend Engineer based in **Namangan, Uzbekistan** with **3+ years** of hands-on experience building production systems. Currently I work as a **DevOps Engineer at IFODA Agro Chemistry**, but my product muscle stays sharp by shipping full backend stacks — Django REST APIs, Telegram bots, WebSocket realtime layers, AI-assisted features, and the Docker/Nginx infrastructure to keep them online.

I care about clean code, **Google-style English docstrings**, and tests that catch the next regression before it ships. When QA pushes back, I take it — and refactor toward the right answer.

- 🔭 Currently scaling **enterprise approval workflows** with Django + Channels + Aiogram 3
- 🤖 Comfortable **integrating AI services** (Gemini Vision, Anthropic) into Django backends — I wire them up, not write the agents
- 🛠️ I bridge **Backend ↔ DevOps** — rare combo that ships products end-to-end
- 🚀 I treat **CI/CD as a product** — multi-stage pipelines, auto-rollback on failure, Telegram alerts to the team
- 💬 Ask me about: **DRF, Aiogram 3, PostgreSQL tuning, Docker networking, WebSocket**
- ⚡ Fun fact: When I'm offline, football and console games own me

---

## 🛠️ Tech Stack

### Core
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/DRF-A30000?style=for-the-badge&logo=django&logoColor=white)
![Django Channels](https://img.shields.io/badge/Channels-092E20?style=for-the-badge&logo=django&logoColor=white)
![Aiogram 3](https://img.shields.io/badge/Aiogram_3-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

### Data & Caching
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

### AI & Automation
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4B8BBE?style=for-the-badge&logo=python&logoColor=white)

### DevOps & Infrastructure
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Let's Encrypt](https://img.shields.io/badge/Let's_Encrypt-003A70?style=for-the-badge&logo=letsencrypt&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)

---

## 🏗️ Architecture & System Design

I think in **workflows, contracts, and clean data models**. Patterns I reach for:

- **Role-based approval chains** — composable `WorkflowPattern` + `ApprovalStep` model with reject/resend routing, multi-manager support, and soft-cancellation
- **Dual-channel notifications** — Django Channels (WebSocket) for in-app + Aiogram 3 for Telegram, both fed from a single service layer
- **AI service integration** — wiring Gemini Vision and Anthropic into Django request flows, handling streaming responses, rate limiting, and error correction
- **Monetary precision** — `Decimal` arithmetic end-to-end, quantize at the boundary (Excel/UI), never `float`
- **Soft-delete + audit trail** — `state` boolean + `ActiveManager` so the default queryset hides deleted rows; `all_objects` for forensics
- **Testable services** — thin DRF views, fat service modules, Google-style English docstrings, comprehensive coverage on critical paths

---

## ⚙️ DevOps & Infrastructure

Backend without deployment is half the job. I run the boxes too — and I treat the deploy pipeline like a product.

### CI/CD I'm proud of

- **Multi-stage GitHub Actions pipelines** — separate `build → test → deploy` stages so a failed test never reaches production
- **Automated rollback on failure** — post-deploy health checks; if a new container fails to pass, the pipeline **reverts to the previous version automatically**. No manual `docker compose down`, no 3 AM panic.
- **Telegram bot notifications** — build / deploy / rollback status pushed to the team channel in real time. Every engineer sees green ✅ or red ❌ without checking the Actions tab.
- **SSH-based zero-downtime deploys** — image built in CI, pulled on the server, hot-swapped behind Nginx

### Infra & ops

- **Docker Compose** stacks behind **host Nginx** + **Let's Encrypt** wildcard SSL on Ubuntu VPS
- Container **health checks**, resource limits (`cpus`, `memory`), automated restarts
- **PostgreSQL tuning** — `pg_hba.conf` for Docker subnets (`172.16.0.0/12`), `scram-sha-256` auth, `listen_addresses` for `docker0`
- **AWS EC2** deployments with secure subnet/firewall rules
- **Debugging-first mindset** — root cause before workaround

---

## 💼 Work Experience

| Role | Company | Duration |
|------|---------|----------|
| 🛠️ **DevOps Engineer** | IFODA Agro Chemistry | _Current_ |
| 🖼️ Image Processor | SiteLabs LLC | 7 months |
| 🎓 Intern | Realsoft LLC | 8 months |
| 💻 Backend Developer | Startup team | 6 months |
| 👨‍🏫 Frontend Assistant Mentor | Nits School | 7 months |

---

## 🌟 Featured Projects

### 🏭 PR_backend — Enterprise Purchase Request System
Production-grade PR approval platform with an **8-stage role-based workflow**, reject / resend logic, multi-manager support per department, Telegram + WebSocket real-time notifications, Excel reports with currency-normalized analytics, and integrated AI-driven market analysis.
- **Stack:** Django 5.2 · DRF · Channels (WebSocket) · Aiogram 3 · Gemini · PostgreSQL · Redis · Docker · Nginx
- **My role:** Sole backend engineer — workflow modeling, service layer, AI integration, deployment

### 🌾 IfodaBackend — AI Plant Disease Detection
Backend API for detecting plant diseases from photos using **Gemini Vision**, with real-time WebSocket chat for AI consultations, smart product recommendations, Telegram bot integration, and Payme / Click payment gateways.
- **Stack:** Django · DRF · Channels (WebSocket) · Aiogram 3 · Gemini Vision · Anthropic · PostgreSQL · Redis · JWT
- **Highlights:** Streaming AI responses, 5 req/min rate limiting, admin panel for error corrections
- **My role:** API design, AI integration pipeline, real-time chat layer

### 🏢 Mexmash Stack — Corporate Platform (Mexmash MChJ)
Corporate platform for Mexmash MChJ. **My work**: backend API + deployment of the entire stack (Next.js site, React admin, Django backend).
- **Backend (contributed):** Django 5.1 · DRF · Channels · SimpleJWT · PostgreSQL · `django-modeltranslation` · drf-spectacular · multilingual content (uz / ru / en) · real-time CRM board via WebSocket
- **Public site (deployed by me):** Next.js 16 · React 19 · TypeScript
- **Admin panel (deployed by me):** React 19 · Vite · TypeScript
- **My role:** Backend architecture & development · Docker / Nginx deployment of all 3 apps · CI/CD pipeline with rollback & Telegram alerts

### 📞 IFODA Call Center CRM
Call-center leaderboard for IFODA — agent metrics, live performance tracking, shift-based stats.
- **Stack:** React 19 · Vite · TypeScript _(frontend by others)_
- **My role:** Production deployment, Nginx config, SSL setup, CI/CD pipeline

### 💎 Gavhar — Jewelry Brand Site
Brand site for Gavhar jewelry — HTML/CSS/JS with campaign video and asset-heavy gallery.
- **Stack:** HTML5 · CSS3 · Vanilla JS _(site delivered by others)_
- **My role:** Production deployment, asset hosting, domain / SSL setup

### 📝 [Oson Test](https://oson-test.uz/)
Online quiz platform serving teachers and students with rich question types and result tracking.
- **Stack:** Django · DRF · PostgreSQL · **My role:** Backend API for quiz creation and grading

### 🤖 [Artel Telegram Bot](https://t.me/ArtelNamanganBot)
Product catalog and management bot for Artel Namangan LLC.
- **Stack:** Aiogram · PostgreSQL · **My role:** Bot architecture, product flows

### 🩺 [TeleCure Bot](https://t.me/TeleCure_bot)
Telegram bot connecting patients with doctors abroad — dual-side app for patients and doctors.
- **Stack:** Aiogram · External API · **My role:** Bot logic, dual-side flow design

### 🚚 [Tezkor Pochta](https://tezkorpochta.pythonanywhere.com/)
Local delivery service platform for moving products between regions.
- **Stack:** Django · PythonAnywhere · **My role:** Full-stack delivery

### ⛑️ [DoctorM](https://doctorm.pythonanywhere.com/)
Hospital call-center website with first-aid lookup and contact routing.
- **Stack:** Django · PythonAnywhere · **My role:** Full-stack delivery

---

## 🎓 Education

🎓 **Bachelor's degree** — Namangan State Technical University

---

## 📈 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=muzaffar-xodjayev&rank_icon=github&include_all_commits=true&card_width=500&hide_border=true&theme=tokyonight&show=reviews,discussions_started,discussions_answered" />
  <br>
  <img src="https://streak-stats.demolab.com?user=muzaffar-xodjayev&theme=tokyonight&hide_border=true&card_width=500" />
  <br>
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=muzaffar-xodjayev&show_icons=true&locale=en&layout=compact&theme=tokyonight&hide_border=true&card_width=500" />
</p>

---

## 📫 Let's Connect

Got a tough backend problem, a stuck deployment, or an idea worth shipping? I'd love to hear it.

<p align="left">
  <a href="mailto:khodjayevmuzaffar@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://t.me/xodjayev_muzaffar"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/muzaffar-xodjayev/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
</p>

---

<p align="center"><i>"Code is read more often than it is written." — Guido van Rossum</i></p>

<p align="center">⭐ Thanks for stopping by — let's build something great together.</p>
