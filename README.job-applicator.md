# 🎯 Job Applicator — Automated Job Search That Explains Itself

**Duration:** 2026 – Present
**Role:** Independent Developer & Product Owner
**Status:** v1.0.0, released November 2026
**Licence:** Free for every System Finder customer — the *same* licence, no second purchase

---

## 📘 Overview

**Job Applicator** finds good-fit jobs, applies at a human pace, and reports every run.

It is a separate Windows desktop app that ships alongside [System Finder](README.system-finder.md)
and runs on **the System Finder licence the user already has**, on the computer where System Finder
is activated. There is no extra purchase, no second key and no separate sign-in — if the licence is
active, the app simply runs.

The design goal was the opposite of the usual "auto-apply to 500 jobs" tool. Volume is deliberately
low, every action is reported back, and the app refuses to guess on the user's behalf.

---

## 🚀 Core Features

- **Runs the user's own browser.** It drives the user's existing Chrome or Edge, signed in with
  their own job-site account. It never sees or stores their password.
- **Private by default.** Profile, resume and run history stay in `%APPDATA%\JobApplicator\` on the
  user's own PC. Nothing is uploaded to a server for safekeeping.
- **Human pace, on purpose.** Around 20 applications a day by default, with randomised pauses
  between actions, and a hard stop the moment it hits a captcha or a quota page.
- **A report for every run.** What it applied to, what needs the user, what it skipped and why —
  plus the keywords recruiters asked for that the user's resume never mentions.
- **It never guesses.** Screening questions it can't answer from the stored profile go to a
  Questions screen. The user answers once, and matching jobs are retried.

---

## 🔐 Licensing Model

This is the unusual part, and the part that has to stay exact:

| | |
|---|---|
| Price | **₹0.** Free for every System Finder customer |
| Licence | The **same** System Finder licence. Nothing extra to buy |
| Machines | **One** — the computer where System Finder is activated. The licence is hardware-locked |
| Activation screen | **None.** The app finds the System Finder licence on the PC and verifies it itself |
| Second licence key | **Never issued.** There is no separate Job Applicator key |

Verification on every start: signature, machine fingerprint, expiry, revocation list, plus a
short-lived server-signed pass from the product's own Cloudflare edge relay. If the licence is
missing, invalid, expired or revoked, the app refuses to run — which is also why a public download
link is harmless: an unlicensed copy cannot be used.

> It does **not** work "on all your devices" or "with any licence". One activated machine, one
> licence, no exceptions.

---

## ⚠️ Honest Framing

Job portals' terms of service generally don't permit automated use. Job Applicator keeps its volume
low and stops at captchas, which **reduces** the risk of an account being flagged — but it does not
remove it. That caveat is stated in the product README, in the user guide, and on the public site,
and it isn't buried.

---

## 🔧 Technical Highlights

- **Licence-gated at runtime, not at download.** A layered check (local signature + machine
  fingerprint + expiry + revocation list + a short-lived server-signed pass) means the binary can be
  distributed openly while still being unusable without an activated System Finder licence.
- **Browser automation against a real, signed-in browser** rather than a headless session with
  stored credentials — the user's login never leaves their machine.
- **Local-first data model.** All state lives under `%APPDATA%\JobApplicator\`; there is no account
  to create and no server-side profile.
- **Deliberate rate limiting and fail-stop behaviour** as product features: randomised pacing, a
  daily cap, and an immediate halt on captcha or quota pages.
- **CI → R2 release pipeline.** Every push to the app's path builds and publishes the executable and
  a `version.json` to Cloudflare R2, which the public download link serves directly.

---

## 🧩 Skills Demonstrated

- Hardware-locked licensing and offline licence verification design
- Browser automation driving a user's own authenticated session
- Local-first, privacy-preserving desktop data design
- Windows desktop development and packaging
- CI/CD release automation to object storage (Cloudflare R2)
- Honest product positioning around terms-of-service risk

---

## ⬇️ Download

**[JobApplicator.exe](https://pub-6e55e125512d46ae8b9465275c991c79.r2.dev/bundles-2026/job-applicator/JobApplicator.exe)** — Windows, ~19 MB, v1.0.0

Requires an activated System Finder installation on the same PC. No licence key to enter.

---

**Author:** Ashish Tiwari
**Project:** Job Applicator (companion to System Finder)
**Website:** [systemfinderapi.com](https://www.systemfinderapi.com/#job-applicator)
