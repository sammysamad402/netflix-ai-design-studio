````markdown
# 🎬 Netflix AI Design Studio

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)
![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Gradio](https://img.shields.io/badge/Gradio-UI-orange)
![OpenAI](https://img.shields.io/badge/OpenAI-gpt--image--1-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A Netflix-inspired AI creative platform built with **Python**, **Gradio**, and **OpenAI's gpt-image-1 model**. Generate high-quality Netflix-style posters, banners, and square promotional artwork through an intuitive dark-themed design studio interface.

---

# 🚀 Preview

Netflix AI Design Studio provides a streamlined workflow for creating AI-generated visual assets with customizable styles, formats, and quality settings.

### Architecture Overview

```text
┌──────────────────────┐
│      User Prompt     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   Gradio Interface   │
│ (Netflix-themed UI)  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ OpenAI gpt-image-1   │
│ Image Generation API │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│  Post Processing     │
│  (Pillow Handling)   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ samples/ Auto Save   │
│ Timestamped Outputs  │
└──────────────────────┘
````

---

# ✨ Features

| Feature                 | Description                                                   |
| ----------------------- | ------------------------------------------------------------- |
| 🎨 Netflix-Themed UI    | Professional dark interface with Netflix-inspired red accents |
| 🖼️ AI Image Generation | Powered by OpenAI's `gpt-image-1` model                       |
| 🎭 Style Presets        | 7 built-in creative style options                             |
| 📐 Multiple Formats     | Poster, Banner, and Square outputs                            |
| ⚡ Quality Selection     | Medium and High quality generation modes                      |
| 🔐 Secure API Handling  | No hardcoded API keys                                         |
| 💾 Auto Save System     | Generated images automatically saved to `samples/`            |
| 🕒 Timestamped Files    | Unique filenames prevent accidental overwrites                |
| ☁️ Google Colab Ready   | Designed for easy deployment in Colab                         |
| 🖥️ Gradio Web App      | Interactive browser-based interface                           |

---

# ⚙️ Quick Start

## Option A — One-Click Google Colab

1. Open the notebook in Google Colab.
2. Run all cells.
3. Enter your OpenAI API key using one of the supported secure methods.
4. Launch the Gradio interface.
5. Generate Netflix-style artwork instantly.

---

## Option B — Manual Setup

### Clone Repository

```bash
git clone https://github.com/sammysamad402/netflix-ai-design-studio.git

cd netflix-ai-design-studio
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment

Create a `.env` file:

```env
OPENAI_API_KEY=your_api_key_here
```

### Launch Application

Run the notebook in Jupyter or Google Colab and start the Gradio interface.

---

# 🔒 Security & API Setup

Netflix AI Design Studio uses a secure **3-tier fallback system** to retrieve API credentials.

### Priority Order

| Priority | Source                | Description                                              |
| -------- | --------------------- | -------------------------------------------------------- |
| 1️⃣      | Colab Secrets         | Recommended for Google Colab deployments                 |
| 2️⃣      | Environment Variables | Reads `OPENAI_API_KEY` from `.env` or system environment |
| 3️⃣      | Getpass Prompt        | Secure hidden terminal input if no key is found          |

### Workflow

```text
Colab Secret Available?
        │
       Yes
        ▼
Use Secret
        │
       No
        ▼
Environment Variable Available?
        │
       Yes
        ▼
Use OPENAI_API_KEY
        │
       No
        ▼
Prompt Secure Input (getpass)
```

### Security Benefits

* ✅ No hardcoded API keys
* ✅ No credential exposure in notebooks
* ✅ Compatible with public GitHub repositories
* ✅ Safe for collaborative development

---

# 📂 Project Structure

```text
netflix-ai-design-studio/
│
├── assets/
│   ├── screenshots/
│   └── branding/
│
├── samples/
│   ├── generated_20260606_183015.png
│   └── generated_20260606_184530.png
│
├── Netflix_AI_Design_Studio.ipynb
├── requirements.txt
├── .env.example
├── .gitignore
├── LICENSE
└── README.md
```

---

# 📦 Dependencies

Install all required packages:

```bash
pip install -r requirements.txt
```

### Core Libraries

| Package       | Purpose                         |
| ------------- | ------------------------------- |
| OpenAI        | Image generation API            |
| Gradio        | Interactive web interface       |
| Pillow        | Image processing                |
| python-dotenv | Environment variable management |

---

# 💰 Estimated API Pricing

> Pricing may change over time. Always refer to OpenAI's official pricing page for the latest rates.

| Usage Level          | Images/Day | Monthly Estimate        |
| -------------------- | ---------- | ----------------------- |
| Hobby Testing        | 5–20       | Low Cost                |
| Personal Projects    | 20–100     | Moderate Cost           |
| Content Creation     | 100–500    | Higher Usage            |
| Production Workloads | 500+       | Based on OpenAI Billing |

### Cost Factors

* Selected output quality
* Image dimensions
* Number of generations
* OpenAI pricing updates

---

# 🛡️ GitHub Safety

The repository includes a `.gitignore` file to prevent accidental uploads of sensitive or unnecessary files.

### Recommended Exclusions

```gitignore
.env
.env.local
__pycache__/
.ipynb_checkpoints/
samples/
*.pyc
*.log
```

### Best Practices

* Never commit API keys.
* Use `.env.example` for configuration templates.
* Keep generated assets out of version control when possible.
* Review commits before pushing to GitHub.
* Rotate exposed API keys immediately.

---

# 🙏 Acknowledgements

Built using:

* OpenAI `gpt-image-1`
* Gradio
* Pillow
* Python
* Google Colab

Special thanks to the open-source community for the tools that make rapid AI prototyping possible.

---

# 📜 License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for full details.

---

### ⭐ Support

If you find this project useful, consider starring the repository:

**[https://github.com/sammysamad402/netflix-ai-design-studio](https://github.com/sammysamad402/netflix-ai-design-studio)**

Happy Creating! 🎬✨

```
```
