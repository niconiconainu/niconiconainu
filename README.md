<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/header-light.svg">
  <img alt="niconiconainu — solo developer in Japan, shipping mobile apps with a fleet of AI agents" src="./assets/header-dark.svg" width="100%">
</picture>

<br><br>

[![Zenn](https://img.shields.io/badge/Zenn-3EA8FF?style=for-the-badge&logo=zenn&logoColor=white)](https://zenn.dev/nicoinu) [![Qiita](https://img.shields.io/badge/Qiita-55C500?style=for-the-badge&logo=qiita&logoColor=white)](https://qiita.com/niconiconainu) [![dev.to](https://img.shields.io/badge/dev.to-0A0A0A?style=for-the-badge&logo=devdotto&logoColor=white)](https://dev.to/nicoinu)

</div>

---

## `whoami`

個人開発者 / **solo developer in Japan**, running a one-person studio called **mulvolin-atelier**.

I take mobile products end to end — domain model, API, infrastructure, store submission,
and the writing that comes after. Most of the day-to-day execution is delegated to a fleet of
AI agents I orchestrate; my job is the part they can't do — deciding what is worth building,
and saying no.

**I build in public.** The failures included — a greyed-out subscribe button that got an app
rejected, a day lost to Android console configuration. Those tend to be the useful posts.

<br>

## 🚢 Currently shipping

| | Product | What it is |
|:--|:--|:--|
| 📚 | **mulvolin** | Flashcards built around *concepts*, not words. Learn one idea across many languages at once. iOS · Expo + NestJS on a Turborepo |
| ✏️ | **HITOFUDE** | Walk the city and draw with your GPS trail. One stroke, one route |
| 🐣 | **unipyoko** | A pet born from your photo, living its own life inside your phone |
| 🍜 | **gochisou-road** | Walk more, eat better. Your steps become the meal |
| 🏮 | **noren** | An agent that takes a single photo all the way to sellable overseas — *Agent Forge AI Hackathon Tokyo* |
| 🏺 | **[tsugumi](https://github.com/niconiconainu/tsugumi-kintsugi-design)** | Turns the story of a broken object into a kintsugi design and a workshop to repair it |

<sub>Most product repos are private while in development. Public ones are linked.</sub>

<br>

## 🤖 How the fleet works

`mulvolin-atelier` is an operations repo, not a product. It runs a set of specialised agents
across every service I own, on one shared workflow:

```
Issue ──▶ /req ──▶ /design ──▶ ★ human approval ──▶ /impl ──▶ /review ──▶ /verify ──▶ /ship ──▶ PR
                                                              │           │
                                                              └───────────┘
                                                        blocker / major → sent back
```

| Agent | Holds |
|:--|:--|
| `pm-lead` | Priorities, issue authoring |
| `dev-lead` | Implementation. **No git write access** |
| `reviewer` | Reads the diff only — never fixes it itself |
| `conflict-resolver` | Reconciles both intents. Never silently drops a side |
| `release` | The **only** agent with git write access |
| `retrospective` | Measures each cycle in minutes saved. No essays |

Two rules do most of the work: **there is exactly one human gate** (design approval, and only
when existing decisions don't already settle it), and **every decision becomes an ADR in the
product's own repo** — because an argument you don't write down, you will have again.

<br>

## ✍️ Writing

A three-part series on shipping subscriptions with **RevenueCat × Expo**, written from the
things that actually went wrong:

| | Article | JA | EN |
|:--|:--|:--|:--|
| 1 | The subscribe button couldn't be tapped — and that got the app rejected | [Zenn](https://zenn.dev/nicoinu/articles/revenuecat-expo-ios) · [Qiita](https://qiita.com/niconiconainu/items/d9b2b51d210ecfd25d06) | [dev.to](https://dev.to/nicoinu/my-subscribe-button-was-greyed-out-and-that-got-my-app-rejected-d42) |
| 2 | Android needed almost no code changes — and still ate a full day in configuration | [Zenn](https://zenn.dev/nicoinu/articles/revenuecat-expo-android) · [Qiita](https://qiita.com/niconiconainu/items/7e22e1a7cf73072ae288) | [dev.to](https://dev.to/nicoinu/android-needed-almost-no-code-changes-and-still-ate-a-full-day-in-configuration-a9m) |
| 3 | Where to split sandbox from production, when there is no right answer | [Zenn](https://zenn.dev/nicoinu/articles/revenuecat-expo-environments) · [Qiita](https://qiita.com/niconiconainu/items/900b4c00dfebefcc0fda) | — |

<br>

## 🧰 Stack

**Language**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)

**Mobile & Front-end**

![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white) ![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Back-end & Data**

![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white) ![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)

**Infra & Tooling**

![Turborepo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white) ![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white) ![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Sentry](https://img.shields.io/badge/Sentry-362D59?style=flat-square&logo=sentry&logoColor=white)

**Agents**

![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=claude&logoColor=white) ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=anthropic&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

<br>

## 📊 GitHub

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/0-profile-details.svg">
  <source media="(prefers-color-scheme: light)" srcset="./profile-summary-card-output/github/0-profile-details.svg">
  <img alt="Profile details" src="./profile-summary-card-output/github_dark/0-profile-details.svg" width="100%">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/1-repos-per-language.svg">
  <source media="(prefers-color-scheme: light)" srcset="./profile-summary-card-output/github/1-repos-per-language.svg">
  <img alt="Top languages by repository" src="./profile-summary-card-output/github_dark/1-repos-per-language.svg" width="48%">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/4-productive-time.svg">
  <source media="(prefers-color-scheme: light)" srcset="./profile-summary-card-output/github/4-productive-time.svg">
  <img alt="Productive time" src="./profile-summary-card-output/github_dark/4-productive-time.svg" width="48%">
</picture>

<br><br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/niconiconainu/niconiconainu/snek/snek-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/niconiconainu/niconiconainu/snek/snek-light.svg">
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/niconiconainu/niconiconainu/snek/snek-dark.svg" width="100%">
</picture>

<br>

<sub>Cards and snake are generated by this repo's own workflows and committed here — no third-party image host to go down.</sub>

</div>
