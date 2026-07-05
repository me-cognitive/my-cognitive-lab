# 🧠 System Finder — AI Assistant for Live Calls

**Duration:** August 2025 – Present  
**Role:** Independent Developer & Product Owner

---

## 📘 Overview

**System Finder** is a real-time AI assistant that runs alongside any live call, meeting, or interview — listening, transcribing, and surfacing contextual AI help without interrupting the conversation. It started as a reverse-engineering exercise on a commercial Electron app and has since grown into an independently owned product with its own infrastructure, pricing model, and feature set.

Where competing tools in this space charge a recurring subscription, System Finder is a **one-time purchase** — the user brings their own OpenAI and Deepgram API keys and pays only for what they actually use.

---

## 🚀 Core Features

- **Live Transcript** — real-time speech-to-text (Deepgram) of both system audio and microphone, so nothing said in the call is missed.
- **Live Insights** — an AI layer on top of the transcript with one-click actions: *"What should I say next?"*, *"Suggest follow-up questions"*, *"Fact-check recent statements"*.
- **Specify / Generate** — type a question directly to the assistant and stream back an AI-generated answer (OpenAI) without leaving the call.
- **Smart Profile Generator** — turn a resume, document, or free-text description into a tailored AI assistant profile (interview prep, legal, medical, engineering, and more), including document/image upload and profession-specific presets.
- **Invisibility Mode** — toggle the overlay to stay hidden from screen-share/recording capture.
- **Adjustable Transparency** — opacity control so the overlay never blocks what's underneath.
- **Smart Network Relay** — auto-detects blocked corporate networks and routes API calls through a low-latency Cloudflare edge relay (sub-20ms, 200+ cities, TLS 1.3) instead of failing outright.
- **Self-Updating** — background updater with live progress and one-click install, no manual redownloads.
- **Cross-Platform** — Windows and macOS, built on Electron.

---

## 💰 Why System Finder

Almost every comparable tool in this category runs on a recurring subscription — and keeps billing every month whether you open the app or not. System Finder doesn't.

*Pricing below reflects each vendor's standard month-to-month rate (not annual/promo-discounted), checked July 2026 — subscription pricing changes often, so verify on the vendor's own site before quoting it elsewhere.*

| Tool | Starting Monthly Price | 6-Month Cost | Break-even vs. System Finder's $200 | Billed If Unused? |
|---|---:|---:|:---:|:---:|
| **System Finder** | **$0** (just your own API usage) | **$200 total, ever** | — | ❌ Never |
| Cluely | $19.99 (up to $149.99 for the undetectable tier) | ~$120 (up to ~$900) | ~10 months | ✅ Yes |
| ShadeCoder | $29 | ~$174 | ~7 months | ✅ Yes |
| LockedIn AI | $35 (up to $148 unlimited) | ~$210 (up to ~$888) | ~6 months | ✅ Yes |
| Final Round AI | $149 | ~$894 | ~1.3 months | ✅ Yes |
| Interview Sidekick | $60 (standard rate listed up to $80) | ~$360 (up to ~$480) | ~3.3 months | ✅ Yes |
| Saner AI¹ | $12 (Standard $20) | ~$72 (up to ~$120) | ~17 months | ✅ Yes |
| Interview Coder² | $299 (or $799 as a separate lifetime purchase) | ~$1,794 | <1 month | ✅ Yes, unless the $799 lifetime tier is bought instead |
| Leetcode Wizard | ~$58 (€49) | ~$348 | ~3.4 months | ✅ Yes |
| OfferGenie³ | $99.99 (or pay-as-you-go credits from $29, non-expiring) | ~$600 (subscription route) | ~2 months | ✅ Yes on the subscription plan |
| Interview Hammer AI | $29.99 | ~$180 | ~6.7 months | ✅ Yes |
| Flowming AI | Pricing not publicly listed | — | — | — |

¹ Saner AI is a general AI productivity/notes assistant rather than a live-call copilot — included for completeness since it was part of the original comparison set.  
² Interview Coder also sells a $799 one-time lifetime pass — real, but 4x System Finder's price for the same "no subscription" outcome.  
³ OfferGenie also offers one-time credit packs — cheaper up front, but credits deplete and need topping up, unlike a flat one-time purchase.

**The core difference isn't just the sticker price:**

- **You pay whether you use it or not.** Every tool above bills monthly regardless of whether you had a single call that month. System Finder is paid once — using it every day or once a year costs the same $0 in software fees.
- **No markup on AI usage.** Subscription tiers bundle in a marked-up allowance of OpenAI/Deepgram usage. System Finder passes your own API keys straight through — you pay the provider's real rate, nothing on top.
- **No lock-in.** Cancel a subscription and access stops immediately, including to your own past sessions in some tools. System Finder keeps working indefinitely once purchased — there's nothing to cancel and nothing that expires.
- **Predictable long-term cost.** Every subscription in this table costs more than $200 within 7 months at most (several within weeks). Past that point, System Finder is strictly cheaper for as long as you keep using it.

---

## 🔧 Technical Highlights

- Electron multi-window architecture: a floating always-on-top overlay, a settings window, and a first-run setup flow, kept in sync without a shared preload where one isn't available.
- Custom auto-updater pipeline: background download with live percentage, cancel support, and an in-place relaunch that preserves the original install path — built for both Windows (exe/bat) and macOS (zip/shell).
- Own edge infrastructure (Cloudflare Worker relay) for regions/networks where direct API access is blocked, with automatic fallback detection on startup.
- Protected build pipeline: packaging → encryption → native launcher, so the shipped binary isn't a bare Electron app.

---

## 🗺️ Roadmap Ideas

- Speaker diarization (label each participant instead of a single merged transcript)
- Auto-generated post-call summary (key points, action items) saved to history
- Calendar-aware profile switching (auto-load the right assistant profile before a scheduled call)
- Local/offline transcription fallback for low-connectivity or privacy-sensitive sessions
- Searchable, tagged transcript history across past sessions

---

## 🧩 Skills Demonstrated

- Reverse Engineering & Independent Product Development
- Electron Framework & Cross-Platform Desktop Development
- AI API Integration (OpenAI, Deepgram)
- Edge Infrastructure Design (Cloudflare Workers)
- Real-Time Audio Capture & Streaming Transcription
- Secure Build & Auto-Update Pipeline Engineering
- Product Pricing Strategy & Competitive Positioning

---

**Author:** Ashish Tiwari  
**Date:** August 2025 – Present  
**Project:** System Finder  
**Website:** [systemfinderapi.com](https://www.systemfinderapi.com/)
