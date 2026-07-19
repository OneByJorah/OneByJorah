<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d0d0c,100:1a1a17&height=210&section=header&text=JORAHONE&fontSize=62&fontColor=FFB300&fontAlignY=36&desc=Network%20Security%20%7C%20Windows%20AD%20%7C%20Self-Hosted%20AI%20Infrastructure&descAlignY=56&descSize=16&descColor=FFB300&animation=fadeIn" width="100%"/>

<img src="https://readme-typing-svg.demolab.com/?font=JetBrains+Mono&size=22&duration=3000&pause=800&color=FFB300&center=true&vCenter=true&width=750&lines=Jhonattan+L.+Jimenez+%2F%2F+OneByJorah;Network+Security+Administrator+%40+VIDE+OIT;Founder+%2F%2F+JorahOne+LLC;Building+Hermes%3A+hub-and-satellite+AI+infra;35%2B+domain+controllers+%2F%2F+zero+downtime;Status%3A+OPERATIONAL" />

[![Profile Views](https://komarev.com/ghpvc/?username=OneByJorah&color=FFB300&style=for-the-badge&label=PROFILE+VIEWS)](https://github.com/OneByJorah)
[![Followers](https://img.shields.io/github/followers/OneByJorah?style=for-the-badge&color=0d0d0c&labelColor=0d0d0c&logoColor=FFB300&logo=github)](https://github.com/OneByJorah?tab=followers)
[![Portfolio](https://img.shields.io/badge/JorahOne.com-0d0d0c?style=for-the-badge&logo=googlechrome&logoColor=FFB300)](https://jorahone.com)
[![Org](https://img.shields.io/badge/JorahOne--Services-0d0d0c?style=for-the-badge&logo=github&logoColor=FFB300)](https://github.com/JorahOne-Services)

</div>

<br/>

## `> whoami`

```
NAME        Jhonattan L. Jimenez ("JorahOne")
ROLE        Network Security Administrator — VIDE Office of Information Technology
SCOPE       35+ domain controllers across St. Thomas (STT) & St. Croix (STX) districts
SIDE        Founder, JorahOne LLC — solo MSP for SMBs (AD, network security, M365)
LOCATION    St. Croix, U.S. Virgin Islands
STACK       Windows Server · Active Directory · Docker · PowerShell · self-hosted everything
PHILOSOPHY  Tailscale-only exposure · CLI over GUI · self-hosted over SaaS · MIT-licensed
UPTIME      Since [career start] — zero unplanned AD outages on my watch
```

<br/>

## `> ops-status`

<div align="center">

| Node | Function | Status |
|---|---|---|
| `ollama-vm` | Hermes primary inference (llama.cpp + LiteLLM) | 🟡 `OPERATIONAL` |
| `gpu-satellite` | VIDEaiCORE (Ornith-1.0-9B, RTX 3060 12GB) | 🟡 `OPERATIONAL` |
| `voice.jorahone.com` | Asterisk PBX / PJSIP / Mitel 6900s | 🟡 `OPERATIONAL` |
| `VIDE-STT / VIDE-STX` | 35+ Domain Controllers | 🟢 `MONITORED` |
| `j1-biographer` | Voice AI memoir agent | 🟠 `IN DEVELOPMENT` |
| `CIPHER` | AI-driven SOC (Suricata/Zeek/Wazuh/OpenVAS) | 🟠 `IN DEVELOPMENT` |

</div>

<br/>

## `> architecture — hermes hub & satellite`

```mermaid
flowchart LR
    subgraph Hub["🛰️ ollama-vm — HUB"]
        A[llama.cpp + LiteLLM Router]
        B[Honcho — Persistent Memory]
        C[Qdrant — Vector Store]
        D[Nightly RAG Pipeline]
    end

    subgraph Satellites["🏝️ Satellite Nodes"]
        E[GPU VM — VIDEaiCORE<br/>RTX 3060 12GB]
        F[Asterisk PBX / ARI]
        G[Telegram Bot]
        H[j1-biographer]
    end

    subgraph Reporting["📡 Approval & Reporting"]
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

<br/>

## `> current-deployments`

<table>
<tr>
<td width="50%" valign="top">

**🛰️ Hermes AI Infrastructure**
Hub-and-satellite multi-agent system. `ollama-vm` running llama.cpp + LiteLLM, Honcho for persistent memory, Qdrant for vector storage, nightly RAG pipeline, Telegram-based approval loop. GPU satellite node runs VIDEaiCORE via FastAPI gateway.
`STATUS: OPERATIONAL`

</td>
<td width="50%" valign="top">

**🏢 VIDE Network Operations**
Enterprise AD replication monitoring, animated NOC topology dashboards, Aruba switch SNMP dashboards (J1-SW-STX-CORE01), and DHCP/AD subnet discovery tooling across a distributed multi-district Windows environment.
`STATUS: MONITORING`

</td>
</tr>
<tr>
<td width="50%" valign="top">

**📞 Self-Hosted VoIP**
Asterisk PBX with PJSIP/ARI, Mitel 6900 phones over Tailscale, Cloudflare Tunnel for external SIP under the JorahOne Networks brand — no public port exposure.
`STATUS: OPERATIONAL`

</td>
<td width="50%" valign="top">

**🎙️ j1-biographer**
Voice AI biographer agent merging Asterisk ARI + Telegram inputs into a shared Hermes brain for memoir-quality, memory-augmented life storytelling.
`STATUS: IN DEVELOPMENT`

</td>
</tr>
<tr>
<td width="50%" valign="top">

**🛡️ CIPHER — AI-Driven SOC**
FastAPI backend integrating Suricata, Zeek, Wazuh, and OpenVAS for VIDE OIT threat detection and response.
`STATUS: IN DEVELOPMENT`

</td>
<td width="50%" valign="top">

**👕 TRANKILO**
Streetclothing brand with a self-hosted social media agent — Postiz, ComfyUI, Umami, n8n, Honcho, Telegram approval loop. Brand voice: calm as strength.
`STATUS: OPERATIONAL`

</td>
</tr>
</table>

<br/>

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

<br/>

## `> featured-repos`

<div align="center">

[![ADSentinel](https://github-readme-stats.vercel.app/api/pin/?username=OneByJorah&repo=ADSentinel&theme=dark&border_color=FFB300&title_color=FFB300&text_color=c9c9c9&bg_color=0d0d0c&icon_color=FFB300)](https://github.com/OneByJorah/ADSentinel)
[![SentryView](https://github-readme-stats.vercel.app/api/pin/?username=OneByJorah&repo=SentryView&theme=dark&border_color=FFB300&title_color=FFB300&text_color=c9c9c9&bg_color=0d0d0c&icon_color=FFB300)](https://github.com/OneByJorah/SentryView)
[![hermes-3d-office](https://github-readme-stats.vercel.app/api/pin/?username=OneByJorah&repo=hermes-3d-office&theme=dark&border_color=FFB300&title_color=FFB300&text_color=c9c9c9&bg_color=0d0d0c&icon_color=FFB300)](https://github.com/OneByJorah/hermes-3d-office)
[![J1-MSP-Toolkit](https://github-readme-stats.vercel.app/api/pin/?username=OneByJorah&repo=J1-MSP-Toolkit&theme=dark&border_color=FFB300&title_color=FFB300&text_color=c9c9c9&bg_color=0d0d0c&icon_color=FFB300)](https://github.com/OneByJorah/J1-MSP-Toolkit)

</div>

<br/>

## `> tech-stack`

<div align="center">

**Infrastructure & Identity**
![Windows Server](https://img.shields.io/badge/Windows_Server-0d0d0c?style=flat-square&logo=windows&logoColor=FFB300)
![Active Directory](https://img.shields.io/badge/Active_Directory-0d0d0c?style=flat-square&logo=microsoft&logoColor=FFB300)
![Entra ID](https://img.shields.io/badge/Entra_ID-0d0d0c?style=flat-square&logo=microsoftazure&logoColor=FFB300)
![PowerShell](https://img.shields.io/badge/PowerShell-0d0d0c?style=flat-square&logo=powershell&logoColor=FFB300)

**Self-Hosted & Networking**
![Docker](https://img.shields.io/badge/Docker-0d0d0c?style=flat-square&logo=docker&logoColor=FFB300)
![Ubuntu](https://img.shields.io/badge/Ubuntu-0d0d0c?style=flat-square&logo=ubuntu&logoColor=FFB300)
![Tailscale](https://img.shields.io/badge/Tailscale-0d0d0c?style=flat-square&logo=tailscale&logoColor=FFB300)
![Cloudflare](https://img.shields.io/badge/Cloudflare-0d0d0c?style=flat-square&logo=cloudflare&logoColor=FFB300)
![Aruba](https://img.shields.io/badge/Aruba_Networking-0d0d0c?style=flat-square&logo=arubanetworks&logoColor=FFB300)
![Nginx](https://img.shields.io/badge/Caddy%2FNginx-0d0d0c?style=flat-square&logo=nginxproxymanager&logoColor=FFB300)

**AI / Automation**
![Ollama](https://img.shields.io/badge/Ollama-0d0d0c?style=flat-square&logo=ollama&logoColor=FFB300)
![FastAPI](https://img.shields.io/badge/FastAPI-0d0d0c?style=flat-square&logo=fastapi&logoColor=FFB300)
![n8n](https://img.shields.io/badge/n8n-0d0d0c?style=flat-square&logo=n8n&logoColor=FFB300)
![React](https://img.shields.io/badge/React-0d0d0c?style=flat-square&logo=react&logoColor=FFB300)
![Three.js](https://img.shields.io/badge/Three.js-0d0d0c?style=flat-square&logo=threedotjs&logoColor=FFB300)

**Monitoring & Security**
![Suricata](https://img.shields.io/badge/Suricata-0d0d0c?style=flat-square&logo=suricata&logoColor=FFB300)
![Wazuh](https://img.shields.io/badge/Wazuh-0d0d0c?style=flat-square&logo=wazuh&logoColor=FFB300)
![Grafana](https://img.shields.io/badge/Grafana-0d0d0c?style=flat-square&logo=grafana&logoColor=FFB300)
![Uptime Kuma](https://img.shields.io/badge/Uptime_Kuma-0d0d0c?style=flat-square&logo=uptimekuma&logoColor=FFB300)

</div>

<br/>

## `> stats`

<div align="center">
<img src="https://github-readme-stats.vercel.app/api?username=OneByJorah&show_icons=true&theme=dark&bg_color=0d0d0c&title_color=FFB300&icon_color=FFB300&text_color=c9c9c9&border_color=FFB300&hide_border=false" height="165"/>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=OneByJorah&theme=dark&background=0d0d0c&stroke=FFB300&ring=FFB300&fire=FFB300&currStreakLabel=FFB300&border=FFB300" height="165"/>
</div>

<div align="center">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=OneByJorah&layout=compact&theme=dark&bg_color=0d0d0c&title_color=FFB300&text_color=c9c9c9&border_color=FFB300&hide_border=false" height="165"/>
<img src="https://github-readme-trophies.vercel.app/?username=OneByJorah&theme=darkhub&column=4&margin-w=8&margin-h=8&title_color=FFB300&text_color=c9c9c9&icon_color=FFB300&border_color=FFB300&no-bg=false&bg_color=0d0d0c" height="165"/>
</div>

<br/>

## `> activity-graph`

<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=OneByJorah&theme=react-dark&bg_color=0d0d0c&color=FFB300&line=FFB300&point=ffffff&area=true&area_color=FFB300&hide_border=true" width="100%"/>
</div>

<br/>

## `> contribution-snake`

<div align="center">
<img src="https://raw.githubusercontent.com/OneByJorah/OneByJorah/output/snake-dark.svg" width="100%" alt="snake animation — activate via the included GitHub Action workflow"/>
</div>

<sub>Renders once the `snake.yml` workflow (included alongside this README) runs for the first time — see setup notes below.</sub>

<br/>

## `> philosophy`

```
"Every satellite reports to the hub. Every hub answers to Tailscale.
 Nothing public that doesn't have to be. Nothing manual that can be scripted."
```

<br/>

## `> connect`

<div align="center">

📍 St. Croix, U.S. Virgin Islands &nbsp;|&nbsp; 🏢 JorahOne LLC &nbsp;|&nbsp; 🛰️ [JorahOne-Services](https://github.com/JorahOne-Services)

[![Portfolio](https://img.shields.io/badge/jorahone.com-FFB300?style=flat-square&logo=googlechrome&logoColor=0d0d0c)](https://jorahone.com)
[![Voice PBX](https://img.shields.io/badge/voice.jorahone.com-FFB300?style=flat-square&logo=asterisk&logoColor=0d0d0c)](#)

<sub>Archipelago metaphor intentional — every node self-hosted, every link Tailscale-only, every deploy MIT-licensed.</sub>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a17,100:0d0d0c&height=100&section=footer" width="100%"/>
