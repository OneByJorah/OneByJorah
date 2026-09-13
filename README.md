<div align="center">

![OneByJorah banner](docs/assets/banner.svg)

# OneByJorah

**Network Security Administrator at JorahOne Networks — I build and self-host the infrastructure that keeps small businesses secure, connected, and automated.**

<a href="https://github.com/OneByJorah?tab=repositories"><img src="https://img.shields.io/badge/dynamic/json?style=flat-square&color=f59e0b&label=repos&query=%24.public_repos&url=https%3A%2F%2Fapi.github.com%2Fusers%2FOneByJorah" alt="Public repos"></a>
<a href="https://github.com/OneByJorah"><img src="https://img.shields.io/github/followers/OneByJorah?style=flat-square&color=38bdf8" alt="Followers"></a>
<img src="https://img.shields.io/badge/location-St%20Thomas%2C%20USVI-blue?style=flat-square" alt="St Thomas, USVI">
<img src="https://img.shields.io/badge/license-MIT-brightgreen?style=flat-square" alt="MIT">
<img src="https://img.shields.io/badge/self--hosted-over%20SaaS-0ea5e9?style=flat-square" alt="Self-hosted">

</div>

![OneByJorah profile overview](docs/assets/screenshot.png)

## What This Is

This is the org profile repository for **JorahOne Networks**. It is not an application — it is the front page that describes who I am, how I work, and the self-hosted infrastructure behind the tools in this org.

Every project here follows the same philosophy: **nothing public that doesn't have to be, nothing manual that can be scripted**. Exposure is Tailscale-only by default, CLI is preferred over GUI, self-hosted over SaaS, and everything is MIT-licensed.

## `> whoami`

```
NAME        Jhonattan L. Jimenez ("JorahOne")
ROLE        Network Security Administrator — JorahOne Networks
SIDE        Founder, JorahOne LLC — solo MSP for SMBs (AD, network security, M365)
LOCATION    St. Thomas, U.S. Virgin Islands
STACK       Windows Server · Active Directory · Docker · PowerShell · self-hosted everything
PHILOSOPHY  Tailscale-only exposure · CLI over GUI · self-hosted over SaaS · MIT-licensed
```

## `> architecture — hermes hub & satellites`

```mermaid
flowchart LR
    subgraph Hub["ollama-vm — HUB"]
        A[llama.cpp + LiteLLM Router]
        B[Honcho — Persistent Memory]
        C[Qdrant — Vector Store]
        D[Nightly RAG Pipeline]
    end

    subgraph Satellites["Satellite Nodes"]
        E[GPU VM — Private AI Core RTX 3060 12GB]
        F[Asterisk PBX / ARI]
        G[Telegram Bot]
        H[j1-biographer]
    end

    subgraph Reporting["Approval & Reporting"]
        I[Telegram Approval Loop]
    end

    A <--> B
    A <--> C
    D --> C
    E <--> A
    F <--> A
    G <--> A
    H <--> A
    A --> I

    style Hub fill:#0d0d0c,stroke:#FFB300,color:#FFB300
    style Satellites fill:#0d0d0c,stroke:#FFB300,color:#FFB300
    style Reporting fill:#0d0d0c,stroke:#FFB300,color:#FFB300
```

<sub>Archipelago metaphor, on purpose: every node self-hosted, every link Tailscale-only, every deploy MIT-licensed.</sub>

## `> ops-status`

| Node | Purpose | State |
|---|---|---|
| `ollama-vm` | Main Hermes inference node — llama.cpp + LiteLLM | operational |
| `gpu-satellite` | Private AI core — Ornith-1.0-9B on RTX 3060 12 GB | operational |
| `voice.jorahone.com` | Asterisk PBX stack with PJSIP + Snom endpoints | operational |
| `j1-biographer` | Voice AI memoir agent | in development |
| `CIPHER` | AI-driven SOC — Suricata, Zeek, Wazuh, OpenVAS | in development |

## `> current-deployments`

<table>
<tr>
<td width="50%" valign="top">

**Hermes AI Infrastructure**
Hub-and-satellite multi-agent system. `ollama-vm` running llama.cpp + LiteLLM, Honcho for persistent memory, Qdrant for vector storage, nightly RAG pipeline, Telegram-based approval loop. GPU satellite node runs a private inference core via FastAPI gateway.
`STATUS: OPERATIONAL`

</td>
<td width="50%" valign="top">

**Enterprise Network Operations**
Enterprise AD replication monitoring, animated NOC topology dashboards, Aruba switch SNMP dashboards, and DHCP/AD subnet discovery tooling across distributed multi-site Windows environments.
`STATUS: MONITORING`

</td>
</tr>
<tr>
<td width="50%" valign="top">

**Self-Hosted VoIP**
Asterisk PBX with PJSIP/ARI, over Tailscale, Cloudflare Tunnel for external SIP under the JorahOne Networks brand — no public port exposure.
`STATUS: OPERATIONAL`

</td>
<td width="50%" valign="top">

**j1-biographer**
Voice AI biographer agent merging Asterisk ARI + Telegram inputs into a shared Hermes brain for memoir-quality, memory-augmented life storytelling.
`STATUS: IN DEVELOPMENT`

</td>
</tr>
<tr>
<td width="50%" valign="top">

**CIPHER — AI-Driven SOC**
FastAPI backend integrating Suricata, Zeek, Wazuh, and OpenVAS for enterprise threat detection and response.
`STATUS: IN DEVELOPMENT`

</td>
<td width="50%" valign="top">

**TRANKILO**
Streetclothing brand with a self-hosted social media agent — Postiz, ComfyUI, Umami, n8n, Honcho, Telegram approval loop. Brand voice: calm as strength.
`STATUS: OPERATIONAL`

</td>
</tr>
</table>

## `> featured-repos`

<table>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/ChatForge">ChatForge</a></h3>
    <p>AI-powered chat interface — multi-model support (OpenAI, Anthropic, Ollama), real-time WebSocket streaming</p>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/AIStack">AIStack</a></h3>
    <p>Unified AI infrastructure stack — Docker Compose deployment for Ollama, Qdrant, LiteLLM, Honcho + Caddy</p>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/BenchDash">BenchDash</a></h3>
    <p>Automated benchmarking platform for local LLMs on Ollama — auto-discover, test, rank, and visualize</p>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/NexusCore">NexusCore</a></h3>
    <p>Enterprise NOC platform — unified monitoring for AD, NTP, DNS, PBX, helpdesk, and AI-powered alerting</p>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/VoiceCortex">VoiceCortex</a></h3>
    <p>Self-hosted phone AI assistant — real-time voice conversations over telephone via STT &rsaquo; LLM &rsaquo; TTS</p>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/OpsCenter">OpsCenter</a></h3>
    <p>AI agent operations dashboard — real-time monitoring, task management, fleet visibility for Hermes agents</p>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/SentryView">SentryView</a></h3>
    <p>Self-hosted RTSP NVR dashboard — live monitoring, recording, and timeline review for IP cameras</p>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/CommandDesk">CommandDesk</a></h3>
    <p>Self-hosted AI helpdesk agent — multi-platform ticketing, email-to-ticket, AI auto-response</p>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/ConfigVault">ConfigVault</a></h3>
    <p>Network backup and asset management dashboard — device inventory, backup scheduling, snapshot restore</p>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/DirWatch">DirWatch</a></h3>
    <p>Active Directory DC monitoring dashboard — real-time health, replication status, and alerting</p>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/MSPEngine">MSPEngine</a></h3>
    <p>Windows 10/11 provisioning and debloat utility for MSP technicians — one-click setup</p>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/AegisPass">AegisPass</a></h3>
    <p>Self-service Active Directory password reset portal — LDAPS-pinned, workflow-driven, fully audited</p>
  </td>
</tr>
</table>

## `> tech-stack`

<p>
  <img src="https://img.shields.io/badge/-Windows%20Server-0078D6?style=flat-square&logo=windows&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Active%20Directory-003366?style=flat-square"/>
  <img src="https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/-PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black"/>
  <img src="https://img.shields.io/badge/-Tailscale-000000?style=flat-square&logo=tailscale&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white"/>
  <img src="https://img.shields.io/badge/-Ollama-000000?style=flat-square"/>
  <img src="https://img.shields.io/badge/-Qdrant-FF6B6B?style=flat-square"/>
</p>

## `> stats`

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=OneByJorah&show_icons=true&theme=transparent&title_color=38bdf8&text_color=e2e8f0&icon_color=f59e0b&hide_border=true" alt="GitHub stats"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=OneByJorah&theme=transparent&hide_border=true&ring=f59e0b&fire=f59e0b&currStreakLabel=38bdf8" alt="GitHub streak"/>
</p>

## `> contribution-snake`

<p align="center">
  <img src="https://raw.githubusercontent.com/OneByJorah/OneByJorah/output/github-contribution-grid-snake.svg" alt="Contribution snake"/>
</p>

## `> philosophy`

```
"Every satellite reports to the hub. Every hub answers to Tailscale.
 Nothing public that doesn't have to be. Nothing manual that can be scripted."
```

## Screenshots

| View | |
|---|---|
| ![Profile overview](docs/assets/screenshot.png) | ![Mobile](docs/assets/screenshot-mobile.png) |
| ![Full viewport](docs/screenshots/main.viewport.full.png) | ![Mobile capture](docs/screenshots/main.mobile.png) |

## Contributing

Fork, branch, and open a pull request — see [CONTRIBUTING.md](CONTRIBUTING.md). [Open an issue](https://github.com/OneByJorah/OneByJorah/issues) for bugs or ideas.

## License

MIT — see [LICENSE](LICENSE).

## Connect

- [jorahone.com](https://jorahone.com)
- [GitHub Org](https://github.com/OneByJorah)
- [info@jorahone.com](mailto:info@jorahone.com)
