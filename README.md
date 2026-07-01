<div align="center">
  <h1>AI Resume Analyzer</h1>
 
  <p><b>A serverless, AI-driven Applicant Tracking System (ATS) that scores resumes against job descriptions and returns actionable feedback to improve match rate.</b></p>
  <p>
    <img alt="React" src="https://img.shields.io/badge/React_19-4c84f3?style=for-the-badge&logo=react&logoColor=white">
    <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
    <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white">
    <img alt="Vite" src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white">
    <img alt="Puter.js" src="https://img.shields.io/badge/Puter.js-181758?style=for-the-badge&logoColor=white">
    <img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
  </p>
  <p>
    <a href="#live-demo"><b>Live Demo</b></a> ·
    <a href="#features"><b>Features</b></a> ·
    <a href="#tech-stack"><b>Tech Stack</b></a> ·
    <a href="#architecture"><b>Architecture</b></a> ·
    <a href="#getting-started"><b>Getting Started</b></a>
  </p>
</div>
---
 
## Overview
 
**AI Resume Analyzer** is a full-stack, AI-powered ATS that helps candidates understand exactly how well their resume matches a target role — before a recruiter ever sees it. A user uploads a resume, pastes a job listing, and receives an ATS compatibility score alongside specific, actionable feedback.
 
The entire application runs **without a traditional backend**. Authentication, file storage, and AI inference are handled client-side through the Puter.js serverless SDK, making the app cheap to run, fast to deploy, and simple to reason about.

---
 
## Live Demo
 
🔗 **[View the live application](https://aianalyzer-vert.vercel.app)**
 
Deployed on Vercel · Fully responsive · No sign-up friction
 
---
 
## Features
 
| Feature | Description |
| --- | --- |
| **Browser-native auth** | Sign-in and session handling entirely client-side via Puter.js — no auth server to provision or maintain. |
| **Resume upload & storage** | Users upload and securely store resumes, persisted through serverless storage. |
| **AI resume scoring** | Paste a job listing and receive an ATS match score with tailored, resume-specific feedback. |
| **Actionable feedback** | Concrete suggestions on how to improve alignment with the target role. |
| **Responsive UI** | Clean, mobile-first interface that adapts seamlessly across devices. |
| **Modular component design** | Reusable, well-typed components for a maintainable codebase. |
 
---
 
## Tech Stack
 
**Frontend**
- **React 19** — component-based UI with the latest concurrent features
- **React Router v7** — nested routes, data loaders, and error boundaries
- **TypeScript** — end-to-end static typing
- **Tailwind CSS** — utility-first styling
- **Zustand** — minimal, hook-based global state management
**Serverless & AI**
- **Puter.js** — client-side SDK providing auth, storage, and AI inference (GPT / Claude / OCR) with no backend
**Tooling & Deployment**
- **Vite** — fast dev server and optimized production builds
- **Docker** — containerized for consistent, reproducible environments
- **Vercel** — production hosting with CI-driven deploys
---
 
## Architecture
 
```
┌─────────────────────────────────────────────────────────┐
│                     Browser (Client)                     │
│                                                          │
│   React 19 + React Router v7 + TypeScript + Tailwind     │
│                          │                               │
│                    Zustand (state)                       │
│                          │                               │
│                     Puter.js SDK                         │
│          ┌───────────────┼───────────────┐              │
│          ▼               ▼               ▼              │
│        Auth          Storage         AI Inference        │
└─────────────────────────────────────────────────────────┘
```
 
The serverless model means there is no server to secure, scale, or pay for at idle — compute cost is deferred to the Puter.js runtime, and the client owns the full request lifecycle.
 
---
 
## Getting Started
 
### Prerequisites
 
- [Node.js](https://nodejs.org/en) (v18+)
- [npm](https://www.npmjs.com/)
- [Git](https://git-scm.com/)
### Installation
 
```bash
# Clone the repository
git clone https://github.com/Piro-Programmer/ai_resume_analyzer.git
cd ai_resume_analyzer
 
# Install dependencies
npm install
 
# Start the development server
npm run dev
```
 
Open [http://localhost:5173](http://localhost:5173) to view the app.
 
### Run with Docker
 
```bash
docker build -t ai-resume-analyzer .
docker run -p 5173:5173 ai-resume-analyzer
```
 
---
 
## Project Structure
 
```
ai_resume_analyzer/
├── app/                # Routes, components, and application logic
├── public/             # Static assets
├── constants/          # Shared constants and config
├── types/              # TypeScript type definitions
├── Dockerfile          # Container definition
├── vite.config.ts      # Vite configuration
└── package.json
```
 
---
 
## Roadmap
 
Planned enhancements to extend this beyond its tutorial foundation into a recruiter-facing tool:
 
- [ ] **Bulk analysis mode** — rank many resumes against a single job description
- [ ] **Explainable scoring** — surface exactly which skills matched and which are missing
- [ ] **Semantic matching** — embedding-based matching beyond keyword overlap
- [ ] **Bias/fairness audit** — flag exclusionary language in job descriptions
---
 
## License
 
This project is available under the MIT License.
 
---
 
<div align="center">
  <sub>Built by <a href="https://github.com/Piro-Programmer">Piro-Programmer</a></sub>
</div>
