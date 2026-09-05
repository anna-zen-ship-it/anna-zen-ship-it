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
  
