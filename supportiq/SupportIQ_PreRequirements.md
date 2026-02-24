
SupportIQ
Pre-Requirements Document
Technical & Business Prerequisites  •  Starting from Zero  •  v1.0


# 1. Prerequisite Overview
SupportIQ is a multi-channel AI customer support platform. Because it touches voice, messaging, email, payments, and AI — all in a single product — the prerequisite footprint is larger than a typical web app. The good news: most services have free tiers or trial credits that let you build the MVP at near-zero cost.


# 2. Technical Prerequisites
## 2.1  Core AI & Language Model
The entire AI conversation engine runs on an LLM. This must be set up and tested before any chat functionality can be built.


## 2.2  Voice Processing
Voice is the most complex channel. You need both speech-to-text (STT) and text-to-speech (TTS) services, plus a telephony provider for handling actual phone calls.



## 2.3  Messaging Channels
Each messaging channel requires its own third-party service integration and, in the case of WhatsApp, an approval process.


## 2.4  Infrastructure & Hosting
SupportIQ needs a cloud provider for compute, database, file storage, and caching. AWS is recommended due to its breadth of managed services and free tier.


## 2.5  Authentication & Multi-tenancy
Every business on SupportIQ is an isolated tenant. Authentication must be set up before any business dashboard or user account flows can be built.


## 2.6  Payments & Billing
Since the business model is pay-per-conversation, a billing system must be in place before any real customers can be charged. Do not attempt to build your own billing logic.


## 2.7  Developer Tooling
These tools need to be installed and configured on every developer machine before coding starts.


## 2.8  Frontend

# 3. Business & Legal Prerequisites
## 3.1  Company Formation
You need a legal entity before opening business bank accounts, signing API agreements (WhatsApp, Stripe), or taking on customers. This is the single most important non-technical step.


## 3.2  Legal Documents
These documents must be live on your website before you accept any customers or process any personal data. Without them you are exposed to significant legal risk.


## 3.3  Data Privacy & Compliance
SupportIQ processes end-customer conversations on behalf of SMBs. This makes it a data processor under GDPR and a service provider under CCPA. These obligations must be understood before storing a single message.



## 3.4  Third-Party Service Agreements
Several service providers require you to agree to specific commercial terms or go through an approval process before using their APIs in a production product.


## 3.5  Brand & Domain

# 4. Estimated Monthly Costs (MVP Phase)
The following table estimates monthly costs for a running MVP serving a small number of test customers (roughly 1,000–5,000 conversations). Most services offer free tiers that cover early development.



# 5. Skills & Team Prerequisites
Building SupportIQ solo is possible but demanding. The following skills are needed across the project. Gaps should be filled before development begins — either through a co-founder, a contractor, or focused upskilling.


# 6. Pre-Development Checklist (Week 0)
Complete every item in this list before writing a single line of application code. These are the minimum viable prerequisites for safe, legal, and unblocked development.

## Business Setup
- Register company (LLC / Pvt Ltd) and obtain PAN/EIN.
- Open a business bank account.
- Register for GST (if India-based).
- Register domain and set up business email (Google Workspace).
- Begin WhatsApp Business API application immediately (long lead time).

## Accounts to Create on Day 1
- Anthropic Console — generate API key, save securely.
- Pinecone — create a starter index.
- Cohere or OpenAI — for embeddings.
- Deepgram — for STT (even if voice is Phase 3).
- ElevenLabs — for TTS.
- Twilio — verify identity, provision one phone number.
- SendGrid — configure Inbound Parse and add DNS records.
- AWS — set up root account, create IAM admin user, enable MFA.
- Stripe — connect bank account, enable Metered Billing, generate test API keys.
- Clerk or Auth0 — set up application.
- GitHub — create organization, private repos.
- Sentry — create project for backend and frontend.
- ngrok — install and authenticate for local webhook testing.
- Doppler or AWS Secrets Manager — set up secret storage.

## Legal & Compliance
- Draft and publish Terms of Service.
- Draft and publish Privacy Policy (GDPR + CCPA compliant).
- Draft Data Processing Agreement (DPA) template.
- Review and accept Anthropic, Twilio, Meta, Stripe commercial terms.
- Define data retention policy (recommended: 90 days default, configurable).
- Register for A2P 10DLC if targeting US SMS customers.

## Technical Setup
- Install Node.js 20, Python 3.11+, Docker on all dev machines.
- Create .env.example file listing every required environment variable.
- Design multi-tenant PostgreSQL schema (tenant_id on every table).
- Set up CI/CD pipeline (GitHub Actions) with lint + test steps.
- Configure Cloudflare DNS for domain.
- Provision AWS S3 bucket with server-side encryption enabled.
- Spin up Supabase (or RDS) instance for development database.

SupportIQ  •  Pre-Requirements v1.0  •  Confidential