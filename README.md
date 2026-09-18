<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0EA5E9,100:8B5CF6&height=220&section=header&text=Vibe%20Apply&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=Speak%20a%20job.%20We'll%20find%20it,%20contact%20them,%20and%20apply.&descAlignY=58&descSize=18&animation=fadeIn" width="100%"/>

<a href="https://devfolio.co/projects/vibe-apply-c25f">
  <img src="https://img.shields.io/badge/🏆_VIEW_ON_DEVFOLIO-vibe--apply-8B5CF6?style=for-the-badge&labelColor=0EA5E9" alt="Devfolio"/>
</a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&duration=2800&pause=900&color=0EA5E9&center=true&vCenter=true&multiline=true&repeat=true&width=680&height=90&lines=%22Data+Analyst+in+Bangalore%22+%E2%86%92+jobs+found;%E2%86%92+recruiters+discovered;%E2%86%92+emails+sent+%E2%9C%94" alt="Typing SVG" />

<br/>

![Team](https://img.shields.io/badge/Built_for-HackByte_3.0-0EA5E9?style=flat-square&logo=devpost&logoColor=white)
![Team ID](https://img.shields.io/badge/Team-9749-8B5CF6?style=flat-square)
![Status](https://img.shields.io/badge/status-active-22C55E?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)

![React](https://img.shields.io/badge/React_18.2-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/GPT--4o--mini-412991?style=for-the-badge&logo=openai&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=googlesheets&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram_Bot-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)

</div>

<br/>

## 🚀 Why We Built This

Job hunting in 2025 still feels like it's stuck in 2010. Open 20 tabs, refresh job boards, copy-paste the same cold email, hope it lands somewhere other than a recruiter's trash. It's exhausting, repetitive, and wildly inefficient — practically a full-time job just to find a job.

**Vibe Apply turns one sentence into a finished job-search sprint.**

<div align="center">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=18&pause=1200&color=8B5CF6&center=true&vCenter=true&width=560&lines=%22Backend+Developer+in+Berlin%22;%22Marketing+Manager%2C+Remote%22;%22Business+Analyst+in+Bangalore%22" alt="examples" />
</div>

<br/>

## 😩 The Problem

<table align="center">
<tr>
<td width="25%" align="center">🕵️‍♂️<br/><b>Recruiter Hunt</b><br/><sub>Hours lost hunting for a hiring manager's email that isn't on LinkedIn or the careers page</sub></td>
<td width="25%" align="center">📋<br/><b>Manual Search</b><br/><sub>20+ tabs, endless refreshing, the same copy-paste on every application</sub></td>
<td width="25%" align="center">📨<br/><b>Generic Outreach</b><br/><sub>Identical cold emails to everyone, zero personalization, zero replies</sub></td>
<td width="25%" align="center">🗂️<br/><b>No Tracking</b><br/><sub>No record of where you applied, no follow-ups, missed opportunities</sub></td>
</tr>
</table>

<br/>

## ✨ What It Actually Does

```
you:  "Data Analyst in Bangalore"
```

<div align="center">

| Step | What happens |
|:---:|:---|
| 1️⃣ | Scrapes LinkedIn for matching, live job listings |
| 2️⃣ | Extracts title, company, location & URL — deduplicated |
| 3️⃣ | Digs up recruiter names straight from the listing |
| 4️⃣ | Finds their professional email address |
| 5️⃣ | Writes a personalized cold email with GPT-4o-mini |
| 6️⃣ | Sends it — no `Ctrl+V` required |
| 7️⃣ | Logs everything into one shareable Google Sheet |

</div>

<div align="center">
<sub>⏱️ From search to sent emails: <b>minutes</b>, not days.</sub>
</div>

<br/>

## 🏗️ Architecture

<div align="center">

```mermaid
flowchart LR
    A["🎙️ User Input<br/>voice or text"] --> B["⚡ n8n Webhook /<br/>Telegram Trigger"]
    B --> C["🧠 GPT-4o-mini<br/>parse role + location"]
    C --> D["🕷️ AgentQL<br/>scrape LinkedIn jobs"]
    D --> E["🔁 Split & process<br/>each job"]
    E --> F["🕵️ AgentQL<br/>find recruiter"]
    F --> G["📧 Hunter.io<br/>find email"]
    G --> H["📊 Google Sheets<br/>append / update"]
    H --> I["✍️ GPT-4o-mini<br/>draft cold email"]
    I --> J["📤 Gmail<br/>send outreach"]
    J --> K["✅ Response back<br/>to user"]

    style A fill:#0EA5E9,color:#fff
    style K fill:#22C55E,color:#fff
    style C fill:#8B5CF6,color:#fff
    style I fill:#8B5CF6,color:#fff
```

</div>

**Design philosophy:** workflow-first (no traditional backend server), event-driven, stateless — Google Sheets *is* the database.

<br/>

## 🖥️ See It In Action

<div align="center">

<b>1. One line in, results out</b><br/>
<img src="assets/demo-app.png" width="80%"/>

<br/><br/>

<b>2. The n8n orchestration engine</b><br/>
<img src="assets/n8n-workflow.png" width="90%"/>

<br/><br/>

<b>3. Personalized outreach, sent automatically</b><br/>
<img src="assets/gmail-outreach.png" width="80%"/>

<br/><br/>

<b>4. Every job & recruiter, tracked live</b><br/>
<img src="assets/job-sheet.png" width="90%"/>

</div>

<br/>

## 🧠 Tech Stack

<div align="center">

| Layer | Tools |
|---|---|
| **Frontend** | React 18.2 · React Router 6.9 · Axios · Web Speech API |
| **Orchestration** | n8n (webhook + Telegram triggers) |
| **AI / NLP** | OpenAI GPT-4o-mini · Whisper (voice transcription) |
| **Scraping** | AgentQL (natural-language, JS-rendered page scraping) |
| **Email Discovery** | Hunter.io |
| **Storage** | Google Sheets API |
| **Alt. Interface** | Telegram Bot API |

</div>

<br/>

## 🎯 Key Innovations

- 🎙️ **Voice-to-Workflow** — speak your search, get results
- 🧩 **AI Query Parsing** — natural language → structured LinkedIn search
- 🕵️ **Recruiter Discovery at Scale** — names *and* emails, automatically
- 🔌 **Zero Backend** — n8n *is* the backend
- 📊 **Sheets as Database** — free, familiar, instantly shareable
- 🔀 **Multi-Channel** — same workflow via web app or Telegram bot

<br/>

## 📈 Impact

<div align="center">

| | Before Vibe Apply | After Vibe Apply |
|---|:---:|:---:|
| Time per application | 15–20 min | **~1 min for 20 jobs** |
| Applications per day | 5–10 | **100+/week** |
| Outreach | Generic | **Personalized, direct to recruiter** |
| Tracking | None | **Centralized Google Sheet** |

</div>

<br/>

## 👥 Team 9749 — Built at HackByte 3.0

<div align="center">

Harshith G &nbsp;•&nbsp; Kesav M &nbsp;•&nbsp; Abhinay B &nbsp;•&nbsp; Pardhesh M

<br/><br/>

<a href="https://devfolio.co/projects/vibe-apply-c25f">
  <img src="https://img.shields.io/badge/🔗_Check_out_the_full_project_on-DEVFOLIO-8B5CF6?style=for-the-badge&labelColor=0EA5E9&logo=vercel&logoColor=white" alt="Devfolio Project Link" width="480"/>
</a>

</div>

<br/>

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8B5CF6,100:0EA5E9&height=120&section=footer" width="100%"/>
<sub>Made with ❤️ for HackByte 3.0</sub>
</div>
