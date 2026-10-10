# 📸 TripDownMemoryLane — Full-Stack Multimodal AI Journaling Platform

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Backend](https://img.shields.io/badge/Backend-Node.js%20%2B%20Express%205-green)](#)
[![AI](https://img.shields.io/badge/AI-Google%20Vision%20%2B%20Hugging%20Face%20%2B%20TTS-blue)](#)

> **Portfolio Note**  
> This is my personal portfolio fork of the team project.  
> I was the **primary backend & AI pipeline engineer**.

An interactive multimodal platform that helps elderly users archive and revisit personal memories through computer vision, generative storytelling, adaptive quizzes, and speech synthesis.


## 👩‍💻 My Contributions

I owned the **backend and AI orchestration layer**:

- Designed and implemented the Express 5 API gateway
- Integrated **Google Cloud Vision API** for image feature & entity extraction
- Built the **Hugging Face** inference pipeline for contextual story + quiz generation
- Implemented **Google Cloud TTS** for dynamic audio synthesis (Base64)
- Wrote REST API contracts and automated integration tests (Jest)
- Coordinated the overall multimodal data flow between frontend and AI services

**Frontend** was primarily developed by [@cts0424](https://github.com/cts0424).


## 📽️ Demo & Presentation

| 📺 Video Demonstration | 📑 Technical Presentation |
| :--- | :--- |
| [![Watch the Demo](https://img.youtube.com/vi/AnKT1Wh7sXg/hqdefault.jpg)](https://www.youtube.com/watch?v=AnKT1Wh7sXg) | [![View Presentation](https://img.shields.io/badge/View_Presentation-PDF-red?style=for-the-badge&logo=adobe-acrobat-reader)](./docs/FinalProjectPresentation.pdf) |
| End-to-end walkthrough: photo upload → AI story generation → quiz → TTS playback | Architecture, AI pipeline, privacy design, and team allocation |


## 🏛️ System Architecture

```text
[ React Frontend (:4000) ]
          │  Base64 Image
          ▼
[ Express API Gateway (:4001) ]   ←── My main contribution
  ├── 1. Google Cloud Vision     → Feature & Entity Extraction
  ├── 2. Hugging Face Inference  → Story + Quiz Generation
  └── 3. Google Cloud TTS        → Audio Synthesis
          │
          ▼
[ Client: Audio Playback + Interactive Quiz ]
```

This repository is the monorepo that orchestrates two Git submodules:

| Tier | Repository | Owner | Stack |
|------|------------|-------|-------|
| **Backend API** | [backend](https://github.com/TripDownMemoryLane/backend) | **@jyliew1912** (me) | Node.js, Express 5, Google Vision, Hugging Face, TTS, Jest |
| Frontend Client | [memoryLaneFrontend](https://github.com/TripDownMemoryLane/memoryLaneFrontend) | @cts0424 + JL | React, Tailwind CSS |


## 🚀 Quick Start

```bash
git clone --recurse-submodules https://github.com/jyliew1912/TripDownMemoryLane.git
cd TripDownMemoryLane

# Configure API keys
cp backend/.env.example backend/.env

# Install & run both services
npm run install:all
npm run dev
```

- Frontend: http://localhost:4000  
- Backend:  http://localhost:4001  
- Backend tests: `npm run test:backend`


## 📄 License

MIT License. See [LICENSE](LICENSE).

**Original team repository:** [TripDownMemoryLane/TripDownMemoryLane](https://github.com/TripDownMemoryLane/TripDownMemoryLane)
