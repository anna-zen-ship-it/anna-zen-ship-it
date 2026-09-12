# My GG Projects

🍵 Experimental creative sandbox — Zen-style storytelling, bilingual narration (Thai/English), and mindful visuals.  
🎬 Daily scripts, prompts, and creative notes.

---

## The Man in the Boat — Wisdom Story & TTS
[View on Google AI Studio](https://aistudio.google.com/apps/fc6eade1-c787-4bcf-b04e-514ca4b655d7?showPreview=true&showAssistant=true)  
*(Demo Mode — safe to explore 🌸)*

---

## One Fruit Per Tree — The Gift of Perfection
[View on Google AI Studio](https://ai.studio/apps/d7920665-4435-418a-ad83-9d1685972f09)  
*(Demo Mode — safe to explore 🌸)*

---

## Deployment Notes

### Root Cause
When bundling into CommonJS via esbuild (`dist/server.cjs`), `import.meta.url` is undefined.  
This caused `fileURLToPath(import.meta.url)` to throw a fatal error on Cloud Run startup.

### Resolution
- Removed `fileURLToPath(import.meta.url)` and `__filename/__dirname` from `server.ts`.
- Utilized `process.cwd()` for static file path resolution:
  ```js
  path.join(process.cwd(), 'dist')
  ---

## 🍜 The Origin of Tsukemen — Narration & TTS Story
“The unseen heart of ramen, revealed only when the soul is ready.”

An experimental narration & TTS project inspired by Kazuo Yamagishi, the God of Ramen.  
Blending Zen priest father’s warmth with cinematic audio storytelling.  

🔗 [Open Tsukemen Narration Demo](https://aistudio.google.com/apps/96b7e278-bc3b-4504-808d-ab6ed58a2b71?showAssistant=true&showPreview=true)

🌿 *This is an experimental branch of the Zen priest father repo — safe to explore, no real API calls.*
## ⚠️ Known Limitations
In AI Studio, small errors may appear:  
- Flash TTS quota reached → fallback to acoustic narration  
- WebSocket closed → hot‑reload disabled by platform  

These are natural boundaries of the demo environment,  
to be embraced lightly, without fear.  

---

🌿 *Here, every project is a step in practice.  
Errors are not obstacles, but gentle reminders:  
the path of creation is imperfect, yet alive.*
---

🌊 *A ship of ideas, sailing through limits —  
guided by calm, carried by practice, alive in imperfection.*
---

## 🎆 Hanabi — Fleeting Beauty (Chapter 01)
*A bilingual narration capturing the fleeting beauty of fireworks — mono no aware.*

🔗 [Open Hanabi Demo on Google AI Studio](https://aistudio.google.com/apps/35eb5c3a-f5b5-4e6e-b3c8-ef1e55a341bf?showPreview=true&showAssistant=true)

### Notes
- Voices: Anna (youthful, lively), Father (deep, resonant Zen tone)  
- Languages: Thai (accurate), Japanese (Tamaya! Kagiya!), English (approximate)  
- Limitation: English TTS may pronounce “Kagiya” as *Kaniya*, but Thai voice is 100% correct.  

🌿 *Fireworks bloom and fade — beauty that lives only in memory.*
