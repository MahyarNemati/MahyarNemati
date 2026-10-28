<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b26,55:24283b,100:3b3f5c&height=190&section=header&text=MAHYAR%20NEMATI&fontSize=54&fontColor=C0CAF5&fontAlign=50&fontAlignY=38&desc=full-stack%20%C2%B7%20cloud-native%20%C2%B7%20security%20engineer&descSize=16&descAlign=50&descAlignY=60&animation=fadeIn" width="100%" />

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&duration=2600&pause=900&color=B4A7E6&center=true&vCenter=true&width=700&height=44&lines=%24+whoami+%E2%86%92+Mahyar+Nemati;Secure+by+design.+Built+to+scale.;Distributed+systems+%C2%B7+Zero-trust+%C2%B7+Platform+eng.;Go+%C2%B7+TypeScript+%C2%B7+Python+%C2%B7+Rust+%C2%B7+Kubernetes" alt="typing" />

<a href="https://mnmti.com"><img src="https://img.shields.io/badge/mnmti.com-1a1b26?style=for-the-badge&logo=googlechrome&logoColor=9ECEC0" /></a>
<a href="https://www.linkedin.com/in/mahyarnemati"><img src="https://img.shields.io/badge/LinkedIn-1a1b26?style=for-the-badge&logo=linkedin&logoColor=A9C1E8" /></a>
<img src="https://img.shields.io/badge/Toronto,_ON-1a1b26?style=for-the-badge&logo=googlemaps&logoColor=E6B8C8" />
<img src="https://img.shields.io/badge/status-open_to_roles-1a1b26?style=for-the-badge&labelColor=24283b&color=1a1b26" />

</div>

```yaml
~/mahyar $ cat profile.yml

name:     Mahyar Nemati
role:     Solution Architect · Full-Stack Engineer
base:     Toronto, ON
exp:      5+ yrs shipping production web & cloud systems
degree:   B.Eng. Computer Engineering
focus:
  - Distributed systems    # event-driven, idempotent, horizontally scalable
  - Cloud-native platform  # Kubernetes, GitOps, IaC, observability
  - Identity & security    # OIDC, passkeys, zero-trust, supply-chain
  - Developer experience   # fast CI, golden paths, internal tooling
open_to:  Senior Full-Stack · Platform · Solution Architect roles
```

```ts
const engineer = {
  ships:     "small, typed, tested, observable",
  designs:   "for failure, scale and the 3am pager",
  secures:   "by default — not as a sprint ticket",
  measures:  "p99 latency, not vibes",
  documents: "decisions (ADRs), not just code",
};
```

### `> ./expertise --verbose`

| Domain | What I actually ship |
|:--|:--|
| **System Design** | Multi-tenant SaaS, event sourcing & CQRS, caching strategies, queues, sharding, back-pressure |
| **Backend & APIs** | Go, Python/Flask, Node/Express, Java/Spring — REST, gRPC, GraphQL, WebSockets |
| **Frontend** | React, Next.js, TypeScript, Tailwind — fast, typed, accessible, edge-rendered UIs |
| **Platform & DevOps** | Docker, Kubernetes, Helm, Terraform, ArgoCD (GitOps), GitHub Actions |
| **Cloud** | Azure, AWS, GCP, Cloudflare Workers — serverless & edge |
| **Security Eng.** | OAuth2 / OIDC, Okta, passkeys (WebAuthn), RBAC/ABAC, secrets mgmt, SBOM & signing |
| **Data** | PostgreSQL, Redis, Kafka, ClickHouse — schema design, indexing, query tuning |
| **Reliability** | OpenTelemetry, Prometheus, Grafana — SLOs, load testing (k6), chaos & incident response |

<details>
<summary><b><code>> cat ~/designs/saas.arch</code></b> &nbsp;— how I architect a multi-tenant platform <i>(click to expand)</i></summary>
<br/>

```text
                  ┌─────────────── edge ────────────────┐
   client  ──▶    │   CDN · WAF · TLS · rate limiting   │
                  └──────────────────┬──────────────────┘
                                     ▼
          ┌──────────── API gateway (OIDC / Okta) ─────────────┐
          │    tenant resolver  →  RBAC  →  request context    │
          └───────┬──────────────────┬──────────────────┬──────┘
                  ▼                  ▼                  ▼
            core services      realtime layer      async workers
            Go · Node · Py     WebSockets · SSE    Kafka · Redis
                  └──────────────────┼──────────────────┘
                                     ▼
              Postgres (RLS per tenant) · Redis · object storage
                                     ▼
          OpenTelemetry → traces · metrics · logs → alerts → on-call
```

**Trade-offs I design for:** idempotent writes · outbox pattern · per-tenant rate limits · blue/green deploys · zero-downtime migrations
</details>

<details>
<summary><b><code>> sudo ./security --audit</code></b> &nbsp;— my security baseline on every project <i>(click to expand)</i></summary>
<br/>

```diff
+ [✓] OWASP Top 10 / ASVS-driven code review
+ [✓] Threat modeling (STRIDE) before the first commit
+ [✓] Zero-trust auth: OIDC, passkeys, short-lived tokens, least privilege
+ [✓] Secrets in Vault, never in repos · pre-commit secret scanning
+ [✓] Supply chain: SBOMs, signed artifacts (Sigstore), pinned dependencies
+ [✓] Tenant isolation: RLS, scoped API keys, immutable audit trails
- [✗] "we'll add security later"
```

<img src="https://img.shields.io/badge/OWASP-1a1b26?style=flat-square&logo=owasp&logoColor=B4A7E6" />
<img src="https://img.shields.io/badge/Burp_Suite-1a1b26?style=flat-square&logo=burpsuite&logoColor=E6B8C8" />
<img src="https://img.shields.io/badge/Wireshark-1a1b26?style=flat-square&logo=wireshark&logoColor=A9C1E8" />
<img src="https://img.shields.io/badge/Kali_Linux-1a1b26?style=flat-square&logo=kalilinux&logoColor=9ECEC0" />
<img src="https://img.shields.io/badge/Vault-1a1b26?style=flat-square&logo=vault&logoColor=E8D4A2" />
<img src="https://img.shields.io/badge/WebAuthn-1a1b26?style=flat-square&logo=webauthn&logoColor=E6B8C8" />
<img src="https://img.shields.io/badge/Okta-1a1b26?style=flat-square&logo=okta&logoColor=A9C1E8" />
<img src="https://img.shields.io/badge/Snyk-1a1b26?style=flat-square&logo=snyk&logoColor=B4A7E6" />
</details>

<details>
<summary><b><code>> cat ~/.radar/2026.md</code></b> &nbsp;— tech I'm adopting, trialing & watching <i>(click to expand)</i></summary>
<br/>

| ring | tech |
|:--|:--|
| 🟣 **adopt** | Go · TypeScript · Postgres · Kubernetes · Terraform · OpenTelemetry · GitHub Actions |
| 🔵 **trial** | Rust · ArgoCD / GitOps · Passkeys (WebAuthn) · ClickHouse · Cloudflare Workers · Bun |
| 🟢 **assess** | eBPF · WebAssembly (WASI) · CRDTs / local-first · Sigstore & SLSA · Temporal workflows |
| ⚪ **hold** | hand-rolled auth · snowflake servers · untested migrations |
</details>

### `> ls ~/projects --featured`

| Project | Stack | What it does |
|:--|:--|:--|
| [**Tweepy-Project**](https://github.com/MahyarNemati/Tweepy-Project) | `Python` `Data Pipelines` | Built for Ontario's Ministry of Transportation — fuses multi-source data to predict highway accidents and alert operators in time to act |
| [**OLE**](https://github.com/MahyarNemati/OLE) | `Java` `Blockchain` `Crypto` | Custom blockchain + encrypted mobile e-wallet with privacy-preserving transactions |
| [**job-application-dashboard**](https://github.com/MahyarNemati/job-application-dashboard) | `TypeScript` `Automation` | JobHunter — upload a resume, auto-discover & apply to jobs across LinkedIn, Indeed, Glassdoor |
| [**chatapp**](https://github.com/MahyarNemati/chatapp) | `Node` `Socket.io` | Real-time chat rooms over WebSockets |
| [**receipt-app**](https://github.com/MahyarNemati/receipt-app) | `Parsing` `Automation` | POS receipts → email → parsed → tax-year expense report, zero manual entry |
| [**BoltFare**](https://github.com/MahyarNemati/BoltFare) | `Solidity` | Web3 smart-contract project |

### `> git log --oneline -now`

```diff
+ building   zero-trust auth gateway — OIDC + passkeys, written in Go
+ shipping   GitOps homelab: k3s · ArgoCD · Terraform · sealed secrets
+ hardening  CI supply chain: SBOMs, signed images, provenance
+ studying   distributed consensus (Raft) & offensive security
- tolerating untyped JS, flaky tests, "works on my machine"
```

### `> stack --all`

| layer | tools |
|:--|:--|
| **lang** | <img src="https://skillicons.dev/icons?i=go,rust,ts,js,py,java,solidity&theme=dark" height="36" /> |
| **front** | <img src="https://skillicons.dev/icons?i=react,nextjs,svelte,tailwind,vitest&theme=dark" height="36" /> |
| **back** | <img src="https://skillicons.dev/icons?i=nodejs,bun,express,flask,spring,graphql,kafka,rabbitmq&theme=dark" height="36" /> |
| **data** | <img src="https://skillicons.dev/icons?i=postgres,redis,mysql,mongodb,sqlite,elasticsearch&theme=dark" height="36" /> |
| **cloud** | <img src="https://skillicons.dev/icons?i=aws,azure,gcp,cloudflare,docker,kubernetes,terraform,ansible,nginx&theme=dark" height="36" /> |
| **ops** | <img src="https://skillicons.dev/icons?i=githubactions,prometheus,grafana,jest,selenium,linux,kali,bash,git&theme=dark" height="36" /> |

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/MahyarNemati/MahyarNemati/output/snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/MahyarNemati/MahyarNemati/output/snake-light.svg" />
  <img alt="contribution snake" src="https://raw.githubusercontent.com/MahyarNemati/MahyarNemati/output/snake-dark.svg" />
</picture>

```
> echo "Have a hard problem? Let's architect it — securely."  ▍
```

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:3b3f5c,45:24283b,100:1a1b26&height=110&section=footer" width="100%" />
