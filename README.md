# ⚡ AI Resume & Portfolio Builder

An AI-powered Flask web app that generates:
- **Resume** (ATS-optimized `.docx`)
- **Cover Letter** (professional `.docx`)
- **Portfolio Website** (single-page `.html`)

All bundled as a **ZIP download** — powered by **Llama-3.1-8B-Instruct** via HuggingFace Free Inference API.

---

## 📁 Project Structure

```
resume_builder/
├── app.py               ← Flask backend (all AI + DOCX + HTML logic)
├── requirements.txt     ← Python dependencies
├── .env.example         ← Template for your secret token
├── .gitignore           ← Keeps .env safe from GitHub
├── README.md
└── templates/
    └── index.html       ← 8-step form frontend
```

---

## 🚀 Setup & Run

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Set up your HuggingFace token
```bash
# Copy the example file
cp .env.example .env
```
Then open `.env` and replace the placeholder with your real token:
```
HF_TOKEN=hf_your_actual_token_here
```

### 3. Run the app
```bash
python app.py
```

### 4. Open in browser
```
http://localhost:5000
```

---

## 🔑 HuggingFace Token (Free)

1. Go to [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens)
2. Click **New Token** → select **Read** access → copy it
3. Paste into your `.env` file

> ✅ Your token stays in `.env` which is listed in `.gitignore` — it will NEVER be uploaded to GitHub.

---

## 🌐 Deploying to Render (Free Live Link)

1. Push your code to GitHub (`.env` will NOT be uploaded thanks to `.gitignore`)
2. Go to [render.com](https://render.com) → New Web Service
3. Connect your GitHub repo
4. Set:
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `python app.py`
5. Go to **Environment** tab → Add variable:
   - Key: `HF_TOKEN` | Value: `hf_your_token`
6. Deploy → get your live link ✅

---

## ✨ Features

| Feature | Details |
|---------|---------|
| 📄 Resume (DOCX) | ATS-friendly — Summary, Education (dual degree), Skills, Projects, Experience, Certs |
| ✉️ Cover Letter (DOCX) | Formal 3-paragraph letter |
| 🌐 Portfolio (HTML) | Responsive dark-themed single-page website |
| 🎯 JD Tailoring | Paste a Job Description → AI tailors keywords for ATS |
| 🎓 Dual Degree | Add both Bachelor's and Master's degree |
| 🌱 Fresher Mode | Experience section auto-hides |
| 🔐 Secure | Token stored in .env, never hardcoded |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python 3.8+ / Flask |
| AI | Llama-3.1-8B-Instruct via HuggingFace Router API |
| Document Generation | python-docx |
| Config | python-dotenv |
| Frontend | HTML5 / CSS3 / Vanilla JS |


## Deployment Link

https://ai-resume-and-portfolio-builder.onrender.com
