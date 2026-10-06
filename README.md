# 💠 V — Personal AI Assistant

> **A sleek, futuristic personal AI assistant inspired by JARVIS, powered by Google Gemini.**
> Built with React 19, TypeScript, Tailwind CSS v4, and the modern `@google/genai` SDK.

---

## 🌟 Key Features

- **Holographic Core Animation:** Dynamic HUD-style orb with live states (`IDLE`, `PROCESSING`, `RESPONDING`, `SYSTEM TELEMETRY`).
- **JARVIS Persona:** Sharp, confident, articulate, and dedicated to structured problem-solving, planning, and execution.
- **Smart Rate-Limit & Quota Protection:** Adaptive retry management with real-time countdown timers to avoid quota exhaustion.
- **Resilient Model Routing:** Prioritizes high-throughput models with seamless automated fallbacks.
- **One-Click Directives:** Quick starter chips for daily briefing, problem breakdown, professional drafting, and concept explanation.
- **Context Management:** Full conversational history with one-click neural context reset.
- **Full-Stack & Production-Ready:** Clean separation of client and backend API proxy to keep API keys secure.

---

## 🚀 Quick Start (Local Development)

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/v-personal-ai-assistant.git
cd v-personal-ai-assistant
```

### 2. Install dependencies
```bash
npm install
```

### 3. Configure your API key
Create a `.env` file in the root directory:
```bash
cp .env.example .env
```

Open `.env` and insert your Gemini API Key from [Google AI Studio](https://aistudio.google.com/):
```env
GEMINI_API_KEY="your_actual_gemini_api_key_here"
PORT=3000
```

### 4. Start the application
```bash
npm run dev
```

Visit `http://localhost:3000` in your browser.

---

## 🌐 Deploying Live from GitHub

### Option A: Free 1-Click Cloud Deployment (Render / Railway / Koyeb)

1. Push this repository to your GitHub account:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of V AI Assistant"
   git branch -M main
   git remote add origin https://github.com/<your-username>/v-personal-ai-assistant.git
   git push -u origin main
   ```
2. Go to [Render](https://render.com) (or Railway / Koyeb):
   - Click **New Web Service** and select your GitHub repository.
   - The included `render.yaml` automatically sets:
     - **Build Command:** `npm install && npm run build`
     - **Start Command:** `npm start`
   - In the **Environment Variables** section, set:
     - `GEMINI_API_KEY`: *Your Google AI Studio Gemini API Key*
3. Click **Deploy**. Your assistant will be live with full API capabilities!

---

### Option B: GitHub Pages (Frontend Hosting with GitHub Actions)

This repository includes a preconfigured GitHub Actions workflow at [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

1. Push your code to your GitHub repository.
2. In your GitHub repository settings:
   - Navigate to **Settings** > **Pages**.
   - Under **Build and deployment** > **Source**, choose **GitHub Actions**.
3. Push any commit to `main`, and GitHub Actions will automatically compile and deploy your web app to `https://<your-username>.github.io/<repository-name>/`.

---

### Option C: Docker Deployment

Run with Docker anywhere:
```bash
docker build -t v-assistant .
docker run -p 3000:3000 -e GEMINI_API_KEY="your_api_key" v-assistant
```

---

## 📁 Project Architecture

```
├── .github/
│   └── workflows/
│       └── deploy.yml        # GitHub Actions workflow for automated deployments
├── public/                   # Static icons and assets
├── src/
│   ├── components/
│   │   ├── ChatStream.tsx      # Message feed, status badges, telemetry & retry button
│   │   ├── InputConsole.tsx    # Futuristic command line input & context reset
│   │   ├── QuickPrompts.tsx    # One-click starter prompts
│   │   └── VCoreAnimation.tsx  # Dynamic holographic core visualization
│   ├── App.tsx               # Main application orchestration & state management
│   ├── index.css             # Tailwind CSS entry point & custom animations
│   ├── main.tsx              # React DOM mounting
│   └── types.ts              # System types and interfaces
├── server.ts                 # Full-stack Express server with Gemini API proxy
├── vite.config.ts            # Vite configuration with relative asset paths
├── package.json              # NPM dependencies & scripts
├── render.yaml               # 1-click cloud deployment blueprint
├── Dockerfile                # Containerized deployment spec
└── README.md                 # Project documentation
```

---

## 🛠 Tech Stack

- **Frontend Framework:** React 19
- **Build Tool:** Vite
- **Styling:** Tailwind CSS v4
- **Language:** TypeScript
- **AI Engine:** `@google/genai` (Google Gemini API)
- **Icons:** Lucide React
- **Animations:** Custom CSS 3D keyframe animations & Tailwind utility classes

---

## 📄 License

Apache-2.0. Feel free to fork, customize, and build your own autonomous assistant!
