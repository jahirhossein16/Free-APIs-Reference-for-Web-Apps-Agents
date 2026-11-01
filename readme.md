# Free APIs Reference for Web Apps & Agents

A curated list of free APIs by category, with links to create keys and how to use them for multiple web apps and agents. Use this to pick APIs by capability when starting new projects.

---

## Table of contents

1. [AI / LLM (chat, agents, reasoning)](#1-ai--llm-chat-agents-reasoning)
2. [Voice / Speech (STT & TTS)](#2-voice--speech-stt--tts)
3. [Image / Vision](#3-image--vision)
4. [Database & Backend-as-a-Service](#4-database--backend-as-a-service)
5. [Authentication](#5-authentication)
6. [Email, SMS, Notifications](#6-email-sms-notifications)
7. [Payments](#7-payments)
8. [Maps, Geo, Weather](#8-maps-geo-weather)
9. [Data / Content](#9-data--content)
10. [Hosting & Serverless](#10-hosting--serverless)
11. [Master directories](#11-master-directories)
12. [How to combine for multiple agents](#12-how-to-combine-for-multiple-agents)

---

## 1. AI / LLM (chat, agents, reasoning)

| API | What it does | Get key / sign up | Free tier (typical) | Use in projects |
|-----|--------------|-------------------|---------------------|-----------------|
| **Google AI Studio (Gemini)** | Text, image, audio, video; chat & reasoning | https://aistudio.google.com/ → Get API key | ~15 RPM, hundreds of RPD; no card | Chatbots, agents, RAG, multimodal apps |
| **Groq** | Very fast inference (Llama, Qwen) | https://console.groq.com/ | ~30–60 RPM, ~1K req/day; no card | Low-latency chat, agents |
| **OpenRouter** | One API to many models (Claude, Llama, Gemini, etc.) | https://openrouter.ai/ → Keys | ~50 req/day free; more with small top-up | Fallback LLM, trying different models |
| **Cerebras** | Fast inference (Llama 3.3 70B, etc.) | https://cloud.cerebras.ai/ | ~14.4K req/day; no card | High-volume agents |
| **Mistral AI** | Chat & embedding models | https://console.mistral.ai/ | ~1B tokens/month free | Chat + embeddings in one place |
| **Cohere** | Chat, embed, classify | https://dashboard.cohere.com/ | ~1K req/month | RAG, classification, agents |
| **DeepSeek** | Strong reasoning, cheap paid | https://platform.deepseek.com/ | Generous free / low-cost | Coding agents, long context |
| **Hugging Face Inference** | Many OSS models via API | https://huggingface.co/settings/tokens | Free tier per model | Experiment with many models |
| **NVIDIA NIM** | Llama, Qwen, etc. on NVIDIA infra | https://build.nvidia.com/ | ~57.6K req/day (tier-dependent) | Scale agents |
| **OpenAI** | GPT-4o mini, embeddings | https://platform.openai.com/api-keys | Limited free credits for new accounts | Chat, embeddings, quick prototypes |

**Agent use:** Use one primary LLM (e.g. Gemini or Groq) + OpenRouter as fallback; use Cohere/Mistral/HF for embeddings or classification in RAG/agents.

---

## 2. Voice / Speech (STT & TTS)

| API | What it does | Get key / sign up | Free tier | Use in projects |
|-----|--------------|-------------------|-----------|-----------------|
| **Google Cloud Speech-to-Text** | Audio → text | https://console.cloud.google.com/ → enable API → Credentials | 60 min/month | Voice input (e.g. iOS), voice agents |
| **Google Cloud Text-to-Speech** | Text → speech | Same GCP project, enable Text-to-Speech API | Free quota/month | Voice replies, IVR, assistants |
| **OpenAI Whisper** | Open-source STT (self-host or via providers) | Local: https://github.com/openai/whisper; API: e.g. OpenAI / Replicate | Varies by provider | Offline or low-cost transcription |
| **Browser Web Speech API** | STT/TTS in browser | No key; JavaScript only | Free, device-dependent | No-backend voice UI (e.g. Chrome, Android) |

**Agent use:** STT for “listen” (e.g. Google STT or Whisper), LLM for “think”, TTS for “speak” in voice agents and assistants.

---

## 3. Image / Vision

| API | What it does | Get key / sign up | Free tier | Use in projects |
|-----|--------------|-------------------|-----------|-----------------|
| **Replicate** | Many image models (FLUX, SD, etc.) | https://replicate.com/ → API tokens | Free tier + pay-per-run | Image gen, inpainting, agents |
| **Hugging Face** | Image models + inference API | https://huggingface.co/settings/tokens | Free tier limits | Image gen, image-to-text |
| **Google Gemini** | Image in, text out (vision) | Same as AI Studio above | Same as Gemini | Describe images, OCR, visual agents |
| **deAPI.ai** | Text-to-image (FLUX etc.) | https://deapi.ai/ | e.g. $5 free credits | Image gen for apps |
| **Pixazo** | FLUX Schnell, SD, inpainting | https://www.pixazo.ai/ | Free tier | Image gen APIs |

**Agent use:** Vision (Gemini/Replicate) for “see”; image gen (Replicate/HF/Pixazo) for “draw” in creative or support agents.

---

## 4. Database & Backend-as-a-Service

| API / Service | What it does | Get key / sign up | Free tier | Use in projects |
|---------------|--------------|-------------------|-----------|-----------------|
| **Supabase** | Postgres, auth, storage, realtime | https://supabase.com/ → New project → Settings → API | ~500 MB DB, 1 GB storage, 50K MAU | Full backend for many web apps |
| **Firebase** | NoSQL DB, auth, functions, hosting | https://console.firebase.google.com/ | Generous free tier | Mobile/web backends, realtime |
| **Neon** | Serverless Postgres | https://neon.tech/ | Free tier DB | SQL backends, serverless |
| **Turso** | SQLite at edge | https://turso.tech/ | Free tier | Lightweight backends, edge |
| **MongoDB Atlas** | NoSQL DB | https://www.mongodb.com/cloud/atlas | Free cluster | Document-style apps |
| **Upstash** | Redis (serverless) | https://upstash.com/ | Free tier | Caching, queues, rate limit |

**Agent use:** Supabase/Firebase/Neon as “memory” and user data store for multi-turn agents and app backends.

---

## 5. Authentication

| API / Service | What it does | Get key / sign up | Free tier | Use in projects |
|---------------|--------------|-------------------|-----------|-----------------|
| **Supabase Auth** | Email, magic link, OAuth, RLS | Same Supabase project | 50K MAU | Login for Supabase-backed apps |
| **Clerk** | Prebuilt login UI, MFA, social | https://clerk.com/ | ~10K MAU free | Fast add-login to any frontend |
| **NextAuth.js (Auth.js)** | OAuth + DB sessions, self-hosted | https://authjs.dev/ (code only) | Unlimited (you host) | Full control, many providers |
| **Firebase Auth** | Email, phone, social | Firebase project | Generous free | Auth for Firebase apps |

**Agent use:** Identify users so agents can have per-user history and permissions (Supabase Auth + RLS, or Clerk/NextAuth).

---

## 6. Email, SMS, Notifications

| API | What it does | Get key / sign up | Free tier | Use in projects |
|-----|--------------|-------------------|-----------|-----------------|
| **SendGrid** | Transactional email | https://signup.sendgrid.com/ → API Keys | 100 emails/day | Signup, reset password, alerts |
| **Resend** | Email API (developer-focused) | https://resend.com/ | 3K emails/month | Same as above |
| **Twilio** | SMS, voice, WhatsApp | https://www.twilio.com/console | Trial credits | OTP, notifications, voice agents |
| **Vonage (Nexmo)** | SMS, voice | https://dashboard.nexmo.com/ | Trial credits | Same as Twilio |
| **OneSignal** | Push notifications | https://onesignal.com/ | Free tier | Web/mobile push for agents |

**Agent use:** “Notify user” (email/SMS/push) when an agent finishes a task or needs approval.

---

## 7. Payments

| API | What it does | Get key / sign up | Free tier | Use in projects |
|-----|--------------|-------------------|-----------|-----------------|
| **Stripe** | Payments, subscriptions | https://dashboard.stripe.com/apikeys | Test mode fully free | Checkout, subscriptions, agent “pay” actions |
| **Razorpay** | Payments (India) | https://dashboard.razorpay.com/ | Test mode free | India-focused apps/agents |

**Agent use:** Use Stripe (or Razorpay) in test mode to prototype “pay for this” or “subscribe” inside an agent flow.

---

## 8. Maps, Geo, Weather

| API | What it does | Get key / sign up | Free tier | Use in projects |
|-----|--------------|-------------------|-----------|-----------------|
| **Google Maps / Geocoding** | Maps, places, geocode | https://console.cloud.google.com/ → APIs → Credentials | Monthly free credit | Location agents, “near me”, delivery |
| **OpenStreetMap / Nominatim** | Geocoding, search | No key (usage policy applies) | Free | Open alternative to Google |
| **OpenWeatherMap** | Weather | https://openweathermap.org/api | 1K calls/day | Weather bots, agents |
| **IPinfo** | IP → location, ASN | https://ipinfo.io/signup | 50K req/month | Geo from IP for agents |

**Agent use:** “Where is X?”, “Weather at Y”, “Places near Z” in location or weather agents.

---

## 9. Data / Content

| API | What it does | Get key / sign up | Free tier | Use in projects |
|-----|--------------|-------------------|-----------|-----------------|
| **REST Countries** | Country data | https://restcountries.com/ | Free | Localization, country-based agents |
| **Bucketlist.nl Dream of the Day** | One daily travel or life-experience idea, image and source URL; Dutch by default | No key; [OpenAPI](https://bucketlist.nl/brand/droom-van-de-dag.openapi.json) | Free keyless GET; numerical quota not published | Travel-inspiration demos and daily suggestion widgets |
| **NewsAPI** | News headlines | https://newsapi.org/ | Dev free tier | News summarizer agents |
| **GNews API** | News | https://gnews.io/ | e.g. 100 req/day | Same as above |
| **NASA API** | Space data, images | https://api.nasa.gov/ (request key) | Free | Education, space-themed agents |
| **Open Library** | Books metadata | https://openlibrary.org/developers/api | Free | Book-search agents |
| **Unsplash** | Stock photos | https://unsplash.com/developers | 50 req/hour | Image content for apps/agents |
| **CoinGecko** | Crypto prices | https://www.coingecko.com/en/api | Free tier | Crypto/portfolio agents |
| **Alpha Vantage** | Stocks, forex | https://www.alphavantage.co/support/#api-key | 25 req/day | Finance agents |

**Agent use:** Feed these into RAG or “tools” so agents can answer about news, books, crypto, stocks, etc.

---

## 10. Hosting & Serverless

| Service | What it does | Sign up | Free tier | Use in projects |
|---------|--------------|--------|-----------|-----------------|
| **Render** | Web services, static sites | https://render.com | 750 h/month, sleep when idle | Host backend + frontend (e.g. MenuMind) |
| **Vercel** | Frontend + serverless functions | https://vercel.com | Generous free | Next.js/React apps, serverless APIs |
| **Netlify** | Static + serverless | https://www.netlify.com/ | Free tier | Same as Vercel |
| **Cloudflare Workers** | Edge serverless | https://workers.cloudflare.com/ | 100K req/day | Edge APIs, lightweight agents |
| **Railway** | Apps, DBs | https://railway.app/ | Free trial / usage-based | Backend + DB in one place |
| **Fly.io** | Run containers globally | https://fly.io/ | Free allowance | Backends, agents close to users |

**Agent use:** Run your agent backend (FastAPI/Node/etc.) on Render/Railway/Fly; call LLM/voice/DB APIs from there.

---

## 11. Master directories

Use these to discover more free APIs by category:

| Resource | What it is | Link |
|----------|------------|------|
| **public-apis** | Large curated list (many categories) | https://github.com/public-apis/public-apis |
| **PublicAPIs.dev** | Searchable list | https://publicapis.dev/ |
| **Free APIs** | Categorized free APIs | https://free-apis.github.io/ |
| **free-llm.com** | Free LLM/API list | https://free-llm.com/ |
| **Awesome Agents – free inference** | Free AI inference providers | https://awesomeagents.ai/tools/free-ai-inference-providers-2026/ |

---

## 12. How to combine for multiple agents

- **Pick by capability:**  
  - Need **chat** → Gemini / Groq / OpenRouter.  
  - Need **voice in/out** → Google STT + TTS or Whisper + TTS.  
  - Need **vision** → Gemini or Replicate.  
  - Need **image gen** → Replicate / Hugging Face / Pixazo.  
  - Need **storage + auth** → Supabase or Firebase.  
  - Need **notify user** → SendGrid / Twilio / OneSignal.  
  - Need **payments** → Stripe (test).  
  - Need **location/weather** → Google Maps + OpenWeatherMap or IPinfo.

- **Combine for agent types:**  
  - **Voice assistant:** Google STT + Gemini/Groq + Google TTS + Supabase (memory).  
  - **Support chatbot:** Gemini/OpenRouter + Supabase (context) + SendGrid (tickets).  
  - **Image agent:** Gemini vision + Replicate image gen + Supabase (history).  
  - **Data agent:** LLM + REST Countries / NewsAPI / Alpha Vantage as tools + Supabase.

- **Keep limits in mind:**  
  - LLM: RPM and RPD (e.g. Gemini, Groq).  
  - Voice: minutes/month (e.g. Google STT 60 min).  
  - Email/SMS: daily/monthly caps.  
  - Hosting: hours or request limits.

---

*This document is a standalone reference. For MenuMind-AI–specific setup (env vars, limits, recovery), see **DOCUMENTATION.md**.*
