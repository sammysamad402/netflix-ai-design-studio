# 🎬 Netflix AI Design Studio

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)
![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Gradio](https://img.shields.io/badge/Gradio-UI-orange)
![OpenAI](https://img.shields.io/badge/OpenAI-gpt--image--1-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A Netflix-inspired AI creative platform built with **Python**, **Gradio**, and **OpenAI's GPT Image Generation API (`gpt-image-1`)**. The application enables users to create professional Netflix-style posters, banners, and promotional artwork through an intuitive dark-themed interface.

---

# 🚀 Preview

Netflix AI Design Studio combines a modern Gradio interface with OpenAI image generation capabilities to create high-quality branded assets.

## Architecture

```text
┌──────────────────────┐
│      User Prompt     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   Gradio Interface   │
│ Netflix-Inspired UI  │
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
│  Pillow Processing   │
│ Resize & Formatting  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ samples/ Auto Save   │
│ Timestamped Outputs  │
└──────────────────────┘
```

---

# ✨ Features

| Feature                     | Description                                       |
| --------------------------- | ------------------------------------------------- |
| 🎨 Netflix-Themed Interface | Dark mode UI with Netflix-inspired styling        |
| 🤖 AI Image Generation      | Powered by OpenAI `gpt-image-1`                   |
| 🎭 7 Style Presets          | Multiple artistic and cinematic generation styles |
| 📐 Multiple Output Sizes    | Poster, Banner, and Square formats                |
| ⚡ Quality Selection         | Medium and High quality generation                |
| 🔐 Secure API Management    | No hardcoded API keys                             |
| ☁️ Google Colab Compatible  | Designed for seamless Colab deployment            |
| 💾 Auto Save System         | Automatically stores generated images             |
| 🕒 Timestamped Filenames    | Prevents accidental overwriting                   |
| 🌐 Gradio Web Interface     | Browser-based user experience                     |

---

# ⚙️ Quick Start

## Option A — Google Colab (Recommended)

### 1. Open the Notebook

Upload or open `Netflix_AI_Design_Studio.ipynb` in Google Colab.

### 2. Install Dependencies

Run all setup cells.

### 3. Configure API Access

Provide your OpenAI API key using one of the supported secure methods.

### 4. Launch the App

Run the notebook and access the generated Gradio URL.

### 5. Generate Images

Enter a prompt, choose style settings, and create Netflix-style artwork.

---

## Option B — Manual Local Setup

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

### Create Environment File

```env
OPENAI_API_KEY=your_api_key_here
```

### Run the Notebook

Open and execute:

```text
Netflix_AI_Design_Studio.ipynb
```

---

# 🔒 Security & API Setup

Netflix AI Design Studio implements a secure **3-Tier API Key Retrieval System**.

## Priority Order

| Priority | Source                                   |
| -------- | ---------------------------------------- |
| 1️⃣      | Google Colab Secrets                     |
| 2️⃣      | Environment Variables (`OPENAI_API_KEY`) |
| 3️⃣      | Secure Getpass Prompt                    |

## Security Workflow

```text
Colab Secret Found?
        │
       Yes
        ▼
 Use Secret
        │
       No
        ▼
Environment Variable Found?
        │
       Yes
        ▼
Use OPENAI_API_KEY
        │
       No
        ▼
Prompt User via getpass()
```

### Benefits

* No hardcoded credentials
* Safe for public repositories
* Supports Colab deployments
* Prevents accidental API key exposure
* Follows security best practices

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
│   └── generated_images/
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

Install all project requirements:

```bash
pip install -r requirements.txt
```

### Core Technologies

| Package       | Purpose                         |
| ------------- | ------------------------------- |
| openai        | Image generation API            |
| gradio        | User interface                  |
| Pillow        | Image processing                |
| python-dotenv | Environment variable management |

---

# 💰 Estimated GPT-Image-1 Usage Costs

> Actual pricing depends on OpenAI's latest pricing model and image settings.

| Usage Type        | Images / Day | Estimated Monthly Cost   |
| ----------------- | ------------ | ------------------------ |
| Testing           | 5–20         | Low                      |
| Personal Projects | 20–100       | Moderate                 |
| Content Creation  | 100–500      | Medium–High              |
| Production Usage  | 500+         | Based on API consumption |

## Cost Factors

* Image resolution
* Quality setting
* Number of generations
* OpenAI pricing updates

For the latest pricing, refer to OpenAI's official pricing documentation.

---

# 🛡️ GitHub Safety

This repository includes a `.gitignore` file to prevent sensitive files from being uploaded.

## Recommended Exclusions

```gitignore
.env
.env.local
__pycache__/
.ipynb_checkpoints/
samples/
*.pyc
*.log
```

## Best Practices

* Never commit API keys
* Use `.env.example` for configuration templates
* Keep generated images outside version control
* Review commits before pushing
* Rotate compromised keys immediately

---

# 🙏 Acknowledgements

This project was built using:

* OpenAI GPT Image Generation (`gpt-image-1`)
* Gradio
* Pillow
* Python
* Google Colab

Special thanks to the open-source community for providing the tools that make rapid AI application development possible.

---

# 📜 License

Licensed under the MIT License.

See the `LICENSE` file for additional information.

---

⭐ If you found this project helpful, consider starring the repository:

https://github.com/sammysamad402/netflix-ai-design-studio
