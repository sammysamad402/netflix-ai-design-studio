# 🎬 Netflix AI Design Studio

> **Course-End Project** — Creating Designs by Leveraging OpenAI & Gradio UI

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/netflix-ai-design-studio/blob/main/Netflix_AI_Design_Studio.ipynb)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://python.org)
[![Gradio](https://img.shields.io/badge/Gradio-4.x-orange?logo=gradio)](https://gradio.app)
[![OpenAI](https://img.shields.io/badge/OpenAI-DALL--E%203-green?logo=openai)](https://openai.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📸 Preview

A Netflix-branded AI image generation platform that converts text prompts into cinematic banners and posters using **OpenAI DALL-E 3** and **Gradio UI**.

```
User Prompt ──► Prompt Enhancer ──► DALL-E 3 API ──► PIL Image ──► Gradio Output
```

---

## ✨ Features

| Feature | Details |
|---------|---------|
| 🎨 **7 Style Presets** | Netflix Cinematic, Neo-Noir, Sci-Fi, Fantasy, Romance, Comedy, Minimalist |
| 📐 **3 Output Sizes** | Vertical Poster (1024×1792), Horizontal Banner (1792×1024), Square (1024×1024) |
| ⚡ **Quality Modes** | Standard (faster) and HD (highest quality) |
| 💾 **One-click Download** | Built into the Gradio image output component |
| 🌐 **Public Sharing** | Auto-generates a 72-hour public Gradio link |
| 🔒 **Secure API Key** | Colab Secrets → Env Var → getpass (never hardcoded) |
| 💡 **6 Example Prompts** | Pre-loaded Netflix campaign scenarios |

---

## 🚀 Quick Start (Google Colab)

### Option A — One-click (Recommended)

Click the badge above: **Open in Colab** → Run All Cells.

### Option B — Manual

1. Upload `Netflix_AI_Design_Studio.ipynb` to [colab.research.google.com](https://colab.research.google.com)
2. Add your OpenAI API key to **Colab Secrets**:
   - Click the 🔑 key icon in the left sidebar
   - Add secret: **Name** = `OPENAI_API_KEY` | **Value** = `sk-...`
3. Run all cells (`Runtime → Run all`)
4. Click the generated `https://xxxx.gradio.live` link

---

## 🔑 API Key Setup

The notebook uses a **3-tier secure fallback**:

```
1. Google Colab Secrets  →  Key name: OPENAI_API_KEY  (recommended)
2. Environment variable  →  export OPENAI_API_KEY=sk-...
3. getpass prompt        →  Masked manual entry (not stored)
```

> **Get an API key:** [platform.openai.com/api-keys](https://platform.openai.com/api-keys)

---

## 📁 Project Structure

```
netflix-ai-design-studio/
│
├── Netflix_AI_Design_Studio.ipynb   ← Main notebook (run this)
├── requirements.txt                  ← Python dependencies
├── .env.example                      ← Environment variable template
├── .gitignore                        ← Prevents key/cache leaks
├── LICENSE                           ← MIT License
└── README.md                         ← This file
```

---

## 📦 Dependencies

```txt
openai>=1.30.0
gradio>=4.0.0
pillow>=10.0.0
requests>=2.31.0
```

Install manually:
```bash
pip install openai gradio pillow requests
```

---

## 💰 OpenAI DALL-E 3 Pricing

| Quality | Size | Cost per Image |
|---------|------|---------------|
| Standard | 1024×1024 | ~$0.040 |
| Standard | 1792×1024 / 1024×1792 | ~$0.080 |
| HD | 1024×1024 | ~$0.080 |
| HD | 1792×1024 / 1024×1792 | ~$0.120 |

Monitor usage: [platform.openai.com/usage](https://platform.openai.com/usage)

---

## 🏗️ Architecture

```python
# Core function signature
def generate_image(
    prompt      : str,    # User's creative description
    style_key   : str,    # Style preset (e.g. "🎬 Netflix Original")
    size_key    : str,    # Output size (e.g. "🖼️ Poster (1024×1792)")
    quality_key : str,    # Quality tier ("Standard" or "HD")
) -> tuple[PIL.Image, str]:
    ...
```

**Prompt Enhancement Pipeline:**
1. User writes a short creative prompt
2. `build_enhanced_prompt()` appends a style-specific professional suffix
3. DALL-E 3 receives the enriched prompt
4. The returned URL is fetched and converted to a PIL Image
5. Gradio displays it with a download button

---

## 🔒 Security & GitHub Safety

- ✅ API key **never hardcoded** in source
- ✅ `.gitignore` excludes `.env`, `*.jpg`, `samples/`, Jupyter checkpoints
- ✅ `.env.example` is a safe template (no real values)
- ✅ `getpass` used for fallback entry (masks input)

---

## 🧪 Running Tests

The notebook includes a **Step 6: Backend Test Cell** that:
- Calls `generate_image()` directly without the UI
- Saves the output to `samples/test_output_<timestamp>.jpg`
- Displays the image inline in Colab

---

## 📋 Course Information

| Item | Detail |
|------|--------|
| **Project** | Course-End Project |
| **Topic** | Creating Designs by Leveraging OpenAI & Gradio UI |
| **Scenario** | Netflix campaign creative design platform |
| **Deliverable** | Jupyter Notebook (.ipynb) |

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙏 Acknowledgements

- [OpenAI DALL-E 3](https://openai.com/dall-e-3) — Image generation model
- [Gradio](https://gradio.app) — Web UI framework
- [Pillow](https://python-pillow.org) — Image processing library
