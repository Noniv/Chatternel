# Chatternel

**A private, fully client-side frontend for OpenRouter LLMs.**

Chatternel is a lightweight, single-file HTML application that lets you chat with any model available on OpenRouter directly from your browser. No backend, no databases, no tracking—just you and the model.

🌐 **Try it live:** [chatternel.com](https://chatternel.com)

---

### ✨ Key Features

- **100% Private & Client-Side:** Your API key and chat history are stored locally in your browser. Nothing is sent to any server except OpenRouter.
- **Single File App:** The entire application is contained in one `index.html` file. No build steps, no dependencies. Just open it and go.
- **Full Model Control:**
  - Choose any model via its ID (e.g., `anthropic/claude-opus-4`).
  - Pin requests to a specific provider (e.g., `DeepInfra`, `Together`).
  - Adjust the `temperature` to control creativity.
  - Modify `top_p` to control diversity via nucleus sampling.
  - Set a custom `System Prompt`.
- **Reasoning Support:**
  - Control the reasoning effort (`MIN`, `LOW`, `MED`, `HIGH`, `MAX`) or set an exact token budget.
  - View the model's reasoning process above the response, or exclude it entirely.
- **Conversation Management:**
  - **Multiple Chats:** Keep several conversations going at once.
  - **Edit History:** Modify your past messages from any point and branch the conversation.
  - **Regenerate:** Don't like an answer? One click regenerates the response.
  - **Edit Titles:** Rename your chats to keep them organized.
- **Data Portability:**
  - Export your entire app state (settings + all conversations) to a JSON file.
  - Import the JSON file on any other device to seamlessly pick up where you left off.

---

### 🚀 Getting Started

1.  **Get an API Key:** If you don't have one, sign up at [OpenRouter](https://openrouter.ai/) and create an API key.
2.  **Open Chatternel:** Go to [chatternel.com](https://chatternel.com) or open the `index.html` file locally.
3.  **Configure Settings:** Tap the settings gear icon in the top right.
4.  **Enter API Key:** Paste your OpenRouter API key (`sk-or-v1-...`). It is stored only in your browser's local storage.
5.  **Choose Model:** Enter the Model ID you want to use (e.g., `openai/gpt-4o`).
6.  **Start Chatting:** Click "New Chat" and start messaging!

---

<details>
<summary><b>⚙️ Advanced Configuration</b></summary>

You can fine-tune the model behavior in the settings panel:

*   **Provider Pinning:** Force OpenRouter to use a specific provider (e.g., `Together`). You can enable "Strict" mode to error out if that provider is unavailable, preventing fallbacks.
*   **Reasoning:**
    *   Use the effort buttons (`MIN` to `MAX`) to let the model decide how hard to think.
    *   Alternatively, specify an exact `Token budget` (e.g., `4000`).
    *   Toggle **Hide reasoning** to exclude the thought process from the API response entirely (if you only want the final answer).
*   **Temperature & Top P:**
    *   **Temperature:** Use the slider to adjust randomness. Higher values (e.g., `1.5`) are more creative; lower values (e.g., `0.2`) are more deterministic.
    *   **Top P:** Use the slider for nucleus sampling. `1.0` considers all tokens, while lower values like `0.9` restrict the model to the most probable tokens. *Note: OpenAI recommends altering either Temperature or Top P, but not both.*

</details>

<details>
<summary><b>💾 Backup & Sync Between Devices</b></summary>

Since Chatternel runs entirely in your browser, your data doesn't automatically sync to the cloud. You can move your data manually:

1.  Open Settings.
2.  Click **⬇ Export JSON**. This will download a file named `chatternel-backup-YYYY-MM-DD.json`.
3.  On your other device, open Chatternel and go to Settings.
4.  Click **⬆ Import JSON** and select the file you downloaded.

*Note: Importing will overwrite the current data on the target device.*

</details>

---

### ❓ FAQ

**Is my API key safe?**
Yes. The key is stored in your browser's `localStorage` and is only sent directly to OpenRouter's API. It never passes through our servers.

**Can I use this on mobile?**
Yes! Chatternel is designed to be responsive and works great on mobile browsers. It also supports "Add to Home Screen" for an app-like experience.