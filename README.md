## Ollama Web Manager ✨

Simplify your Ollama workflow! This is a convenient, browser-based UI for managing your local Ollama AI server without needing complex installations or command-line juggling. Everything is packed into a **single HTML file**.

![Main Interface Screenshot](https://github.com/user-attachments/assets/4f49e47e-f489-4b1f-b47d-3b6ea3d986c7)

**Packed into this one page, you can easily:**

*   👀 **View Models:** See all your downloaded models at a glance, including size, family, and parameters.
*   📥 **Pull Models:** Download new models directly from the Ollama registry (with progress!).
*   🗑️ **Delete Models:** Clean up models you no longer need.
*   📝 **Create Models:** Write Modelfiles with syntax highlighting and create new custom models.
*   ✂️ **Edit Modelfiles:** Load an existing model's Modelfile, tweak it, and save it as a *new* model.
*   💬 **Chat:** Interact conversationally with any of your models.
*   ✍️ **Generate:** Perform simple text generation with options for temperature, seed, etc.
*   🔬 **Get Embeddings:** Generate text embeddings using your models.
*   ☀️/🌙 **Theme Toggle:** Switch between light and dark modes.

![Chat Interface Screenshot](https://github.com/user-attachments/assets/0579baef-5f4a-47fb-82b7-b642b242c5a6)

### 🚀 Getting Started

Because this tool runs in your browser, there are a couple of ways to use it, especially when connecting to your *own* computer (`localhost`).

**1. Easiest Way (Connecting to `localhost`): Download & Run Locally**

This method avoids most browser security restrictions when connecting to your own machine.

*   **Download the File:** Click here to **[Download `index.html`](https://raw.githubusercontent.com/MillionthOdin16/Ollama-Web-Manager/main/index.html)** (Right-click the link -> "Save Link As..." if needed).
*   **Open Locally:** Just double-click the downloaded `index.html` file to open it in your browser.
*   **Connect:** Use the default `http://localhost:11434` URL (or your Ollama server's local IP if different). It should connect without needing any changes to your Ollama server setup!

**2. Alternative: Use the Live Version (Needs Ollama Config for `localhost`)**

You can try the manager directly online, but **connecting to `localhost` requires a one-time Ollama server configuration** due to browser security (CORS).

*   **Live Link:** **[https://millionthodin16.github.io/Ollama-Web-Manager/](https://millionthodin16.github.io/Ollama-Web-Manager/)** *(Make sure this link is correct!)*
*   **If Connecting to `localhost` from the live link:** You *must* tell Ollama to allow requests from this website.
    *   Stop your Ollama server.
    *   Restart it with the `OLLAMA_ORIGINS` environment variable set. The manager itself includes detailed instructions in the "Connection" section, but a common command is:
        ```bash
        # Allow this specific site + common local addresses (Recommended)
        OLLAMA_ORIGINS=https://millionthodin16.github.io,http://localhost:*,http://127.0.0.1:* ollama serve
        ```
        *(Replace the URL if needed. Using `OLLAMA_ORIGINS=*` also works but is less secure.)*

### How It Works

This tool is built with vanilla HTML, CSS, and JavaScript, using only the CodeMirror library (fetched via CDN) for syntax highlighting. No build steps, no frameworks, just a single file interacting directly with the Ollama API.

![Model Manager Screenshot](https://github.com/user-attachments/assets/4d73b5a8-81de-418d-a871-52e83293e9e4)

### Contributing

Found a bug or have an idea? Feel free to [open an issue](https://github.com/MillionthOdin16/Ollama-Web-Manager/issues)! Pull requests are also welcome.
