# Content Maker - API Keys Checklist

## Required API Keys Status

### HAVE (From Existing Projects)
| Service | Status | Where to Get |
|---------|--------|--------------|
| Anthropic (Claude) | HAVE | Used in existing content makers |
| OpenAI (DALL-E) | HAVE | Used in existing content makers |
| Supabase | HAVE | o1dmatch project: oubszyfragjtiudhfygw.supabase.co |
| Stripe | HAVE | o1dmatch project (for future billing) |
| Vercel | HAVE | innovative-automations-projects team |

### NEED TO VERIFY
| Service | Status | Where to Get |
|---------|--------|--------------|
| Perplexity | CHECK | https://www.perplexity.ai/settings/api |
| LlamaParse | CHECK | https://cloud.llamaindex.ai/ |

### NEED TO GET
| Service | Purpose | Where to Get |
|---------|---------|--------------|
| Google Cloud (Vertex AI) | RAG Engine for document processing | https://console.cloud.google.com/ |
| YouTube Data API | Extract video transcripts | https://console.developers.google.com/ |
| NanoBanana Pro | Alternative image generation | Contact NanoBanana |

---

## Step-by-Step Setup Instructions

### 1. Perplexity API
1. Go to https://www.perplexity.ai/settings/api
2. Create API key
3. Note: Uses `sonar` model, pricing ~$1/M tokens

### 2. Google Cloud / Vertex AI RAG
1. Go to https://console.cloud.google.com/
2. Create or select project
3. Enable APIs:
   - Vertex AI API
   - Document AI API
   - Cloud Storage API
4. Create service account
5. Download JSON key
6. Set environment variable: `GOOGLE_APPLICATION_CREDENTIALS`

### 3. YouTube Data API
1. Go to https://console.developers.google.com/
2. Enable YouTube Data API v3
3. Create API key (API restrictions optional)
4. For transcripts, can use: `youtube-transcript-api` npm package

### 4. NanoBanana Pro
1. Visit NanoBanana website
2. Request API access
3. May need business account

---

## Environment Variables Template

```env
# ============================================
# CONTENT MAKER - REQUIRED KEYS
# ============================================

# AI Content Generation
ANTHROPIC_API_KEY=sk-ant-xxxxx
OPENAI_API_KEY=sk-xxxxx

# Real-time Research
PERPLEXITY_API_KEY=pplx-xxxxx

# RAG / Document Processing
GOOGLE_APPLICATION_CREDENTIALS=./path-to-service-account.json
GOOGLE_CLOUD_PROJECT=your-project-id

# YouTube Integration
YOUTUBE_API_KEY=AIza-xxxxx

# Image Generation (Alternative)
NANOBANANA_API_KEY=xxxxx

# Database
NEXT_PUBLIC_SUPABASE_URL=https://xxxxx.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=xxxxx
SUPABASE_SERVICE_ROLE_KEY=xxxxx

# ============================================
# GOOGLE APPS SCRIPT KEYS
# (Store in Script Properties)
# ============================================
# ANTHROPIC_API_KEY
# OPENAI_API_KEY
# PERPLEXITY_API_KEY
```

---

## Action Items

- [ ] Verify Perplexity API key exists in mega-internal project
- [ ] Set up Google Cloud project for Vertex AI
- [ ] Enable YouTube Data API
- [ ] Contact NanoBanana for API access
- [ ] Copy existing Anthropic & OpenAI keys to Content Maker

---

## Notes

- Google Apps Script stores keys in "Script Properties" (Project Settings)
- SaaS app will use .env.local file
- Keep keys secure - never commit to git!
