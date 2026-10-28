<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=24&duration=2800&pause=900&color=B4A7E6&center=true&vCenter=true&width=720&height=60&lines=%24+whoami+%E2%86%92+Mahyar+Nemati;Solution+Architect+%2F%2F+Full-Stack+Engineer;Secure+by+design.+Built+to+scale.;AI-native+SaaS+%C2%B7+Cloud+%C2%B7+Zero-Trust+Auth" alt="Mahyar Nemati" />

<a href="https://mnmti.com"><img src="https://img.shields.io/badge/mnmti.com-1a1b26?style=for-the-badge&logo=googlechrome&logoColor=9ECEC0" /></a>
<a href="https://www.linkedin.com/in/mahyarnemati"><img src="https://img.shields.io/badge/LinkedIn-1a1b26?style=for-the-badge&logo=linkedin&logoColor=A9C1E8" /></a>
<img src="https://img.shields.io/badge/Toronto,_ON-1a1b26?style=for-the-badge&logo=googlemaps&logoColor=E6B8C8" />

</div>

```yaml
~/mahyar $ cat profile.yml

name:     Mahyar Nemati
role:     Solution Architect · Full-Stack Engineer
base:     Toronto, ON
exp:      5+ yrs shipping production web & cloud systems
degree:   B.Eng. Computer Engineering
focus:
  - AI-native SaaS       # multi-tenant platforms on LLM APIs
  - Cloud architecture   # Azure, AWS, Kubernetes, IaC
  - Identity & security  # Okta, OAuth2/OIDC, SSO, zero-trust
  - Developer tooling    # MCP servers, browser automation, agents
open_to:  Senior Full-Stack · Solution Architect roles
```

```ts
const engineer = {
  ships:     "small, typed, tested, observable",
  designs:   "for failure, scale and the 3am pager",
  secures:   "by default — not as a sprint ticket",
  documents: "decisions (ADRs), not just code",
};
```

### `> ./expertise --verbose`

| Domain | What I actually ship |
|:--|:--|
| **System Design** | Multi-tenant architecture, event-driven systems, caching, queues, horizontal scaling |
| **Backend & APIs** | Python/Flask, Node/Express, Go, Java/Spring, GraphQL, gRPC, REST contracts |
| **Frontend** | React, Next.js, TypeScript, Tailwind — fast, typed, accessible UIs |
| **Cloud & DevOps** | Azure, AWS, Docker, Kubernetes, Terraform, GitHub Actions CI/CD |
| **Auth & Security** | Okta, OAuth2 / OIDC, SSO, RBAC, row-level tenant isolation, secrets management |
| **AI Engineering** | LLM integration (Claude API), MCP servers, RAG, agent tooling, automation |
| **Data** | PostgreSQL, Redis, Kafka, schema design, indexing & query tuning |
| **Reliability** | Observability (Prometheus, Grafana), testing pyramids, SLOs, incident response |

### `> cat ~/designs/saas.arch`

```text
                  ┌─────────────── edge ────────────────┐
   client  ──▶    │   CDN · WAF · TLS · rate limiting   │
                  └──────────────────┬──────────────────┘
                                     ▼
          ┌──────────── API gateway (OIDC / Okta) ─────────────┐
          │    tenant resolver  →  RBAC  →  request context    │
          └───────┬──────────────────┬──────────────────┬──────┘
                  ▼                  ▼                  ▼
            core services      AI orchestrator     async workers
            Flask · Node       LLM + MCP tools     queue · Redis
                  └──────────────────┼──────────────────┘
                                     ▼
              Postgres (RLS per tenant) · Redis · object storage
                                     ▼
               logs · traces · metrics · alerts  →  on-call
```

### `> sudo ./security --audit`

```diff
+ [✓] OWASP Top 10 / ASVS-driven code review
+ [✓] Threat modeling (STRIDE) before the first commit
+ [✓] Zero-trust auth: OIDC, short-lived tokens, MFA, least privilege
+ [✓] Secrets in vaults, never in repos · dependency & SBOM scanning
+ [✓] Tenant isolation: RLS, scoped API keys, audit trails
- [✗] "we'll add security later"
```

<p>
<img src="https://img.shields.io/badge/OWASP-1a1b26?style=flat-square&logo=owasp&logoColor=B4A7E6" />
<img src="https://img.shields.io/badge/Burp_Suite-1a1b26?style=flat-square&logo=burpsuite&logoColor=E6B8C8" />
<img src="https://img.shields.io/badge/Wireshark-1a1b26?style=flat-square&logo=wireshark&logoColor=A9C1E8" />
<img src="https://img.shields.io/badge/Kali_Linux-1a1b26?style=flat-square&logo=kalilinux&logoColor=9ECEC0" />
<img src="https://img.shields.io/badge/Vault-1a1b26?style=flat-square&logo=vault&logoColor=E8D4A2" />
<img src="https://img.shields.io/badge/Okta-1a1b26?style=flat-square&logo=okta&logoColor=A9C1E8" />
<img src="https://img.shields.io/badge/Snyk-1a1b26?style=flat-square&logo=snyk&logoColor=B4A7E6" />
<img src="https://img.shields.io/badge/Let's_Encrypt-1a1b26?style=flat-square&logo=letsencrypt&logoColor=9ECEC0" />
</p>

### `> ls ~/projects --featured`

| Project | Stack | What it does |
|:--|:--|:--|
| [**cdp-extended-mcp**](https://github.com/MahyarNemati/cdp-extended-mcp) | `TypeScript` `MCP` `CDP` | MCP server for Chrome DevTools Protocol — fetch interception, device emulation, a11y audits, perf profiling |
| [**job-application-dashboard**](https://github.com/MahyarNemati/job-application-dashboard) | `TypeScript` `Automation` | JobHunter — upload a resume, auto-discover & apply to jobs across LinkedIn, Indeed, Glassdoor |
| [**Tweepy-Project**](https://github.com/MahyarNemati/Tweepy-Project) | `Python` `ML` | Built for Ontario's Ministry of Transportation — predicts highway accidents from multi-source data and alerts operators |
| [**BoltFare**](https://github.com/MahyarNemati/BoltFare) | `Solidity` | Web3 smart-contract project |
| [**receipt-app**](https://github.com/MahyarNemati/receipt-app) | `Parsing` `Automation` | POS receipts → email → parsed → tax-year expense report, zero manual entry |

### `> git log --oneline -now`

```diff
+ building   multi-tenant AI platforms on LLM APIs
+ shipping   MCP servers that give AI agents real browser superpowers
+ hardening  auth flows: Okta / OIDC / SSO across tenants
+ studying   distributed systems & offensive security
- tolerating untyped JS, flaky tests, "works on my machine"
```

### `> stack --all`

| layer | tools |
|:--|:--|
| **lang** | <img src="https://skillicons.dev/icons?i=ts,js,py,go,rust,java,solidity&theme=dark" height="36" /> |
| **front** | <img src="https://skillicons.dev/icons?i=react,nextjs,tailwind,vitest&theme=dark" height="36" /> |
| **back** | <img src="https://skillicons.dev/icons?i=nodejs,express,flask,spring,graphql,kafka,rabbitmq&theme=dark" height="36" /> |
| **data** | <img src="https://skillicons.dev/icons?i=postgres,mysql,redis,supabase&theme=dark" height="36" /> |
| **cloud** | <img src="https://skillicons.dev/icons?i=azure,aws,gcp,cloudflare,docker,kubernetes,terraform,githubactions,nginx&theme=dark" height="36" /> |
| **ops** | <img src="https://skillicons.dev/icons?i=prometheus,grafana,jest,selenium,linux,kali,bash,git&theme=dark" height="36" /> |

<div align="center">

```
> echo "Have a hard problem? Let's architect it — securely."  ▍
```

</div>
