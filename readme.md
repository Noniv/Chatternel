# ✨ Chatternel

**A lightweight, fast, single-file chat client for OpenRouter — built to get out of your way.**

🔗 **[Launch Chatternel →](https://noniv.github.io/Chatternel/)**

No install. No account. No backend. Bring your own OpenRouter API key, pick a model, and start talking. Your entire chat history lives in your browser — Chatternel never sees it, and neither does anyone else.

---

## 🪶 Why Chatternel

Most chat frontends today try to be everything at once — plugins, workspaces, dashboards, sync layers — and end up feeling heavy before you've typed a single word. Chatternel is the opposite bet: **one HTML file, zero dependencies to install, and every feature earns its place.** It opens instantly, feels instantly familiar, and stays out of the way while you think.

If you just want a clean, quick, no-nonsense window into any model on OpenRouter — this is it.

---

## 💬 Core Chat Experience

- **🌐 Talk to any OpenRouter model** — Claude, GPT, Gemini, Llama, Mistral, DeepSeek, and hundreds more. Just paste a model ID.
- **⚡ Real-time streaming** — responses render token-by-token with a smooth, throttled renderer that stays buttery even on long, code-heavy replies.
- **🧠 Reasoning model support** — see a model's chain-of-thought in a clean, collapsible panel, separate from its final answer. Works with native `reasoning` fields *and* `<think>` tag models.
- **🎛️ Full sampling control** — temperature, top-p, and reasoning effort (from `AUTO` all the way to `MAX`), or dial in an exact reasoning token budget. Nothing is sent to OpenRouter unless you've actually changed it from the default — your requests stay minimal and predictable.
- **🔀 Provider pinning** — lock a model to a specific provider (e.g. only run Llama through Fireworks) with optional strict mode if you don't want silent fallbacks.
- **✍️ Markdown rendering** — bold, italics, inline code, and fenced code blocks with syntax labels and one-tap **copy** buttons.

---

## 🗂️ Conversation Management

- **📚 Unlimited local conversations** — organized in a clean home list, most recent first.
- **✏️ Editable titles** — rename any chat inline.
- **🔁 Regenerate & branch replies** — not happy with an answer? Regenerate it and flip between alternatives with a simple `1/3` counter, without losing the earlier version.
- **📝 Edit any message** — yours or the assistant's — and continue the conversation from there.
- **➕ Continue mode** — no new message to send? Hit continue and let the model keep going.
- **✦ Smart summarization** — condense a long conversation into a compact summary (with your own custom prompt) that's quietly appended to context going forward, while the raw transcript stays trimmed and readable.

---

## 🎨 An Interface That Respects Your Eyes

- **📱 Mobile-first, desktop-perfected** — a snappy swipe-to-go-back gesture on mobile, and a centered, comfortably-wide reading column on desktop instead of text stretched edge-to-edge across your monitor.
- **🔠 Genuinely readable type** — no squinting at 9px labels. Text sizes were tuned throughout for comfortable reading, including for users with limited vision.
- **🌙 Easy on the eyes** — a warm, low-glare dark theme designed for long sessions.
- **🧭 Calm scrolling** — the transcript doesn't fight you. It won't yank you back down while you're scrolling up to reread something mid-response, and a small **jump to bottom ↓** button appears whenever you've wandered away from the latest message.
- **🫧 Clear generation state** — a lightweight typing indicator while the model is thinking, and a visible stop button to cancel anytime.

---

## 🔒 Privacy & Data Ownership

- **💾 Everything stored locally** — conversations, settings, and your API key live in your browser's local storage. Nothing touches a third-party server except OpenRouter itself.
- **🔑 Your key, your control** — entered once, stored only on your device, sent only to OpenRouter.
- **📤 Export / 📥 Import** — back up your entire chat history (and settings) to a single JSON file, or restore it on another device. Full portability, zero lock-in.

---

## 🚀 Getting Started

1. Open **[noniv.github.io/Chatternel](https://noniv.github.io/Chatternel/)**
2. Tap ⚙️ **Settings** and paste your [OpenRouter API key](https://openrouter.ai/keys)
3. Set a model ID (e.g. `anthropic/claude-opus-4`, `openai/gpt-4o`, `deepseek/deepseek-r1`)
4. Hit **New Chat** and start talking 🎉

That's it — no build step, no sign-up, no waiting room.

---

## 🛠️ Built With

Just HTML, CSS, and vanilla JavaScript. One file. No frameworks, no bundlers, no npm install. Fork it, self-host it, or tweak it to taste — it's designed to be read as easily as it's used.

---

*Chatternel — chat, uncluttered.* 🪶