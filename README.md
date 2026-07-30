<div align="center">

![OneByJorah banner](docs/assets/banner.svg)

# OneByJorah

Network Security Administrator — JorahOne Networks

[![License: MIT](https://img.shields.io/badge/license-MIT-brightgreen?style=flat-square)](LICENSE)
[![Location](https://img.shields.io/badge/location-St%20Thomas%2C%20USVI-blue?style=flat-square)](https://maps.google.com/?q=St+Thomas+USVI)
[![Stack](https://img.shields.io/badge/stack-AD%20%D7%90%20Docker%20%D7%90%20PowerShell%20%D7%90%20Tailscale-0ea5e9?style=flat-square)](#-tech-stack)
[![Profile Views](https://komarev.com/ghpvc/?username=OneByJorah&style=flat-square&color=38bdf8)](https://github.com/OneByJorah)
[![Repos](https://img.shields.io/badge/dynamic/json?style=flat-square&color=f59e0b&label=repos&query=%24.public_repos&url=https%3A%2F%2Fapi.github.com%2Fusers%2FOneByJorah)](https://github.com/OneByJorah?tab=repositories)

</div>

---

<p align="center">
  <img src="docs/assets/screenshot.png" alt="OneByJorah archipelago preview" width="90%">
</p>

## `> whoami`

```
NAME        Jhonattan L. Jimenez ("JorahOne")
ROLE        Network Security Administrator — JorahOne Networks
SIDE        Founder, JorahOne LLC — solo MSP for SMBs (AD, network security, M365)
LOCATION    St. Thomas, U.S. Virgin Islands
STACK       Windows Server · Active Directory · Docker · PowerShell · self-hosted everything
PHILOSOPHY  Tailscale-only exposure · CLI over GUI · self-hosted over SaaS · MIT-licensed
UPTIME      Zero unplanned AD outages since career start
```

## `> ops-status`

| Node | Purpose | State |
|---|---|---|
| `ollama-vm` | Main Hermes inference node — llama.cpp + LiteLLM | operational |
| `gpu-satellite` | Private AI core — Ornith-1.0-9B on RTX 3060 12 GB | operational |
| `voice.jorahone.com` | Asterisk PBX stack with PJSIP + Snom endpoints | operational |
| `j1-biographer` | Voice AI memoir agent | in development |
| `CIPHER` | AI-driven SOC — Suricata, Zeek, Wazuh, OpenVAS | in development |

## `> architecture — hermes hub & satellite`

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

## `> changelog`

```
[RECENT]     Aruba SNMP dashboards · GCDS/Entra Connect directory sync · iOS on-device LLM (Hermes)
             PowerShell DHCP/AD subnet discovery tooling · CIPHER SOC buildout

[EARLIER]    jorahone-ai-stack Docker Compose (Honcho + Qdrant + LiteLLM + Caddy)
             J1-FLEET (Three.js fleet dashboard) · J1-PULSE (uptime monitor) · J1-BENCH (LLM eval harness)
             StackDeploy multi-service orchestration · hermes-realm (PixiJS archipelago viz)

[FOUNDATION] j1-adrepl-monitor — open-sourced AD replication daemon for 35+ DC environment
             NOC Operations Platform v5.0 · JorahOne MSP framework (SOPs, SLAs, onboarding playbooks)
```

## `> featured-repos`

<table>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/ChatForge">ChatForge</a></h3>
    <img src="https://raw.githubusercontent.com/OneByJorah/ChatForge/main/screenshot.png" alt="ChatForge" width="100%"/>
    <p>AI-powered chat interface — multi-model support (OpenAI, Anthropic, Ollama), real-time WebSocket streaming</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/ChatForge?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/ChatForge?color=f59e0b&style=flat-square" alt="license"/>
    <img src="https://img.shields.io/github/last-commit/OneByJorah/ChatForge?color=34d399&style=flat-square" alt="last commit"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/AIStack">AIStack</a></h3>
    <img src="https://raw.githubusercontent.com/OneByJorah/AIStack/master/screenshot.png" alt="AIStack" width="100%"/>
    <p>Unified AI infrastructure stack — Docker Compose deployment for Ollama, Qdrant, LiteLLM, Honcho + Caddy</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/AIStack?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/AIStack?color=f59e0b&style=flat-square" alt="license"/>
    <img src="https://img.shields.io/github/last-commit/OneByJorah/AIStack?color=34d399&style=flat-square" alt="last commit"/>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/BenchDash">BenchDash</a></h3>
    <p>Automated benchmarking platform for local LLMs on Ollama — auto-discover, test, rank, and visualize</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/BenchDash?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/BenchDash?color=f59e0b&style=flat-square" alt="license"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/NexusCore">NexusCore</a></h3>
    <p>Enterprise NOC platform — unified monitoring for AD, NTP, DNS, PBX, helpdesk, and AI-powered alerting</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/NexusCore?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/NexusCore?color=f59e0b&style=flat-square" alt="license"/>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/VoiceCortex">VoiceCortex</a></h3>
    <p>Self-hosted phone AI assistant — real-time voice conversations over telephone via STT > LLM > TTS</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/VoiceCortex?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/VoiceCortex?color=f59e0b&style=flat-square" alt="license"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/OpsCenter">OpsCenter</a></h3>
    <p>AI agent operations dashboard — real-time monitoring, task management, fleet visibility for Hermes agents</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/OpsCenter?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/OpsCenter?color=f59e0b&style=flat-square" alt="license"/>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/SentryView">SentryView</a></h3>
    <p>Self-hosted RTSP NVR dashboard — live monitoring, recording, and timeline review for IP cameras</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/SentryView?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/SentryView?color=f59e0b&style=flat-square" alt="license"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/CommandDesk">CommandDesk</a></h3>
    <p>Self-hosted AI helpdesk agent — multi-platform ticketing, email-to-ticket, AI auto-response</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/CommandDesk?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/CommandDesk?color=f59e0b&style=flat-square" alt="license"/>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/PrimeHub">PrimeHub</a></h3>
    <p>Portfolio hub — repo health, standardization status, and ecosystem overview for OneByJorah infrastructure</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/PrimeHub?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/PrimeHub?color=f59e0b&style=flat-square" alt="license"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/VirtOffice">VirtOffice</a></h3>
    <p>Animated 3D virtual office for Hermes AgentOS subagents — real-time isometric AI visualization</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/VirtOffice?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/VirtOffice?color=f59e0b&style=flat-square" alt="license"/>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/ConfigVault">ConfigVault</a></h3>
    <p>Network backup and asset management dashboard — device inventory, backup scheduling, snapshot restore</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/ConfigVault?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/ConfigVault?color=f59e0b&style=flat-square" alt="license"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/DirWatch">DirWatch</a></h3>
    <p>Active Directory DC monitoring dashboard — real-time health, replication status, and alerting</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/DirWatch?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/DirWatch?color=f59e0b&style=flat-square" alt="license"/>
  </td>
</tr>
<tr>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/MSPEngine">MSPEngine</a></h3>
    <p>Windows 10/11 provisioning and debloat utility for MSP technicians — one-click setup</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/MSPEngine?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/MSPEngine?color=f59e0b&style=flat-square" alt="license"/>
  </td>
  <td width="50%" valign="top">
    <h3><a href="https://github.com/OneByJorah/StackForge">StackForge</a></h3>
    <p>Multi-service container orchestration — deploy and manage complex Docker stacks</p>
    <img src="https://img.shields.io/github/languages/top/OneByJorah/StackForge?color=38bdf8&style=flat-square" alt="language"/>
    <img src="https://img.shields.io/github/license/OneByJorah/StackForge?color=f59e0b&style=flat-square" alt="license"/>
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

## `> activity-graph`

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=OneByJorah&theme=react-dark&hide_border=true&color=38bdf8&line=f59e0b&point=38bdf8" alt="Activity graph"/>
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

## `> connect`

- 🌐 Portfolio: [jorahone.com](https://jorahone.com)
- 📡 VoIP site: [voice.jorahone.com](https://voice.jorahone.com)
- 🐙 GitHub Org: [JorahOne-Services](https://github.com/JorahOne-Services)
- 📧 Contact: info@jorahone.com

---

<p align="center">Built with 🌴 by <a href="https://github.com/OneByJorah">OneByJorah</a> · <a href="https://jorahone.com">jorahone.com</a></p>
