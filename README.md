<div align="center">

# Dmitrii Bogdanov

**Backend / full-stack engineer**

Go · TypeScript · PostgreSQL

<br>

[![Telegram](https://img.shields.io/badge/Telegram-1a1a1a?style=for-the-badge&logo=telegram&logoColor=26A5E4)](https://t.me/NobodYYY_devvv)
[![platon.school](https://img.shields.io/badge/platon.school-1a1a1a?style=for-the-badge&logo=googlechrome&logoColor=4285F4)](https://platon.school)

</div>

<br>

I build backends end to end: data model, API, migrations, tests, deployment.
Two years of commercial work, currently on a SaaS platform for private tutors.

<br>

<div align="center">

### Stack

![Go](https://img.shields.io/badge/Go-1a1a1a?style=flat-square&logo=go&logoColor=00ADD8)
![TypeScript](https://img.shields.io/badge/TypeScript-1a1a1a?style=flat-square&logo=typescript&logoColor=3178C6)
![JavaScript](https://img.shields.io/badge/JavaScript-1a1a1a?style=flat-square&logo=javascript&logoColor=F7DF1E)
![SQL](https://img.shields.io/badge/SQL-1a1a1a?style=flat-square&logo=postgresql&logoColor=4169E1)

![Fiber](https://img.shields.io/badge/Fiber-1a1a1a?style=flat-square&logo=go&logoColor=00ADD8)
![Node.js](https://img.shields.io/badge/Node.js-1a1a1a?style=flat-square&logo=nodedotjs&logoColor=5FA04E)
![Express](https://img.shields.io/badge/Express-1a1a1a?style=flat-square&logo=express&logoColor=ffffff)
![gRPC](https://img.shields.io/badge/gRPC-1a1a1a?style=flat-square&logo=grpc&logoColor=2DA6B0)
![WebSocket](https://img.shields.io/badge/WebSocket-1a1a1a?style=flat-square&logo=socketdotio&logoColor=ffffff)

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1a1a?style=flat-square&logo=postgresql&logoColor=4169E1)
![Redis](https://img.shields.io/badge/Redis-1a1a1a?style=flat-square&logo=redis&logoColor=FF4438)
![MongoDB](https://img.shields.io/badge/MongoDB-1a1a1a?style=flat-square&logo=mongodb&logoColor=47A248)
![MinIO](https://img.shields.io/badge/S3%20%2F%20MinIO-1a1a1a?style=flat-square&logo=minio&logoColor=C72E49)

![Next.js](https://img.shields.io/badge/Next.js-1a1a1a?style=flat-square&logo=nextdotjs&logoColor=ffffff)
![React](https://img.shields.io/badge/React-1a1a1a?style=flat-square&logo=react&logoColor=61DAFB)
![Redux](https://img.shields.io/badge/Redux%20Toolkit-1a1a1a?style=flat-square&logo=redux&logoColor=764ABC)

![Docker](https://img.shields.io/badge/Docker-1a1a1a?style=flat-square&logo=docker&logoColor=2496ED)
![nginx](https://img.shields.io/badge/nginx-1a1a1a?style=flat-square&logo=nginx&logoColor=009639)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-1a1a1a?style=flat-square&logo=githubactions&logoColor=2088FF)
![Linux](https://img.shields.io/badge/Linux-1a1a1a?style=flat-square&logo=linux&logoColor=FCC624)

</div>

<br>

---

## Currently building

### PLATON &nbsp;·&nbsp; SaaS platform for private tutors and online schools

<sub>Go · Fiber · PostgreSQL · Redis · WebSocket · LiveKit · Next.js &nbsp;—&nbsp; private repository</sub>

<table>
<tr>
<td align="center"><b>37</b><br><sub>domain packages</sub></td>
<td align="center"><b>~395</b><br><sub>REST endpoints</sub></td>
<td align="center"><b>107</b><br><sub>DB tables</sub></td>
<td align="center"><b>58</b><br><sub>migrations</sub></td>
<td align="center"><b>243</b><br><sub>test files</sub></td>
<td align="center"><b>84</b><br><sub>recorded ADRs</sub></td>
</tr>
</table>

- Go backend monolith, layered `handlers / service / repository`, **no ORM** — all SQL by hand over pgxpool
- PostgreSQL schema of 107 tables via goose migrations, every one with a reversible rollback and backfill
- **Billing:** subscriptions, four course payment models, refunds, double-entry wallet, payouts, fiscal receipts
- **Collaborative whiteboard** built from scratch on the Canvas API with a custom WebSocket protocol
- **Video lessons** on self-hosted LiveKit + coturn, with recording via egress
- Next.js frontend — 78 cabinet screens, 37 admin screens with a role/permission matrix and audit log
- 7 CI pipelines: image builds, deployment, repository mirroring via `git subtree split`

<br>

### Shispar &nbsp;·&nbsp; B2C/B2B e-commerce platform

<sub>Node.js · Express · MongoDB · React · Docker &nbsp;—&nbsp; sole developer, private repository</sub>

- **YooKassa payments:** cards, instant transfers, cash on delivery, invoice payment for companies
- Order lifecycle automation: stock reservation, statuses, auto-cancellation, tracking numbers
- **Telegram and MAX bots** as separate services — invoices and order status without visiting the site
- Permission model scoped to sections and actions, replacing a single shared admin account
- CI/CD from scratch: Docker → GHCR → deploy over SSH on push to `main`

<br>

---

## A problem I enjoyed solving

> Per-plan student limits and storage quotas were both breachable by parallel requests.
>
> The fix was PostgreSQL advisory locks, with one rule that is easy to get wrong: **the check has
> to be a separate statement issued after the lock.** Combine locking and checking into one query
> and you read the snapshot taken before you started waiting — which is exactly the state the lock
> existed to protect you from.
>
> Locks are also taken in **ascending key order**, because one person can be a tutor on their own
> course and a student on someone else's — so "tutor first, then students" is not an order at all.

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
<sub>Open to remote work only</sub>
</div>
