<!-- ═══════════════════════════════════════════════════════════════════ -->
<!--                          HEADER                                   -->
<!-- ═══════════════════════════════════════════════════════════════════ -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:08090d,40:0d1220,100:0f1a2e&height=280&section=header&text=Alleluia%20Cervi&fontSize=54&fontColor=eceef4&animation=fadeIn&fontAlignY=38&desc=Software%20Engineer%20%E2%80%A2%20AI%20Systems%20%E2%80%A2%20Infrastructure%20%E2%80%A2%20DevOps&descSize=15&descAlignY=58&descColor=4f9eff" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=3200&pause=900&color=4F9EFF&center=true&vCenter=true&width=720&lines=Architect+of+systems+that+scale+to+1M%2B+users.;AI-powered+forex+intelligence+%E2%80%94+Forex+Future.;Arcjet+security+%7C+Kubernetes+%7C+Cloud-native.;Private+work.+Production+impact.;Quality+of+commits+%3E+quantity+of+commits." />
</p>

<br/>

<p align="center">
  <img src="https://img.shields.io/badge/Focus-AI%20%26%20Systems%20Engineering-4f9eff?style=flat-square&labelColor=0f172a" />
  &nbsp;
  <img src="https://img.shields.io/badge/Based%20in-Kigali%2C%20Rwanda-38d9a9?style=flat-square&labelColor=0f172a" />
  &nbsp;
  <img src="https://img.shields.io/badge/Security-Arcjet%20Protected-f87171?style=flat-square&labelColor=0f172a&logo=shield" />
  &nbsp;
  <img src="https://img.shields.io/badge/Status-Open%20to%20Collaboration-a78bfa?style=flat-square&labelColor=0f172a" />
</p>

---

## `$ whoami`

```
Name    : Alleluia Cervi
Role    : Software Engineer · AI Systems Architect · DevOps Engineer
Focus   : Systems that don't freeze, don't break, and don't stop at scale
Motto   : Low noise. High signal. Permanent results.
```

> Most of my work lives in **private repositories**, production systems, and infrastructure
> that can't be measured in commit counts.
> **I don't optimize for GitHub metrics — I optimize for impact.**

---

## ⚙️ Expertise

<table>
<tr>
<td width="33%" valign="top">

### 🤖 AI & LLM Systems
- LLM application architecture
- Prompt engineering & RAG pipelines
- Real-time AI signal engines
- Intelligent automation workflows
- Multi-model orchestration

</td>
<td width="33%" valign="top">

### 💻 Software Engineering
- Full-stack system design
- High-performance backend services
- API design & microservices
- Database architecture & optimization
- Real-time data pipelines

</td>
<td width="34%" valign="top">

### ☁️ DevOps & Infrastructure
- CI/CD pipeline engineering
- Docker · Kubernetes orchestration
- Cloud-native deployment strategies
- **Arcjet** rate-limiting & edge protection
- Reliability & uptime engineering

</td>
</tr>
</table>

---

## 🛠️ Tech Stack

**Languages**
<p>
  <img src="https://skillicons.dev/icons?i=ts,python,js,java,cpp&theme=dark" />
</p>

**Frontend & Backend**
<p>
  <img src="https://skillicons.dev/icons?i=react,nextjs,nodejs,express,fastapi,postgres,mongodb,redis,firebase&theme=dark" />
</p>

**Infrastructure & DevOps**
<p>
  <img src="https://skillicons.dev/icons?i=docker,kubernetes,aws,githubactions,linux,nginx&theme=dark" />
</p>

`🛡️ Arcjet` &nbsp; `📊 Prometheus` &nbsp; `🔭 OpenTelemetry` &nbsp; `🔐 Vault` &nbsp; `⚡ Redis`

---

## 🚀 Selected Work

### 📈 Forex Future — Market Beats *(AI-Powered · Production)*

> An AI-powered forex intelligence platform delivering real-time market signals,
> predictive analytics, and automated trading insights.
> **Built to serve 1,000,000+ concurrent users without degradation.**

<table>
<tr>
<td width="50%" valign="top">

**🤖 AI Engine**
- Real-time LLM signal analysis on live forex data
- Predictive price movement models
- Sub-100ms AI inference pipeline
- Intelligent alert & notification engine

</td>
<td width="50%" valign="top">

**🏗️ Architecture**
- Event-driven microservices at scale
- Distributed caching & data sharding
- Arcjet-protected API layer
- Designed for 1M+ concurrent sessions

</td>
</tr>
</table>

---

### 🔒 Private & Enterprise Work

```diff
+ Most of my portfolio lives under NDA or in private infrastructure.
+ Commit counts do not reflect production systems.

  → Enterprise integrations across Rwanda and East Africa
  → Long-cycle infrastructure (months of design before a single commit)
  → High-stakes builds for organizations that can't afford downtime
  → Internal tooling deployed to production, not to GitHub

# Engineers who measure themselves by commit frequency
# are optimizing for the wrong variable.
```

---

## 💡 How I Think — Engineering Wonder

> *I don't just build features. I ask hard questions before writing a single line.*

---

**🤔 Wonder: what happens when 1,000,000 users hit the system at once?**

I don't wait to find out. I model it first — load test at **2× expected peak**, introduce queue-based ingestion with backpressure, distribute state across Redis clusters, and horizontally scale stateless services behind a load balancer. The system answers the same whether there are 10 users or 10 million.

---

**🤔 Wonder: what if a database node goes down mid-transaction?**

I design for failure as a default state. **Write-ahead logging, replica failover, and idempotent operations** mean a node loss is a non-event. Transactions either complete or cleanly roll back — users never see corrupted state.

---

**🤔 Wonder: what if the AI inference layer becomes the bottleneck?**

Pre-empt it with **async inference queues, result caching on repeated patterns, and model warm pools**. Heavy computation never blocks the user-facing request cycle. Users get instant UI response; AI results arrive via WebSocket when ready.

---

**🤔 Wonder: what if an attacker floods the API with 50,000 requests per second?**

**Arcjet handles it at the edge** before it touches application code — rate limiting, bot detection, and IP reputation scoring run in microseconds. Legitimate users feel nothing; malicious traffic is silently dropped.

---

**🤔 Wonder: what if the market spikes and every user opens the app simultaneously?**

Event-driven architecture with **message queues absorbs burst traffic** like a buffer. Consumers scale out automatically via Kubernetes HPA. The spike becomes a queue, the queue drains — no freezes, no 503s, no calls at 3am.

---

**🤔 Wonder: what if a memory leak develops in a long-running service?**

**Observability is built in from day one** — Prometheus metrics, structured logging, and health-check probes. Kubernetes restarts degraded containers automatically. I find the root cause in the dashboard before any user notices.

---

## 🛡️ Security & Infrastructure Defence

<table>
<tr>
<td width="50%" valign="top">

### 🔐 Application Security
- 🔑 JWT & OAuth2 authentication flows
- 🔒 End-to-end data encryption
- 👤 RBAC access control layers
- 🧹 Input validation & sanitization
- 🕵️ Secrets management (Vault)

</td>
<td width="50%" valign="top">

### 🚨 Arcjet — Edge Protection
- 📊 Adaptive rate limiting per route
- 🤖 Bot detection & fingerprinting
- 🌍 IP reputation & geo-blocking
- 🔥 DDoS mitigation at the edge
- ⚡ SDK-native — zero infra changes

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 👁️ Monitoring & Observability
- 📈 Prometheus metrics collection
- 📋 Structured logging pipelines
- 🔔 Real-time alerting & on-call
- 🔭 Distributed tracing (OpenTelemetry)
- 📊 SLA dashboards & uptime SLOs

</td>
<td width="50%" valign="top">

### 🔄 CI/CD & Infrastructure
- 🔀 GitOps deployment workflows
- 📦 Immutable container builds
- ✅ Automated security scanning
- 🔵 Blue/green zero-downtime deploys
- ☁️ Infrastructure as Code (IaC)

</td>
</tr>
</table>

---

## 📊 Engineering Signals

<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=alleluiacervi-tech&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=4f9eff&icon_color=38d9a9&text_color=8b96aa&include_all_commits=true&rank_icon=github" />
  &nbsp;
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=alleluiacervi-tech&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=4f9eff&text_color=8b96aa" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=alleluiacervi-tech&theme=github-dark-blue&hide_border=true&background=0d1117&ring=4f9eff&fire=38d9a9&currStreakLabel=8b96aa" />
</p>

> ⚠️ *Low commit count = private infrastructure, enterprise NDA work, and long-cycle system design.*
> *The graph doesn't show what's running in production.*

---

## 🤝 What I'm Looking For

| Signal | What it means to me |
|--------|----------------------|
| 🌍 **Global Impact** | Problems that matter beyond a single market |
| 🧩 **Technical Depth** | Systems complex enough to demand real engineering |
| 🤝 **Serious Teams** | People who value craft, reliability, and ownership |
| 🤖 **AI Integration** | Bringing real intelligence into real workflows |
| 🚀 **Startup Velocity** | Moving fast while building things that last |

**Open to:**
→ Full-time remote roles (AI / Backend / DevOps)
→ Contract infrastructure and systems work
→ Technical co-founder conversations
→ High-stakes, high-autonomy builds

---

## 📫 Contact

<p align="center">
  <a href="https://github.com/alleluiacervi-tech">
    <img src="https://img.shields.io/badge/GitHub-alleluiacervi--tech-0d1117?style=for-the-badge&logo=github&logoColor=white&labelColor=161b22" />
  </a>
</p>

<p align="center"><i>Fast response for projects worth moving on.</i></p>

---

<p align="center">
  <b>The most important systems I've built aren't public.</b><br/>
  <sub>That's not a limitation — that's how serious engineering works.</sub>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f1a2e,50:0d1220,100:08090d&height=120&section=footer" />
</p>
