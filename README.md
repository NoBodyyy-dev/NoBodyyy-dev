<div align="center">

# Dmitrii Bogdanov

**Full-stack developer**

React / Next.js · Go · Python · ML

<br>

[![Telegram](https://img.shields.io/badge/Telegram-1a1a1a?style=for-the-badge&logo=telegram&logoColor=26A5E4)](https://t.me/NobodYYY_devvv)
[![platon.school](https://img.shields.io/badge/platon.school-1a1a1a?style=for-the-badge&logo=googlechrome&logoColor=4285F4)](https://platon.school)

</div>

<br>

I build products end to end: interface, API, database, ML services and the infrastructure they run on.
Two years of commercial work, currently on a SaaS platform for private tutors.

<br>

<div align="center">

### Stack

![TypeScript](https://img.shields.io/badge/TypeScript-1a1a1a?style=flat-square&logo=typescript&logoColor=3178C6)
![Go](https://img.shields.io/badge/Go-1a1a1a?style=flat-square&logo=go&logoColor=00ADD8)
![Python](https://img.shields.io/badge/Python-1a1a1a?style=flat-square&logo=python&logoColor=3776AB)
![SQL](https://img.shields.io/badge/SQL-1a1a1a?style=flat-square&logo=postgresql&logoColor=4169E1)

![Next.js](https://img.shields.io/badge/Next.js-1a1a1a?style=flat-square&logo=nextdotjs&logoColor=ffffff)
![React](https://img.shields.io/badge/React-1a1a1a?style=flat-square&logo=react&logoColor=61DAFB)
![Redux](https://img.shields.io/badge/Redux%20Toolkit-1a1a1a?style=flat-square&logo=redux&logoColor=764ABC)
![Tailwind](https://img.shields.io/badge/Tailwind-1a1a1a?style=flat-square&logo=tailwindcss&logoColor=06B6D4)

![Fiber](https://img.shields.io/badge/Fiber-1a1a1a?style=flat-square&logo=go&logoColor=00ADD8)
![FastAPI](https://img.shields.io/badge/FastAPI-1a1a1a?style=flat-square&logo=fastapi&logoColor=009688)
![Node.js](https://img.shields.io/badge/Node.js-1a1a1a?style=flat-square&logo=nodedotjs&logoColor=5FA04E)
![gRPC](https://img.shields.io/badge/gRPC-1a1a1a?style=flat-square&logo=grpc&logoColor=2DA6B0)
![WebSocket](https://img.shields.io/badge/WebSocket-1a1a1a?style=flat-square&logo=socketdotio&logoColor=ffffff)

![PyTorch](https://img.shields.io/badge/PyTorch-1a1a1a?style=flat-square&logo=pytorch&logoColor=EE4C2C)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1a1a1a?style=flat-square&logo=scikitlearn&logoColor=F7931E)
![pandas](https://img.shields.io/badge/pandas-1a1a1a?style=flat-square&logo=pandas&logoColor=ffffff)
![LLM](https://img.shields.io/badge/LLM%20%2F%20RAG-1a1a1a?style=flat-square&logo=openai&logoColor=ffffff)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1a1a?style=flat-square&logo=postgresql&logoColor=4169E1)
![Redis](https://img.shields.io/badge/Redis-1a1a1a?style=flat-square&logo=redis&logoColor=FF4438)
![MongoDB](https://img.shields.io/badge/MongoDB-1a1a1a?style=flat-square&logo=mongodb&logoColor=47A248)
![MinIO](https://img.shields.io/badge/S3%20%2F%20MinIO-1a1a1a?style=flat-square&logo=minio&logoColor=C72E49)

![Docker](https://img.shields.io/badge/Docker-1a1a1a?style=flat-square&logo=docker&logoColor=2496ED)
![Kubernetes](https://img.shields.io/badge/Kubernetes-1a1a1a?style=flat-square&logo=kubernetes&logoColor=326CE5)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-1a1a1a?style=flat-square&logo=githubactions&logoColor=2088FF)
![nginx](https://img.shields.io/badge/nginx-1a1a1a?style=flat-square&logo=nginx&logoColor=009639)
![Prometheus](https://img.shields.io/badge/Prometheus-1a1a1a?style=flat-square&logo=prometheus&logoColor=E6522C)
![Linux](https://img.shields.io/badge/Linux-1a1a1a?style=flat-square&logo=linux&logoColor=FCC624)

</div>

<br>

---

## Currently building

### PLATON &nbsp;·&nbsp; SaaS platform for private tutors and online schools

<sub>Go · Fiber · PostgreSQL · Redis · WebSocket · LiveKit · Next.js &nbsp;—&nbsp; private repository</sub>

- Go backend with handlers, services and repositories, plain SQL over pgxpool without an ORM
- PostgreSQL schema managed by goose migrations, each with a rollback
- Billing: subscriptions, several course payment models, refunds, wallet, payouts, fiscal receipts
- Collaborative whiteboard built from scratch on the Canvas API with its own WebSocket protocol
- Video lessons on self-hosted LiveKit and coturn, with recording
- Next.js frontend: tutor and student cabinets, admin panel with roles, permissions and audit log
- CI pipelines for image builds, deployment and repository mirroring

<br>

### Shispar &nbsp;·&nbsp; B2C/B2B e-commerce platform

<sub>Node.js · Express · MongoDB · React · Docker &nbsp;—&nbsp; sole developer, private repository</sub>

- YooKassa payments: cards, instant transfers, cash on delivery, invoices for companies
- Order lifecycle automation: stock reservation, statuses, auto-cancellation, tracking numbers
- Telegram and MAX bots as separate services for invoices and order status
- Permissions scoped to sections and actions instead of one shared admin account
- CI/CD from scratch: Docker, GHCR, deploy over SSH on push to `main`

<br>

---

## Public projects

| Project | What it is | Stack |
| --- | --- | --- |
| [na-storone-zakona](https://github.com/NoBodyyy-dev/na-storone-zakona) | Law firm website and booking bots for Telegram and MAX | TypeScript · PostgreSQL · Docker · nginx |
| [mango](https://github.com/NoBodyyy-dev/mango) | Web studio website with scroll animations | HTML · CSS · GSAP · GitHub Pages |

<br>

---

## A problem I enjoyed solving

> Per-plan student limits and storage quotas were both breachable by parallel requests.
>
> The fix was PostgreSQL advisory locks, with one rule that is easy to get wrong: **the check has
> to be a separate statement issued after the lock.** Combine locking and checking into one query
> and you read the snapshot taken before you started waiting, which is exactly the state the lock
> existed to protect you from.
>
> Locks are also taken in **ascending key order**, because one person can be a tutor on their own
> course and a student on someone else's, so "tutor first, then students" is not an order at all.

<br>

---

<details>
<summary><b>Education</b></summary>

<br>

**NUST MISIS**, Moscow — BSc, Computer Science and Engineering · expected 2028

**Higher School of Programming** — vocational diploma, Software Development · 2024

</details>

<br>

<div align="center">
<sub>Open to remote work</sub>
</div>
