# Chatternel

**A clean, mobile-first chat interface for LLMs via [OpenRouter](https://openrouter.ai).**

→ **[Try it live](https://noniv.github.io/Chatternel/)**

---

Chatternel is a single HTML file you can open in any browser — no installation, no account, no backend. Your API key lives in your browser's local storage and goes nowhere except directly to OpenRouter's API.

---

## Features

### Multiple Conversations
Keep as many conversations going as you want. Each one has its own title (auto-set from your first message, tap to rename), timestamp, and full message history. Switch between them instantly from the home screen.

### Any Model on OpenRouter
Type in any model ID available on OpenRouter — Claude, GPT-4o, Llama, Mistral, Gemma, DeepSeek, and hundreds more. The active model is always visible as a chip in the chat header.

### Streaming Responses
Responses stream in token by token as they're generated, so you're never staring at a blank screen waiting.

### Extended Thinking / Reasoning
For models that support it (Claude, DeepSeek R1, etc.), you can enable reasoning output. Choose an effort level (low / medium / high / max) or set an exact token budget. Reasoning traces are shown in a collapsible block above the response so they stay out of the way until you want them.

### Full Message Control

- **Edit user messages** — tap EDIT on any message you sent, modify it, and the conversation reruns from that point.
- **Edit AI responses** — tap EDIT on any assistant message to correct or adjust it in place without triggering a regeneration.
- **Regenerate** — tap ↺ REDO on any AI response to get an alternative. Flick through all alternatives with ‹ › arrows.

### Code Blocks
Fenced code in responses is rendered as a proper code block with a language label and a one-tap **COPY** button. Inline code is styled separately. All rendering happens client-side with no external libraries.

### Conversation Summarisation
When a long conversation starts eating into your context window, hit **✦ Summarise Conversation** in settings. The flow:

1. Review (and optionally edit) the summarisation prompt.
2. The current conversation — plus any existing summary — is sent to the model, which produces one consolidated summary.
3. Review and edit the result, then confirm.

On confirmation the conversation is trimmed to its last 2 messages, and the summary is stored as a separate field on the conversation. It's automatically injected at the end of your system prompt on every subsequent request, and fed back as prior context the next time you summarise — so you can repeat this as many times as you like without your system prompt growing unboundedly or summaries contradicting each other.

The summary is always visible as a **✦ SUMMARY** chip in the chat header when one exists. Tap it to view, edit, or clear it at any time.

### Fully Configurable

| Setting | Details |
|---|---|
| System prompt | Per-session, editable at any time |
| Temperature | 0 – 2 slider |
| Top-P | 0 – 1 slider |
| Provider pin | Lock requests to a specific OpenRouter provider |
| Strict mode | Error instead of falling back to another provider |
| Reasoning effort | Low / Med / High / Max, or exact token budget |
| Hide reasoning | Strip reasoning from the API response entirely |

### Data Stays Yours

- **Export** the entire app state (all conversations + settings) as a JSON file at any time.
- **Import** it back on any device or browser.
- Nothing is ever sent to a server other than OpenRouter's API endpoint.

### Mobile-First
The layout is built for phones. The home and chat screens slide in and out with native-feeling transitions. Swipe right from the left edge to go back. Safe-area insets are respected on iOS. The input field grows as you type and stops at a sensible maximum height.

---

## Getting Started

1. Open [noniv.github.io/Chatternel](https://noniv.github.io/Chatternel/)
2. Tap the ⚙ settings icon and paste your [OpenRouter API key](https://openrouter.ai/keys)
3. Optionally change the model ID (default: `anthropic/claude-opus-4`)
4. Tap **Save Settings**, then **New Chat**

That's it.

---

## Privacy

Chatternel has no backend, no analytics, no telemetry, and no accounts. The only network requests the app makes are:

- `fonts.googleapis.com` — to load Roboto and Roboto Mono
- `openrouter.ai/api/v1/chat/completions` — your actual chat requests

Your API key is stored in `localStorage` in your own browser. It is sent only in the `Authorization` header of your chat requests, directly to OpenRouter.
