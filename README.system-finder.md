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

Every comparable tool in this category runs on a recurring subscription. System Finder doesn't.

| Tool | One-Time Purchase | Subscription Required |
|---|:---:|:---:|
| **System Finder** | ✅ **$200 (one-time)** | ❌ Not required |
| Cluely | ❌ Not available | ✅ Included |
| ShadeCoder | ❌ Not available | ✅ Included |
| LockedIn AI | ❌ Not available | ✅ Included |
| Final Round AI | ❌ Not available | ✅ Included |
| Interview Sidekick | ❌ Not available | ✅ Included |
| Saner AI | ❌ Not available | ✅ Included |
| Interview Coder | ❌ Not available | ✅ Included |
| Leetcode Wizard | ❌ Not available | ✅ Included |
| OfferGenie | ❌ Not available | ✅ Included |
| Interview Hammer AI | ❌ Not available | ✅ Included |
| Flowming AI | ❌ Not available | ✅ Included |

Pay once, plug in your own OpenAI + Deepgram keys, and the only ongoing cost is direct API usage — no markup, no monthly fee, no vendor lock-in.

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
