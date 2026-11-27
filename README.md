# Hi, I'm Deepak Pun 👋

**Full-Stack Developer & Cloud / DevOps Engineer** based in Maryland, USA.  
Focused on what happens *after* `git push`—building, containerizing, automating, and monitoring resilient cloud infrastructure.

🌐 **Portfolio & Interactive Resume:** [deepakpun.com](https://deepakpun.com) ([View Resume](https://deepakpun.com/resume))  
🚀 **Live Microservices & Observability Lab:** [labs.deepakpun.com](https://labs.deepakpun.com)  
📝 **Technical Notes & Homelab Logs:** [notes.deepakpun.com](https://notes.deepakpun.com)  
💼 **LinkedIn:** [LinkedIn](https://www.linkedin.com/in/mrpun)

---

### 🏗️ Featured Architecture: Multiverse Labs (`https://labs.deepakpun.com`)

A containerized microservices application deployed on a DigitalOcean Linux Droplet with automated GitHub Actions CI/CD, Vitest/Supertest integration checks, Nginx SSL/TLS reverse proxy, and full Prometheus + Grafana + Loki observability.

```text
                        ┌───────────────────────────────────────┐
                        │           Public Internet             │
                        └───────────────────┬───────────────────┘
                                            │ HTTPS (443)
                                            ▼
                        ┌───────────────────────────────────────┐
                        │    Nginx Reverse Proxy (SSL/TLS)      │
                        └───┬───────────────┬───────────────┬───┘
                  /         │         /api/ │      /grafana/│
                  ▼         │               ▼               ▼
        ┌───────────────────┐     ┌───────────────────┐   ┌───────────────────┐
        │   Next.js Client  │     │  Express Core API │   │      Grafana      │
        │   (TypeScript)    │     │   (REST + Health) │   │ (Unified Portal)  │
        └───────────────────┘     └─────────┬─────────┘   └────┬─────────┬────┘
                                            │                  │         │
                                            ▼          Metrics │         │ Logs
                                  ┌───────────────────┐        ▼         ▼
                                  │      MongoDB      │   ┌─────────┐ ┌─────────┐
                                  │  (mongo_data vol) │   │Prometheus│ │  Loki   │
                                  └───────────────────┘   └────┬────┘ └────▲────┘
                                                               │           │
                                            ┌──────────────────┴───┐       │
                                            ▼                      ▼       │
                                  ┌───────────────────┐  ┌───────────────┐ │
                                  │   Node Exporter   │  │   Blackbox    │ │
                                  │ (Droplet Vitals)  │  │ (HTTP/SSL 15s)│ │
                                  └───────────────────┘  └───────────────┘ │
                                                                           │
                                                         ┌─────────────────┴─┐
                                                         │     Promtail      │
                                                         │  (Docker Socket)  │
                                                         └───────────────────┘
```

---

### 🚀 Highlighted Projects

| Project | Architecture & Highlights | Links |
| :--- | :--- | :--- |
| **Multiverse Labs** *(Capstone 01)* | Decoupled microservices (**Next.js**, **Express**, **MongoDB**) orchestrated with **Docker Compose**. Automated **GitHub Actions** CI/CD with **Vitest & Supertest** API checks, **Nginx** reverse proxy, and **Grafana / Prometheus / Loki** monitoring. | [Live App](https://labs.deepakpun.com) • [Repo](https://github.com/DeepakPun/labs.deepakpun.com) |
| **Serverless Full-Stack** *(Capstone 02)* | Serverless **Express** API on **AWS Lambda** + **API Gateway (HTTP API)** with least-privilege **IAM**. Private **S3** React frontend served via **CloudFront (OAC)** & custom edge rewrite function, **AWS Amplify** CI/CD, and $0.00 FinOps teardown. | [Architecture Notes](https://notes.deepakpun.com/notes/en/aws-serverless-fullstack/) |
| **Tech Notes** | Fast, minimal static Markdown knowledge base documenting cloud setups, Docker networking, and troubleshooting logs, built with **Astro** and deployed via **Vercel**. | [Live Site]([https://notes.deepakpun.com](https://notes.deepakpun.com/) • [Repo](https://github.com/DeepakPun/noted.deepakpun.com) |
| **Portfolio Hub** | Central `whoami`-style developer hub and interactive Next.js resume component with built-in PDF preview/download, routed via **AWS Route 53**. | [Live Site](https://deepakpun.com) • [Repo](https://github.com/DeepakPun/deepakpun.com) |

---

### 🛠️ Technical Stack

* **Cloud & DevOps:** Docker, Docker Compose, GitHub Actions (CI/CD), AWS (EC2, S3, Lambda, API Gateway, CloudFront, Route 53, IAM, Amplify, CloudWatch), DigitalOcean, Nginx, Linux CLI
* **Observability & Testing:** Grafana, Prometheus, Loki, Promtail, Node Exporter, Blackbox Exporter, Vitest, Supertest
* **Frontend:** TypeScript, JavaScript (ES6+), Next.js, React, Astro, Tailwind CSS, HTML5/CSS3
* **Backend & Data:** Node.js, Express.js, REST APIs, MongoDB, Git / GitHub

---

### 🎯 Current Focus
* Preparing for the **AWS Certified Solutions Architect – Associate (SAA-C03)** certification.
* Open to **Entry-Level Full-Stack Developer**, **Junior DevOps Engineer**, and **Cloud Engineering** roles (Remote or Baltimore / Washington D.C. metro area).
