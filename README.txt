APNA AI v7 — HYBRID LOCAL + ONLINE PROTOTYPE

Features:
- Hybrid routing: short/everyday questions go to Local AI; harder/long/code/current-information questions go to Online AI when an API key is configured.
- Local model options via WebLLM/WebGPU (Llama 3.2 1B and 3B). The model must be downloaded on first use and needs a compatible browser/device, sufficient RAM/storage, and HTTPS.
- Online AI through an OpenAI-compatible /chat/completions endpoint.
- Fast streaming for online answers.
- Voice input: tap microphone, speak, and the recognized question is sent automatically.
- Voice replies with browser speech synthesis; can be turned off in Settings.
- Image generation, chat history, dark/light theme, Hindi/English preference, export, code preview.

QUICK START:
1. Extract the ZIP.
2. Host the Apna_AI folder on an HTTPS web server (WebGPU and PWA features may not work when opening index.html directly as a file).
3. Open it in Chrome on a compatible device and install/Add to Home Screen if desired.
4. Settings > Model: select Hybrid, then Download / Load Local AI. First model download can be large and may take time.
5. Settings > API: add a compatible online API key and model for difficult questions and image generation.

IMPORTANT LIMITATIONS:
- This is a web prototype, not a signed Android APK.
- Local AI only works when the browser/device supports WebGPU and has enough memory. Local answers can be weaker/slower than online models.
- Hybrid mode sends difficult questions online only if an API key is configured; otherwise it attempts local AI.
- API usage may cost money and providers can impose their own limits. The app does not add a daily message cap, but cannot remove provider/device/network limits.
- Voice replies need browser speech synthesis support.
- “Hey Apna” always-listening in the background/while the phone is locked is NOT provided by this web prototype. That requires a native Android app, microphone foreground service, persistent notification, battery/privacy handling, and may still be restricted by Android. Do not promise iPhone-Siri-level background wake behavior from a PWA.
- API keys saved in browser storage are not secure for public distribution. Production release should use a secure backend and native Android implementation (Android Studio/Capacitor).

NEW IN V8: LEARNING MEMORY + OPTIONAL COMMUNITY LEARNING
- Tap the “✦ Learn” action under an AI answer to save that Q&A to your browser's learning memory.
- Relevant saved notes are added to future prompts. This is retrieval-based memory, not automatic model-weight training.
- Settings > Prefs > Use saved learning turns this on/off. Clear learning memory deletes the saved notes.
- Community learning is opt-in. To share a note, enable sharing and press Learn; the app asks again before uploading.
- Community submissions are queued for manual review and are not shared to everyone until an administrator approves them.
- To enable community learning, host the included ../community-server on a server with HTTPS, set ADMIN_TOKEN, and put its public base URL in Settings > Prefs > Community learning server URL. Click “Sync approved community learning” to import approved notes.
- The community server is a starter template, not a hosted service. It must be deployed and maintained. Use HTTPS, set a strong ADMIN_TOKEN, review submissions for privacy and accuracy, and back up community-data.json.
- Never share personal, confidential, or identifying details. Community knowledge can be wrong; review before approval.

- Smooth animations: throttled streaming render, no re-animation of old messages, eased sidebar/modal/overlay transitions, reduced-motion support
- Icons: unified SVG icon set (header, composer, sidebar, message actions, code blocks), mic listening pulse, touch-friendly actions
- Image generation works without API key via free Pollinations fallback (rate limited; add API key for full quality)
- Claude-style theme: cream/terracotta, serif replies, card composer, Auto/Light/Dark, font/size/accent in Settings > Prefs
