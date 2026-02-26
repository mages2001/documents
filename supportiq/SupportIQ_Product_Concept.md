
SupportIQ
AI-Powered Customer Support for Every SMB
Product Concept Document  •  v1.0

# 1. Executive Summary
SupportIQ is a multi-channel AI customer support platform built exclusively for small and medium businesses (SMBs). It enables any business — regardless of technical skill — to deploy an intelligent support agent across chat, email, WhatsApp/SMS, and voice calls within minutes. The AI handles the majority of customer interactions autonomously, and when it cannot, it performs a seamless handoff to a human agent whose responses it then learns from — continuously improving without manual retraining.
Businesses are charged only for conversations that occur, making SupportIQ accessible to the smallest shop and scalable to a fast-growing company.

# 2. The Problem

| SMB Pain Points | SupportIQ Solution |
| :--- | :--- |
| ❌ Hiring even one support agent costs $30,000–$50,000/year | ✅ SupportIQ handles routine queries automatically, 24/7 |
| ❌ Chatbot builders require technical setup and ongoing maintenance | ✅ No-code onboarding: upload a document or chat to build your knowledge base |
| ❌ AI tools that work well for enterprises are priced out of SMB reach | ✅ Pay-per-conversation pricing — zero cost when idle |
| ❌ Generic bots frustrate customers with irrelevant answers | ✅ AI trained on YOUR business data for relevant, accurate answers |
| ❌ Missed support requests outside business hours lose sales | ✅ Omnichannel: chat, email, WhatsApp/SMS, and voice in one platform |

# 3. Product Vision
"Any SMB — from a local bakery to a fast-growing e-commerce brand — should be able to offer enterprise-grade customer support without hiring a single dedicated support agent."

SupportIQ achieves this through three core principles:
- Zero-friction onboarding: a business is live in under 10 minutes.
- Human-in-the-loop learning: the AI gets smarter by watching real human agents resolve edge cases.
- Radical accessibility: pay only for what you use, no contracts, no setup fees.

# 4. Target Customer
## Primary Segment
SMBs across all industries with 1–200 employees who receive repetitive customer inquiries and currently handle them manually via email, WhatsApp, or phone.
## Example Verticals
- 🛍 E-commerce / retail stores
- 🏡 Real estate agencies
- 💈 Salons, spas, clinics
- 🛠 Home services (plumbers, electricians)
- 🍕 Restaurants & food delivery
- 📚 Online education / coaching
- 🏋 Gyms & fitness studios
- 🏥 Healthcare & wellness clinics

# 5. Supported Channels
SupportIQ meets customers wherever they already are. All channels share the same AI brain and knowledge base.

| Channel | How It Works | Integration |
| :--- | :--- | :--- |
| 💬 Website Chat | Embeddable chat widget installed via a single script tag. AI responds in real time. | Copy-paste JS snippet |
| 📱 WhatsApp / SMS | Business WhatsApp number connects to SupportIQ. Customers text as normal. | WhatsApp Business API / Twilio |
| 📧 Email | Business email address (e.g. support@company.com) routed through SupportIQ. | Email forwarding / SendGrid |
| 📞 Voice Calls | Inbound calls handled by an AI voice agent with natural speech. Escalates to human if needed. | Twilio Voice / Deepgram STT |

# 6. Core Features
## 6.1  Knowledge Base Builder
The AI needs to know your business before it can help customers. SupportIQ offers three zero-friction ways to build this knowledge base:
- Document Upload: upload a PDF, Word doc, or text file of FAQs, policies, pricing, etc. The AI parses and indexes it automatically.
- Chat-to-KB: the onboarding assistant interviews the business owner through a guided conversation ("What are your most common questions?") and constructs the knowledge base from the answers.
- Voice-to-KB: business owners can speak their answers, which are transcribed and structured into the knowledge base automatically.

## 6.2  AI Conversation Engine
The core AI agent that handles live customer interactions across all channels. It:
- Understands intent and extracts key information from natural language, including voice.
- Answers from the knowledge base with high accuracy, citing specific policies or FAQs when relevant.
- Handles multi-turn conversations — it remembers context within a session.
- Detects when it cannot resolve an issue and triggers a handoff rather than giving a wrong answer.

## 6.3  Smart Human Handoff
When the AI cannot resolve a query, it escalates to a human agent. This is the most critical moment in the product — it must be seamless:
- The human agent sees the full conversation history before stepping in, with a summary of what was tried.
- The customer is notified naturally: "Let me connect you with a team member who can help further."
- The human can take over mid-conversation on any channel (chat, email, or via a call queue for voice).
- Handoff thresholds are configurable: businesses set how many AI attempts before escalation.

## 6.4  Learning from Human Agents  (Key Differentiator)
Every time a human agent resolves a case the AI could not handle, the system observes the resolution and learns from it:
- The AI flags: "I could not resolve this. Here is what the human agent did."
- A lightweight review step lets the business approve or reject the suggested knowledge update.
- Approved resolutions are added to the knowledge base, improving future AI accuracy.
- Learning is isolated per business — no cross-customer data sharing.

## 6.5  Business Dashboard
- Real-time conversation monitoring across all channels.
- AI resolution rate, handoff rate, average response time, and CSAT scores.
- Knowledge base editor: add, edit, or remove entries manually.
- Billing overview: conversations used, cost-to-date, projected monthly bill.
- Agent management: add human agents and configure escalation rules.

# 7. Business Model & Pricing
Pay-per-conversation: businesses are charged only when a conversation occurs. A conversation is defined as a continuous interaction with one customer on one channel, regardless of the number of messages exchanged, up to 30 minutes of inactivity.

| Tier | Conversations/Month | Price Per Conversation |
| :--- | :--- | :--- |
| Starter | 0 – 500 | $0.08 |
| Growth | 501 – 5,000 | $0.06 |
| Scale | 5,001 – 50,000 | $0.04 |
| Enterprise | 50,000+ | Custom negotiated |

Additional charges apply for voice (billed per minute of call at $0.03/min) and SMS (billed per outbound message at $0.01/message). A free trial of 100 conversations is included on signup with no credit card required.

# 8. Technical Architecture
## 8.1  High-Level Components

| Core Backend Components | Supporting Systems |
| :--- | :--- |
| Omnichannel Gateway | Human Agent Interface |
| AI Orchestration Layer | Business Dashboard (Web App) |
| Knowledge Base Engine | Billing & Usage Metering |
| Voice Processing Pipeline | Authentication & Multi-tenancy |
| Learning & Feedback Loop | Notification Service |

## 8.2  AI & ML Stack
- LLM: Claude (Anthropic) via API for conversation understanding, response generation, and KB synthesis.
- Speech-to-Text: Deepgram or Whisper for transcribing voice calls in real time.
- Text-to-Speech: ElevenLabs or Amazon Polly for natural AI voice responses.
- Vector Database: Pinecone or Weaviate for fast semantic search across each business's knowledge base.
- Embeddings: OpenAI or Cohere for embedding knowledge base documents for similarity search.

## 8.3  Infrastructure
- Backend: Node.js / Python microservices, deployed on AWS or GCP.
- Database: PostgreSQL (structured data), Redis (session/cache), S3 (documents/audio files).
- Messaging: WhatsApp Business API via 360dialog or Twilio; SMS via Twilio.
- Email: SendGrid Inbound Parse for routing support emails into the platform.
- Multi-tenancy: each business is a fully isolated tenant with its own knowledge base and conversation history.

# 9. Key User Journeys
## Journey 1: Business Owner Onboarding (Target: < 10 minutes)
- 1. Signs up with email — no credit card required.
- 2. Chooses business type and uploads an FAQ document (or skips to chat-based setup).
- 3. AI-guided chat interview asks 5–7 questions to fill gaps in the knowledge base.
- 4. Picks channels to activate (chat widget, WhatsApp, email, voice).
- 5. Installs the chat widget via a script tag, or connects WhatsApp/email/phone number.
- 6. Sends a test message — sees the AI respond correctly.
- 7. Goes live.

## Journey 2: Customer Interaction (AI Resolves)
- Customer contacts via any supported channel.
- AI greets, understands the query, and responds accurately from the knowledge base.
- Conversation closes. Business is billed for 1 conversation.

## Journey 3: Customer Interaction (AI Escalates)
- Customer asks something the AI cannot resolve (e.g. a complex complaint).
- AI says: "Let me connect you with someone from our team."
- Human agent receives a notification with full conversation context.
- Agent resolves the issue. The AI observes the resolution.
- Platform suggests a knowledge base update for owner approval.

# 10. Risks & Mitigations

| Risk | Mitigation |
| :--- | :--- |
| AI gives a wrong answer confidently | Confidence scoring: AI declines to answer below a threshold and escalates instead |
| Business provides poor/no knowledge base | Mandatory onboarding quality check before going live; AI interview mode fills gaps |
| Voice quality is poor in noisy environments | Voice channel flagged as beta; fallback to text when STT confidence is low |
| Privacy concerns about conversation data | Data stored per-tenant; no cross-business training; GDPR/CCPA compliant |
| SMBs churn when ROI is not clear | Dashboard shows clear "cost saved vs. agent" metric; in-app ROI calculator |

# 11. Phased Roadmap

| PHASE 1 — MVP (Month 0–4) | PHASE 2 — Expand (Month 5–8) |
| :--- | :--- |
| Website chat widget only | WhatsApp / SMS channel |
| Document upload knowledge base | Email channel |
| Basic human handoff (email notification) | Chat-to-KB and voice-to-KB onboarding |
| Simple dashboard with usage stats | Improved handoff (in-platform agent console) |
| Pay-per-conversation billing | Mobile app for agents |

| PHASE 3 — Growth (Month 9–15) | PHASE 4 — Scale (Month 16+) |
| :--- | :--- |
| Voice channel (inbound calls) | Multilingual support (10+ languages) |
| AI learning from human agents | CRM integrations (HubSpot, Zoho, Salesforce) |
| Multi-agent team management | White-label version for resellers |
| Advanced analytics & CSAT tracking | Industry-specific AI models |
| API access for custom integrations | Self-service Enterprise tier |

# 12. Success Metrics
- AI Resolution Rate: % of conversations fully handled by AI without human handoff. Target: >70% by Month 6.
- Time to First Response: AI should respond within 3 seconds on chat/WhatsApp; within 1 minute on email.
- Onboarding Completion Rate: % of signups that go live on at least one channel. Target: >60%.
- Monthly Churn Rate: Target <5% of active paying customers per month.
- Customer CSAT Score: Target >4.2/5 average across resolved conversations.
- Knowledge Base Improvement Rate: % of escalations that result in an approved KB update. Target: >40%.

SupportIQ  •  Product Concept v1.0  •  Confidential