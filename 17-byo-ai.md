---
id: pg-docs-byo-ai
title: BYO-AI Integration (Bring Your Own AI) 🤖
icon: 🤖
tags: [ai, byo-ai, ollama, colab, groq, openrouter, deepseek, local-first]
createdAtDaysAgo: 60
updatedAtDaysAgo: 0
---

> 💡 **Doction never sells proprietary AI tokens.** With our **BYO-AI (Bring Your Own AI)** architecture, you maintain 100% data sovereignty. Connect your own free Google Colab GPU tunnel, local offline models (Ollama, LM Studio), or Cloud API keys (Groq, OpenRouter, DeepSeek, Google Gemini, OpenAI).

---

## 1. Zero-Bloat Architecture

By default, the AI Integration plugin is **disabled (`false`)**. When disabled, it consumes **0 MB RAM**, registers no background processes, and incurs zero network traffic.

To activate:
1. Open **Settings ⚙️** → **Plugins & Extensions**.
2. Toggle on the **AI Assistant (BYO-AI)** plugin.
3. A dedicated **AI Setup** tab immediately unlocks in Settings under Workspace.

---

## 2. Three Flexible AI Provider Categories

Doction standardizes all AI communication on the universal OpenAI `/v1/chat/completions` and `/v1/models` protocol:

### 1. ⚡ Google Colab GPU Tunnel
- Run massive open-weight models (Llama 3, Qwen 2.5, DeepSeek R1, Mistral) on Google Colab's free T4/A100 cloud GPUs.
- Expose the running model with a single-line Cloudflare Tunnel (`cloudflared tunnel --url http://localhost:11434`).
- Paste the `trycloudflare.com` URL into **AI Setup** → **Google Colab Tunnel**.

### 2. 🦙 Local Offline AI (Ollama / LM Studio)
- **100% Offline & Zero Latency:** Not a single token leaves your local device.
- Select your engine preset: **Ollama** (`:11434`), **LM Studio** (`:1234`), or **Custom Local** (`:8000`).
- *Browser CORS Tip:* For Ollama, launch with `OLLAMA_ORIGINS="*" ollama serve` to permit browser cross-origin requests.

### 3. 🔑 Cloud API Providers
- Configure multiple API keys with 1-click presets:
  - **Groq Cloud:** Ultra-fast ~500 tokens/sec inference with free tier open models.
  - **OpenRouter:** Access DeepSeek R1, Claude 3.5, and 200+ models with unified routing.
  - **DeepSeek API:** State-of-the-art coding and reasoning at ultra-low token cost.
  - **Google Gemini:** Large-context Gemini models via official OpenAI-compatible endpoint.
  - **OpenAI:** GPT-4o and GPT-4o-mini direct endpoints.
  - **LiteLLM / Custom Proxy:** Corporate gateway or self-hosted proxy.

---

## 3. Free Live Model Discovery & Sticky DB Persistence

Every OpenAI-compatible endpoint supports a free `GET /v1/models` call:
1. Enter your URL and API Key in **AI Setup**.
2. Click **Test & Fetch** or **Fetch Live**.
3. Doction contacts the endpoint for free and dynamically populates all available models in the dropdown.
4. Your chosen model is saved **permanently in local IndexedDB**. It will never reset or change unless you deliberately pick another one.

---

## 4. In-Editor Slash Commands

Whenever the AI plugin is active, you can invoke your chosen AI right from the document editor:

| Command | Action |
| :--- | :--- |
| `/ai_create` | Draft full specifications, articles, outlines, or code examples from a prompt. |
| `/ai_summary` | Summarize the entire document into executive bullet points and key takeaways. |
| `/ai_explain` | Explain complex terminology, selected text, code snippets, or architectural concepts. |

---

## 5. Live Typewriter Preview & In-Modal Switcher

Running any AI command opens the interactive **AI Generation Preview Modal**:
- **In-Modal Provider Switcher:** Switch between Colab, Local Ollama, or Cloud APIs directly inside the modal without leaving your writing flow.
- **Real-Time SSE Streaming:** Live typewriter streaming with token-by-token visual feedback.
- **1-Click Insertion:** Click **Insert into Document** to drop the formatted markdown directly at your active cursor position.
