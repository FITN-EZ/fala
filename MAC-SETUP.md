# Run Bia on your Mac (free, no API key)

Your phone talks to an AI model running on your Mac through Tailscale, a private network between your own devices. This works at home or out, as long as the Mac is awake and online.

## 1. Ollama (the model runner)
1. Install Ollama from ollama.com and open it.
2. Download a model. Pick by your Mac's memory:
   - 16 GB: `ollama pull gemma3:12b`
   - 8 GB: `ollama pull gemma3:4b` (noticeably weaker Portuguese)
   - 32 GB or more: try a larger model from the Ollama library
3. Allow the app to call it. Replace YOUR-USERNAME:
   `launchctl setenv OLLAMA_ORIGINS "https://YOUR-USERNAME.github.io"`
   then quit and reopen Ollama.

## 2. Tailscale (secure HTTPS link)
1. Install Tailscale on the Mac and on your phone, signed into the same account.
2. In the Tailscale admin console > DNS, turn on MagicDNS and HTTPS certificates.
3. On the Mac: `tailscale serve --bg 11434`
   It prints an address like https://your-mac.tailXXXX.ts.net. That's your Mac address.
   (Use `serve`, not `funnel`. Funnel makes it public.)

## 3. In Fala
Progresso > Settings > AI for Bia > My Mac (Ollama). Paste the address and the model name, tap Test, then Save.

## Keep the Mac awake
System Settings > Energy (or Battery) > prevent automatic sleeping when the display is off, while plugged in.
