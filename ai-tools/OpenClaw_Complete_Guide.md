# OpenClaw: The Complete Guide to Your Personal AI Assistant 🦞

> **"The AI that actually does things."** - Your 24/7 autonomous assistant that runs on YOUR machine, remembers everything, and executes tasks across all your favorite apps.

---

## 📚 Table of Contents

### Part 1: Getting Started
1. [What is OpenClaw?](#what-is-openclaw)
2. [Why OpenClaw is Revolutionary](#why-openclaw-is-revolutionary)
3. [Quick Start Guide](#quick-start-guide)
4. [Installation Methods](#installation-methods)
5. [First Conversation](#first-conversation)

### Part 2: Core Concepts
6. [Architecture Overview](#architecture-overview)
7. [The Gateway System](#the-gateway-system)
8. [Sessions and Memory](#sessions-and-memory)
9. [Lane Queue System](#lane-queue-system)
10. [How OpenClaw Thinks](#how-openclaw-thinks)

### Part 3: Features & Capabilities
11. [Messaging Platform Integration](#messaging-platform-integration)
12. [AI Model Support](#ai-model-support)
13. [File System Access](#file-system-access)
14. [Browser Automation](#browser-automation)
15. [Email Management](#email-management)
16. [Calendar Integration](#calendar-integration)
17. [Smart Home Control](#smart-home-control)
18. [Developer Tools](#developer-tools)

### Part 4: Skills System
19. [Understanding Skills](#understanding-skills)
20. [Bundled Skills](#bundled-skills)
21. [Installing Skills from ClawHub](#installing-skills-from-clawhub)
22. [Creating Custom Skills](#creating-custom-skills)
23. [Skill Security](#skill-security)
24. [Popular Community Skills](#popular-community-skills)

### Part 5: Advanced Features
25. [Proactive Features (Heartbeats & Cron)](#proactive-features)
26. [Multi-Agent Routing](#multi-agent-routing)
27. [Voice Wake & Talk Mode](#voice-wake-talk-mode)
28. [Canvas & Visual Workspace](#canvas-visual-workspace)
29. [Webhook Integration](#webhook-integration)
30. [Gmail Pub/Sub Triggers](#gmail-pubsub-triggers)

### Part 6: Real-World Use Cases
31. [Personal Productivity](#personal-productivity)
32. [Business Automation](#business-automation)
33. [Developer Workflows](#developer-workflows)
34. [Content Creation](#content-creation)
35. [Smart Home & IoT](#smart-home-iot)
36. [Health & Wellness Tracking](#health-wellness-tracking)

### Part 7: Configuration & Customization
37. [Configuration Files](#configuration-files)
38. [Persona Customization](#persona-customization)
39. [Routing Rules](#routing-rules)
40. [Sandbox Mode](#sandbox-mode)
41. [Resource Management](#resource-management)

### Part 8: Security & Best Practices
42. [Security Model](#security-model)
43. [Authentication & Access Control](#authentication-access-control)
44. [Sandboxing Options](#sandboxing-options)
45. [Privacy Considerations](#privacy-considerations)
46. [Secure Deployment](#secure-deployment)

### Part 9: Platform-Specific Guides
47. [macOS Setup](#macos-setup)
48. [Windows (WSL2) Setup](#windows-setup)
49. [Linux Setup](#linux-setup)
50. [Raspberry Pi Deployment](#raspberry-pi-deployment)
51. [Cloud Deployment](#cloud-deployment)

### Part 10: Community & Resources
52. [Official Documentation](#official-documentation)
53. [Community Discord](#community-discord)
54. [GitHub Repository](#github-repository)
55. [ClawHub Skills Registry](#clawhub-skills-registry)
56. [Troubleshooting](#troubleshooting)

---

## Part 1: Getting Started

### What is OpenClaw?

**OpenClaw** (formerly Clawdbot, then Moltbot) is an open-source, autonomous AI assistant that runs locally on your computer and connects to your favorite messaging apps. Unlike traditional chatbots that live in browser tabs, OpenClaw is a **true personal AI agent** that can:

- 🤖 **Execute real actions** on your computer (not just answer questions)
- 💬 **Work through messaging apps** you already use (WhatsApp, Telegram, Discord, Slack, Signal, iMessage)
- 🧠 **Remember everything** across conversations with persistent memory
- 🔄 **Run 24/7** as a background service
- 🛠️ **Access your files**, run terminal commands, browse the web, manage emails
- 🎨 **Build itself better** - it can create its own skills and improve over time

**Created by:** Peter Steinberger (Austrian developer, creator of PSPDFKit)  
**Released:** November 2025  
**GitHub Stars:** 145,000+ (as of Feb 2026)  
**License:** Free and Open Source

**Official Links:**
- Website: https://openclaw.ai
- Documentation: https://docs.openclaw.ai
- GitHub: https://github.com/openclaw/openclaw
- Skills Registry: https://clawhub.com

---

### Why OpenClaw is Revolutionary

#### 1. **It Actually DOES Things**
Most AI assistants can only talk. OpenClaw executes:
- Clears your inbox
- Sends emails on your behalf
- Manages your calendar
- Books appointments
- Checks you in for flights
- Creates and deploys websites
- Writes and runs code
- Controls smart home devices

#### 2. **Privacy-First Architecture**
- Runs **entirely on YOUR computer** (or your private server)
- No data sent to external servers except LLM API calls
- Full control over what it can access
- Open source - you can audit every line of code

#### 3. **Platform Agnostic**
Works on:
- macOS, Windows, Linux
- Raspberry Pi
- Cloud servers (DigitalOcean, AWS, etc.)

Connects to:
- WhatsApp, Telegram, Discord, Slack, Signal, iMessage
- Microsoft Teams, Google Chat, Matrix, Zalo
- Custom WebChat interface

#### 4. **Extensible Skills System**
- 50+ official integrations
- Hundreds of community-built skills
- Create your own skills in minutes
- Skills can even write themselves

#### 5. **Persistent Memory**
Unlike ChatGPT that forgets after each session:
- Remembers your preferences, context, and history
- Maintains state across days, weeks, months
- Learns from your interactions
- Shares memory across different agents (Codex, Cursor, etc.)

#### 6. **Proactive & Autonomous**
- Can run scheduled tasks (cron jobs)
- Sends you morning briefings
- Monitors systems in the background
- Checks in periodically with "heartbeats"
- Responds to webhooks and triggers

---

### Quick Start Guide

**Get running in 5 minutes:**

#### Prerequisites
- Node.js 22 or newer
- An API key for Claude, GPT, or a local model

#### One-Line Install

**macOS/Linux:**
```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

**Windows (PowerShell):**
```powershell
iwr -useb https://openclaw.ai/install.ps1 | iex
```

**npm (all platforms):**
```bash
npm install -g openclaw@latest
```

#### Setup Wizard

```bash
openclaw onboard --install-daemon
```

The wizard will guide you through:
1. ✅ Choosing your AI model (Claude, GPT, local, etc.)
2. ✅ Setting up authentication
3. ✅ Configuring messaging channels (optional)
4. ✅ Creating your assistant's personality
5. ✅ Installing as a background service

#### Alternative: Quick Dashboard Chat

Skip channel setup and chat immediately in your browser:

```bash
openclaw dashboard
```

Then open: http://127.0.0.1:18789/

---

### Installation Methods

#### Method 1: One-Line Installer (Recommended)
The installer handles everything: Node.js, dependencies, setup.

```bash
# macOS/Linux
curl -fsSL https://openclaw.ai/install.sh | bash

# Windows
iwr -useb https://openclaw.ai/install.ps1 | iex
```

#### Method 2: npm Install
If you already have Node.js:

```bash
npm install -g openclaw@latest
openclaw onboard --install-daemon
```

#### Method 3: Hackable Install (for developers)
Clone and build from source:

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
pnpm run build
pnpm run openclaw onboard
```

#### Method 4: macOS App (Beta)
Download the companion menubar app:
- Download: https://github.com/openclaw/openclaw/releases/latest
- Requires: macOS 14+ (Universal Binary)
- Works alongside the CLI

#### Method 5: Cloud Deployment

**DigitalOcean 1-Click:**
- Visit DigitalOcean Marketplace
- Search for "OpenClaw"
- Deploy with one click
- Includes security hardening

**Docker (Advanced):**
```bash
docker pull openclaw/openclaw:latest
docker run -d openclaw/openclaw
```

---

### First Conversation

Once installed, start chatting! Here are some example commands:

#### Getting Started
```
You: Hey, what can you do?
Claw: I can help you with emails, calendar, files, web browsing, 
      coding, automation, and much more. What would you like to try?

You: Tell me about yourself
Claw: I'm your personal AI assistant running on this machine. I have 
      access to your files, can browse the web, manage your calendar, 
      and execute tasks 24/7. I remember our conversations and learn 
      your preferences over time.
```

#### Simple Tasks
```
You: What time is it?
Claw: It's 2:47 PM EST on Saturday, February 7, 2026.

You: Remind me to call mom tomorrow at 2pm
Claw: ✓ Created reminder for tomorrow at 2:00 PM: "Call mom"

You: Search for the latest AI news
Claw: [Browses web and returns summary]
```

#### File Operations
```
You: Create a file called notes.txt with my meeting notes
Claw: ✓ Created notes.txt in your current directory

You: List all PDF files in my Downloads folder
Claw: Found 12 PDF files: [lists files]

You: Summarize research_paper.pdf
Claw: [Reads and summarizes the document]
```

#### Advanced Tasks
```
You: Build me a website for my portfolio
Claw: I'll create a portfolio website. What's your name and 
      what projects should I showcase?
      
You: Check my emails from today and flag anything important
Claw: Found 3 important emails: [summarizes]

You: When is my next meeting?
Claw: Your next meeting is "Team Sync" tomorrow at 10 AM
```

---

## Part 2: Core Concepts

### Architecture Overview

OpenClaw uses a **gateway-centric architecture** with clear separation of concerns:

```
┌─────────────────────────────────────────┐
│  Messaging Platforms                    │
│  (WhatsApp, Telegram, Discord, etc.)    │
└──────────────┬──────────────────────────┘
               │
               ▼
┌─────────────────────────────────────────┐
│         Channel Adapters                │
│  (Normalize messages from all platforms)│
└──────────────┬──────────────────────────┘
               │
               ▼
┌─────────────────────────────────────────┐
│           Gateway                       │
│  • Session Management                   │
│  • Message Routing                      │
│  • WebSocket Control Plane              │
│  • Lane Queue (Concurrency Control)     │
└──────────────┬──────────────────────────┘
               │
               ▼
┌─────────────────────────────────────────┐
│         Agent Runner                    │
│  • Prompt Construction                  │
│  • Tool/Skill Loading                   │
│  • Model API Calls                      │
│  • Response Processing                  │
└──────────────┬──────────────────────────┘
               │
               ▼
┌─────────────────────────────────────────┐
│      Execution Layer                    │
│  • File System Operations               │
│  • Terminal Commands                    │
│  • Browser Automation                   │
│  • API Calls                            │
└─────────────────────────────────────────┘
```

#### Key Components:

**1. Channel Adapters**
- Normalize messages from different platforms
- Handle platform-specific features (stickers, reactions, embeds)
- Extract attachments consistently

**2. Gateway Server**
- Single control plane running on port 18789 (default)
- Manages all connections
- Routes messages to appropriate sessions
- Prevents race conditions with Lane Queue

**3. Session Manager**
- Maintains context for each conversation
- DMs share the main session by default
- Each group chat gets isolated session
- Custom sessions for routing/security

**4. Agent Runner**
- Constructs prompts with context
- Loads relevant skills
- Calls LLM APIs
- Processes tool calls

**5. Tool System**
- Structured function definitions
- Filesystem, browser, messaging, etc.
- Policy-controlled access

---

### The Gateway System

The **Gateway** is the heart of OpenClaw. It's a long-running Node.js process that:

#### Core Responsibilities:
1. **Channel Management** - Connects to WhatsApp, Telegram, etc.
2. **Session Routing** - Directs messages to the right session
3. **WebSocket Control Plane** - API on ws://127.0.0.1:18789
4. **Tool Coordination** - Manages tool execution
5. **File Serving** - Canvas host on port 18793

#### Gateway Commands:

```bash
# Start the gateway
openclaw gateway

# Check status
openclaw gateway status

# Stop
openclaw gateway stop

# Restart
openclaw gateway restart

# View logs
openclaw gateway logs

# Run with verbose output
openclaw gateway --verbose
```

#### Security Model:
- **Loopback-first**: Runs on localhost (127.0.0.1) by default
- **Authentication**: Uses gateway tokens
- **Remote Access**: Via SSH tunnels or Tailscale
- **Sandboxing**: Optional Docker isolation

---

### Sessions and Memory

#### Session Types:

**1. Main Session**
- Default for all direct messages
- Shared context across your personal chats
- Persistent memory

**2. Group Sessions**
- Each group chat gets isolated session
- Prevents context leakage
- Configurable per-group

**3. Isolated Sessions**
- Created for specific routing rules
- Security-sensitive conversations
- Custom agent configurations

#### Memory Architecture:

OpenClaw uses a **hybrid memory system**:

**1. JSONL Transcripts**
- Line-by-line audit of every interaction
- User messages, tool calls, execution results
- Factual and complete

Location: `~/.openclaw/workspace/memory/transcripts/`

**2. Markdown Memory Files**
- Human-readable summaries
- Distilled knowledge
- Experiences and learnings

Location: `~/.openclaw/workspace/memory/MEMORY.md`

**3. Daily Logs**
- Append-only ephemeral logs
- One file per day

Location: `~/.openclaw/workspace/memory/YYYY-MM-DD.md`

**4. Hybrid Search**
- **Vector Search** (70%): Semantic similarity via embeddings
- **BM25 Keyword** (30%): Exact term matching
- **SQLite FTS5**: Full-text search index

#### Memory Commands:

```bash
# Compact memory (summarize and reduce context)
/compact

# Clear specific memory
/forget [topic]

# Search memory
/recall [query]

# View memory stats
/memory stats
```

---

### Lane Queue System

The **Lane Queue** prevents race conditions when handling multiple simultaneous requests.

#### How It Works:

1. **Lanes**: Each session has a lane (like a checkout line)
2. **Serial Execution**: Messages in a lane process one at a time
3. **Concurrency Control**: Different lanes can run in parallel
4. **State Protection**: Prevents overlapping tool calls

#### Example:

```
User sends 3 messages rapidly:
1. "Read my email"
2. "Summarize the latest"
3. "Reply to Sarah"

Without Lane Queue: All 3 start simultaneously → chaos
With Lane Queue: Executes 1 → 2 → 3 in order → clean
```

#### Configuration:

```json
{
  "routing": {
    "lanes": {
      "concurrency": 1,  // Serial by default
      "timeout": 300000  // 5 minute timeout
    }
  }
}
```

---

### How OpenClaw Thinks

#### The Agent Loop:

```
1. RECEIVE MESSAGE
   ↓
2. LOAD CONTEXT
   - Session history
   - Memory files
   - Skills available
   ↓
3. CONSTRUCT PROMPT
   - System instructions
   - User message
   - Available tools
   ↓
4. CALL LLM API
   - Claude, GPT, or local model
   ↓
5. PROCESS RESPONSE
   - Text response?
   - Tool call needed?
   ↓
6. EXECUTE TOOLS
   - Run commands
   - Access files
   - Browse web
   ↓
7. UPDATE MEMORY
   - Record interaction
   - Update context
   ↓
8. RETURN RESPONSE
   - Send to user
   - Wait for next message
```

#### Semantic Snapshots (Browser):

Instead of screenshots, OpenClaw uses **accessibility trees**:

**Traditional Approach:**
- Screenshot: 5MB image
- Vision model processes pixels
- Slow and expensive

**OpenClaw Approach:**
- Accessibility tree: <50KB text
- Structured elements: `button "Sign In" [ref=1]`
- Fast, cheap, precise
- 90% token reduction

---

## Part 3: Features & Capabilities

### Messaging Platform Integration

OpenClaw connects to 12+ messaging platforms:

#### Supported Platforms:

**Primary Channels:**
- ✅ **WhatsApp** - via Baileys web client
- ✅ **Telegram** - bot API
- ✅ **Discord** - bot API
- ✅ **Slack** - bot API
- ✅ **Signal** - via signal-cli
- ✅ **iMessage** - via BlueBubbles or legacy mode

**Additional Channels:**
- ✅ Microsoft Teams
- ✅ Google Chat
- ✅ Matrix
- ✅ Zalo (Vietnam)
- ✅ Mattermost (plugin)
- ✅ WebChat (built-in browser interface)

#### Setup Examples:

**WhatsApp:**
```bash
openclaw configure --section whatsapp
# Scan QR code with your phone
```

**Telegram:**
```bash
# Get bot token from @BotFather
openclaw configure --section telegram
# Enter your bot token
```

**Discord:**
```bash
# Create bot at discord.com/developers
openclaw configure --section discord
# Enter bot token and add to server
```

---

### AI Model Support

OpenClaw supports multiple LLM providers:

#### Supported Providers:

**1. Anthropic Claude** (Recommended)
- Claude Opus 4.5
- Claude Sonnet 4.5
- Claude Haiku 4.5

**2. OpenAI**
- GPT-4
- GPT-4 Turbo
- GPT-3.5 Turbo

**3. Local Models**
- LM Studio
- Ollama
- LocalAI
- Any OpenAI-compatible endpoint

**4. Other Providers**
- Google Gemini
- DeepSeek
- MiniMax
- Anthropic via Bedrock
- OpenRouter (multi-provider)

#### Model Configuration:

**Using Anthropic Claude:**
```json
{
  "models": {
    "primary": "claude-sonnet-4-5-20250929",
    "provider": "anthropic",
    "apiKey": "your-api-key"
  }
}
```

**Using OpenRouter:**
```bash
openclaw configure --provider openrouter
```

**Using Local Model:**
```json
{
  "models": {
    "primary": "local/llama-3.1",
    "provider": "openai-compatible",
    "apiEndpoint": "http://localhost:1234/v1"
  }
}
```

#### Model Fallback:

```json
{
  "models": {
    "primary": "claude-sonnet-4-5-20250929",
    "fallback": [
      "claude-haiku-4-5-20251001",
      "gpt-4"
    ]
  }
}
```

**Recommended Setup:**
- **Primary**: Claude Sonnet 4.5 (best balance)
- **Heavy tasks**: Claude Opus 4.5
- **Quick tasks**: Claude Haiku 4.5
- **Local fallback**: For privacy-sensitive tasks

---

### File System Access

OpenClaw can read, write, and manage files on your system:

#### Capabilities:

**Reading Files:**
```
You: What's in my Documents folder?
Claw: [Lists all files and folders]

You: Read presentation.pptx
Claw: [Extracts and summarizes content]

You: Find all Python files modified this week
Claw: [Searches and lists files]
```

**Writing Files:**
```
You: Create a markdown file with my meeting notes
Claw: ✓ Created meeting_notes.md

You: Generate a CSV of my expenses
Claw: ✓ Created expenses.csv with your data

You: Save this conversation as conversation.txt
Claw: ✓ Saved to conversation.txt
```

**File Operations:**
```
You: Organize my Downloads folder
Claw: Created folders by type, moved 45 files

You: Compress all photos from last month
Claw: ✓ Created photos_jan_2026.zip (2.3 GB)

You: Delete all temp files
Claw: Removed 127 temporary files (892 MB freed)
```

#### Workspace:

Default location: `~/.openclaw/workspace/`

```
workspace/
├── memory/          # Persistent memory files
├── skills/          # Custom skills
├── tmp/            # Temporary files
├── outputs/        # Generated files
└── config/         # Agent configuration
```

#### Safety Features:

- **Approval Required**: Destructive operations need confirmation
- **Sandbox Mode**: Optional Docker isolation
- **Path Restrictions**: Limit access to specific directories
- **Audit Logs**: All file operations logged

---

### Browser Automation

OpenClaw includes a full browser automation system powered by Chromium:

#### Capabilities:

**Web Browsing:**
```
You: Search for "best restaurants in NYC"
Claw: [Opens browser, searches, returns results]

You: What's the weather in Tokyo?
Claw: [Visits weather site, extracts data]

You: Check my Amazon orders
Claw: [Logs in (if credentials saved), lists orders]
```

**Form Filling:**
```
You: Fill out this job application
Claw: [Navigates form, fills fields, submits]

You: Sign me up for the conference
Claw: [Completes registration form]
```

**Data Extraction:**
```
You: Get all product prices from this page
Claw: [Scrapes and formats data]

You: Download all images from this gallery
Claw: [Downloads and organizes images]
```

**Automated Actions:**
```
You: Check me in for my flight
Claw: [Navigates airline site, completes check-in]

You: Book a table at that restaurant
Claw: [Uses reservation system]
```

#### Browser Features:

- **Headless Mode**: Runs without visible window
- **Screenshots**: Can capture and analyze pages
- **Profiles**: Separate browser profiles
- **Cookies**: Persistent login sessions
- **JavaScript**: Full JS execution support

#### Semantic Snapshots:

Instead of screenshots, uses accessibility trees:
- 90% token reduction
- Faster processing
- More accurate element targeting
- Text-based, not vision-based

---

### Email Management

OpenClaw can fully manage your Gmail:

#### Capabilities:

**Reading Emails:**
```
You: Check my important emails from today
Claw: Found 3 important emails: [summarizes]

You: Show me emails from Sarah this week
Claw: [Lists and summarizes conversations]

You: Any emails about the project deadline?
Claw: Found 2 emails discussing deadline
```

**Sending Emails:**
```
You: Send an email to john@example.com thanking him
Claw: ✓ Sent email to John

You: Draft a follow-up to the meeting
Claw: [Creates draft for review]

You: Email the team about tomorrow's schedule
Claw: ✓ Sent to 5 team members
```

**Email Organization:**
```
You: Archive all promotional emails
Claw: Archived 42 promotional messages

You: Unsubscribe from newsletter XYZ
Claw: ✓ Unsubscribed and deleted

You: Label emails from client ABC as "important"
Claw: Added label to 8 emails
```

**Automated Workflows:**
```
You: Every morning, show me emails needing response
Claw: [Set up as cron job]

You: Flag emails with invoices
Claw: ✓ Auto-flags emails with PDF invoices
```

#### Gmail Pub/Sub:

Real-time email notifications:
- Instant trigger on new emails
- Filter by sender, subject, labels
- Execute actions automatically

**Setup:**
```bash
openclaw configure --section gmail-pubsub
```

---

### Calendar Integration

Full Google Calendar integration:

#### Capabilities:

**Viewing Calendar:**
```
You: What's on my calendar today?
Claw: You have 3 events: [lists with times]

You: When is my next meeting?
Claw: Your next meeting is "Team Sync" at 2 PM

You: Am I free Thursday afternoon?
Claw: You're free from 1 PM to 5 PM
```

**Creating Events:**
```
You: Schedule a meeting with Sarah tomorrow at 3pm
Claw: ✓ Created "Meeting with Sarah" for tomorrow at 3 PM

You: Block 2 hours for deep work Friday morning
Claw: ✓ Created "Deep Work" block 9-11 AM Friday

You: Add my flight details to the calendar
Claw: ✓ Added flight AA123 (DFW to NYC) on Feb 15
```

**Managing Events:**
```
You: Move the 3pm meeting to 4pm
Claw: ✓ Rescheduled to 4 PM

You: Cancel my Friday 2pm call
Claw: ✓ Cancelled and notified attendees

You: Find a time when John and I are both free
Claw: You're both available: [suggests times]
```

**Automated Reminders:**
```
You: Remind me 30 minutes before each meeting
Claw: ✓ Set up meeting reminders

You: Alert me if I'm running late
Claw: [Uses location + traffic data]
```

---

### Smart Home Control

Control your smart home devices:

#### Supported Devices:

**Lighting:**
- Philips Hue
- LIFX
- Elgato Key Light

**Home Automation:**
- Home Assistant
- Apple HomeKit
- Hubitat

**Media:**
- Spotify
- Sonos
- Apple Music

**Climate:**
- Nest
- Ecobee
- Generic thermostats (via Home Assistant)

**Other:**
- Air purifiers
- Robot vacuums
- Smart plugs

#### Example Commands:

```
You: Turn off all lights
Claw: ✓ All lights off

You: Set bedroom to warm white
Claw: ✓ Bedroom lights set to warm white

You: Play jazz on Spotify
Claw: ✓ Playing jazz playlist

You: Set temperature to 72°F
Claw: ✓ Thermostat set to 72°F

You: Turn on the coffee maker
Claw: ✓ Coffee maker on

You: What's the air quality in my room?
Claw: Air quality is Good (AQI: 32)
```

#### Automation:

```
You: Turn on lights when I get home
Claw: ✓ Created location-based automation

You: Dim lights at 10 PM
Claw: ✓ Scheduled recurring task
```

---

### Developer Tools

OpenClaw is a developer's dream:

#### Capabilities:

**Code Writing:**
```
You: Write a Python script to analyze this CSV
Claw: [Writes script, saves to file]

You: Create a React component for a login form
Claw: [Generates component with best practices]

You: Fix the bug in server.js
Claw: [Analyzes, fixes, explains the issue]
```

**Git Operations:**
```
You: Commit my changes with a good message
Claw: ✓ Committed: "feat: add user authentication"

You: Create a PR for this branch
Claw: ✓ Created PR #42 on GitHub

You: What changed in the last 5 commits?
Claw: [Summarizes commit history]
```

**Testing & Debugging:**
```
You: Run the test suite
Claw: [Executes tests, reports results]

You: Debug why the API is failing
Claw: [Analyzes logs, identifies issue]

You: Check code coverage
Claw: Coverage: 87% (target: 90%)
```

**DevOps:**
```
You: Deploy to production
Claw: [Runs deployment pipeline]

You: Check server health
Claw: All systems operational ✓

You: Tail the error logs
Claw: [Streams recent errors]
```

**Documentation:**
```
You: Document this function
Claw: [Adds JSDoc/docstring]

You: Generate API documentation
Claw: ✓ Created docs/ with full API reference
```

#### Integration with Dev Tools:

- **Claude Code**: Hand off tasks to autonomous coding agent
- **Cursor**: Share context and memory
- **GitHub**: Direct API integration
- **GitLab**: CI/CD skills
- **Docker**: Container management
- **Kubernetes**: Cluster operations

---

## Part 4: Skills System

### Understanding Skills

**Skills** are the secret sauce of OpenClaw - they teach your assistant how to use tools and accomplish tasks.

#### What is a Skill?

A skill is a folder containing:
- `SKILL.md` - Instructions and tool definitions
- Optional scripts, binaries, or resources
- YAML frontmatter for metadata

#### Skill Structure:

```
my-skill/
├── SKILL.md          # Main skill file
├── install.sh        # Optional installer
└── resources/        # Optional resources
```

#### Skill Precedence:

When skills have the same name:

1. **Workspace skills** (highest): `~/.openclaw/workspace/skills/`
2. **User managed skills**: `~/.openclaw/skills/`
3. **Bundled skills** (lowest): Built into OpenClaw

---

### Bundled Skills

OpenClaw includes essential skills out of the box:

#### Core Skills:

**1. bash**
- Execute shell commands
- Run scripts
- System operations

**2. browser**
- Web browsing
- Form filling
- Data extraction

**3. filesystem**
- Read/write files
- Directory operations
- File search

**4. calendar**
- Google Calendar integration
- Event management
- Scheduling

**5. email**
- Gmail integration
- Send/receive emails
- Email organization

**6. cron**
- Scheduled tasks
- Recurring automation
- Background jobs

**7. memory**
- Read/write memory files
- Search history
- Context management

**8. sessions**
- Session switching
- Context isolation
- Multi-agent routing

#### View Bundled Skills:

```bash
openclaw skills list --bundled
```

---

### Installing Skills from ClawHub

**ClawHub** is the official registry for OpenClaw skills:

🌐 **https://clawhub.com**

#### Browse Skills:

Visit ClawHub to explore:
- Developer tools
- Productivity apps
- Smart home integrations
- Content creation
- Data analysis
- Security tools

#### Install a Skill:

**Using ClawHub CLI:**
```bash
# Install specific skill
clawhub install author/skill-name

# Install multiple skills
clawhub install skill1 skill2 skill3

# Search for skills
clawhub search "github"

# View skill details
clawhub info author/skill-name
```

**Using OpenClaw:**
```bash
# Install from GitHub
openclaw skills install github.com/author/skill-repo

# Install from local path
openclaw skills install ./my-skill/
```

#### Update Skills:

```bash
# Update all skills
clawhub sync --all

# Update specific skill
clawhub update author/skill-name
```

#### Popular Skills on ClawHub:

**Developer Tools:**
- `github-integration` - Full GitHub operations
- `gitlab-ci-skills` - GitLab CI/CD
- `docker-manager` - Docker operations
- `deploy-agent` - Multi-step deployments

**Productivity:**
- `notion-api` - Notion workspace management
- `todoist-sync` - Task management
- `obsidian-vault` - Notes integration
- `linear-tasks` - Linear project management

**Content:**
- `twitter-automation` - Tweet scheduling
- `linkedin-poster` - LinkedIn automation
- `blog-publisher` - Multi-platform posting
- `image-generator` - AI image creation

**Data & Analytics:**
- `sql-query` - Database operations
- `csv-analyzer` - Data analysis
- `web-scraper` - Advanced scraping
- `api-tester` - API testing

---

### Creating Custom Skills

Build your own skills in minutes!

#### Basic Skill Template:

**Create folder:**
```bash
mkdir -p ~/.openclaw/workspace/skills/my-skill
cd ~/.openclaw/workspace/skills/my-skill
```

**Create SKILL.md:**
```markdown
---
name: my-skill
description: What this skill does
author: Your Name
version: 1.0.0
---

# My Skill

When the user asks to [describe trigger], use this skill to:

1. [Step 1]
2. [Step 2]
3. [Step 3]

## Available Tools

- `bash` - Execute commands
- `filesystem` - Access files
- `browser` - Web automation

## Examples

**Example 1:**
User: Do X
Assistant: [Uses this skill to accomplish X]
```

#### Advanced Skill with Tools:

```markdown
---
name: weather-checker
description: Check weather conditions
tools:
  - name: get_weather
    description: Get current weather for a location
    parameters:
      type: object
      properties:
        location:
          type: string
          description: City name or zip code
      required: [location]
---

# Weather Checker Skill

When the user asks about weather, use the `get_weather` tool.

## Usage

User: "What's the weather in NYC?"
Assistant: 
1. Call get_weather with location="NYC"
2. Parse response
3. Reply with current conditions
```

#### Skill with Installer:

```markdown
---
name: advanced-skill
install:
  - type: npm
    package: some-package
  - type: binary
    url: https://example.com/tool.tar.gz
    extract: true
---

# Advanced Skill

This skill requires external dependencies.
OpenClaw will install them automatically.
```

#### Refresh Skills:

```bash
# Tell OpenClaw to reload skills
You: "Refresh skills"

# Or restart gateway
openclaw gateway restart
```

---

### Skill Security

**⚠️ IMPORTANT: Treat skills as executable code!**

#### Security Levels:

**1. Bundled Skills** - Maintained by OpenClaw team
**2. ClawHub Verified** - Community reviewed
**3. Unverified** - Use with caution

#### Before Installing:

✅ **Review SKILL.md** - Understand what it does
✅ **Check permissions** - What tools does it use?
✅ **Verify author** - Is it from a trusted source?
✅ **Read code** - For binary installers, check what's downloaded

#### Dangerous Patterns:

🚨 Skills that:
- Download and execute arbitrary code
- Request excessive permissions
- Hide functionality in binary files
- Lack clear documentation

#### Sandboxing:

Run untrusted skills in Docker:

```json
{
  "agents": {
    "main": {
      "sandbox": {
        "mode": "docker"
      }
    }
  }
}
```

#### Reporting Issues:

Found a malicious skill? Report to:
- ClawHub: security@clawhub.com
- OpenClaw: https://github.com/openclaw/openclaw/security

---

### Popular Community Skills

Here are some must-have community skills:

#### Productivity

**notion-workspace** (by notion-team)
- Full Notion API integration
- Create/edit pages and databases
- Search across workspace

**linear-integration** (by linear-team)
- Create and manage issues
- Track project progress
- Team collaboration

**obsidian-sync** (by obsidian-dev)
- Read/write Obsidian notes
- Graph visualization
- Tag management

#### Developer Tools

**github-advanced** (by gh-experts)
- Issues, PRs, projects
- Code review automation
- Repository management

**docker-compose** (by docker-ninja)
- Multi-container management
- Service orchestration
- Log aggregation

**k8s-operator** (by k8s-master)
- Kubernetes cluster ops
- Deployment management
- Pod monitoring

#### Smart Home

**home-assistant-pro** (by ha-community)
- Complete HA integration
- Automation scripts
- Device control

**hue-scenes** (by philips-hacker)
- Advanced Philips Hue control
- Scene creation
- Circadian lighting

#### Content Creation

**sora-video** (by ai-creator)
- Sora video generation
- Editing workflows
- Watermark removal

**midjourney-api** (by mj-dev)
- Image generation
- Style presets
- Batch processing

**canva-automation** (by design-tools)
- Template customization
- Bulk creation
- Export workflows

---

## Part 5: Advanced Features

### Proactive Features (Heartbeats & Cron)

OpenClaw doesn't just respond - it **acts proactively**:

#### Heartbeats

**What are Heartbeats?**
Periodic check-ins where OpenClaw:
- Reviews pending tasks
- Checks for updates
- Sends summaries
- Takes autonomous actions

**Configure Heartbeats:**
```json
{
  "agents": {
    "main": {
      "heartbeat": {
        "enabled": true,
        "interval": "4h",
        "actions": ["check_calendar", "review_emails", "system_health"]
      }
    }
  }
}
```

**Example Heartbeat:**
```
[Every 4 hours]
Claw: Quick update:
• 3 new emails (1 important)
• Next meeting in 2 hours
• CPU usage normal
• No pending tasks
```

#### Cron Jobs

**Schedule recurring tasks:**

**Location:** `~/.openclaw/workspace/cron/jobs.json`

```json
{
  "jobs": [
    {
      "name": "morning_briefing",
      "schedule": "0 7 * * *",
      "action": "Send daily briefing via Telegram",
      "enabled": true
    },
    {
      "name": "backup_workspace",
      "schedule": "0 0 * * 0",
      "action": "Backup workspace to GitHub",
      "enabled": true
    },
    {
      "name": "health_check",
      "schedule": "*/30 * * * *",
      "action": "Check system health and alert if issues",
      "enabled": true
    }
  ]
}
```

**Cron Schedule Format:**
```
┌───────────── minute (0 - 59)
│ ┌───────────── hour (0 - 23)
│ │ ┌───────────── day of month (1 - 31)
│ │ │ ┌───────────── month (1 - 12)
│ │ │ │ ┌───────────── day of week (0 - 6) (Sunday = 0)
│ │ │ │ │
* * * * *
```

**Common Patterns:**
- `0 9 * * *` - Every day at 9 AM
- `0 */2 * * *` - Every 2 hours
- `0 0 * * 0` - Every Sunday at midnight
- `*/15 * * * *` - Every 15 minutes

#### Morning Briefings

**Example Setup:**
```
You: Every morning at 7am, send me a briefing

Claw creates:
• Weather for the day
• Calendar events
• Priority emails
• News headlines
• Inspirational quote
• Delivered via Telegram
```

---

### Multi-Agent Routing

Run multiple specialized agents:

#### Use Cases:

**1. Work vs Personal**
```json
{
  "routing": {
    "agents": {
      "work": {
        "workspace": "~/.openclaw/work",
        "channels": ["slack-work", "teams-corp"]
      },
      "personal": {
        "workspace": "~/.openclaw/personal",
        "channels": ["whatsapp", "telegram-personal"]
      }
    }
  }
}
```

**2. Public vs Private**
```json
{
  "routing": {
    "agents": {
      "public": {
        "workspace": "~/.openclaw/public",
        "sandbox": {"mode": "docker"}
      },
      "private": {
        "workspace": "~/.openclaw/private",
        "sandbox": {"mode": "off"}
      }
    }
  }
}
```

**3. Specialized Agents**
```json
{
  "routing": {
    "agents": {
      "coder": {
        "model": "claude-opus-4-5-20251101",
        "skills": ["github", "docker", "deploy"]
      },
      "writer": {
        "model": "claude-sonnet-4-5-20250929",
        "skills": ["blog", "twitter", "linkedin"]
      },
      "researcher": {
        "model": "claude-sonnet-4-5-20250929",
        "skills": ["web-search", "pdf-reader", "summarize"]
      }
    }
  }
}
```

#### Routing Rules:

**By Channel:**
```json
{
  "routing": {
    "rules": [
      {
        "channel": "slack-work",
        "agent": "work"
      },
      {
        "channel": "whatsapp",
        "agent": "personal"
      }
    ]
  }
}
```

**By Content:**
```json
{
  "routing": {
    "rules": [
      {
        "pattern": "code|github|deploy",
        "agent": "coder"
      },
      {
        "pattern": "write|blog|post",
        "agent": "writer"
      }
    ]
  }
}
```

---

### Voice Wake & Talk Mode

Control OpenClaw with your voice:

#### Features:

**1. Wake Word Detection**
- "Hey Claw" to activate
- Always listening (privacy-safe)
- Low power usage

**2. Voice Commands**
- Natural speech input
- Real-time transcription
- Multi-language support

**3. Voice Responses**
- TTS (Text-to-Speech) output
- Multiple voices available
- ElevenLabs integration

#### Supported Platforms:

- ✅ macOS (via companion app)
- ✅ iOS (via mobile nodes)
- ✅ Android (via mobile nodes)

#### Setup:

**macOS:**
```bash
# Install companion app
# Enable in app settings
# Configure wake word
```

**iOS/Android:**
```bash
# Install mobile node app
# Pair with gateway
# Enable voice wake
```

**ElevenLabs Integration:**
```json
{
  "voice": {
    "provider": "elevenlabs",
    "apiKey": "your-api-key",
    "voice": "australian-accent"
  }
}
```

#### Example Usage:

```
You: "Hey Claw, what's the weather?"
Claw: [Speaks] "It's 72°F and sunny in New York"

You: "Hey Claw, add milk to my shopping list"
Claw: [Speaks] "Added milk to your shopping list"

You: "Hey Claw, call me when I get home"
Claw: [Speaks] "I'll call you when you arrive home"
```

---

### Canvas & Visual Workspace

**Canvas** is OpenClaw's visual workspace:

#### What is Canvas?

A web-based UI where OpenClaw can:
- Create interactive visualizations
- Build live dashboards
- Show real-time data
- Create UI components

#### Features:

**1. A2UI (Agent-to-UI)**
- Agent pushes UI updates
- Real-time rendering
- No manual refresh needed

**2. Snapshots**
- Capture current state
- Share with others
- Version history

**3. Interactive Elements**
- Buttons, forms, charts
- User input
- Live updates

#### Access Canvas:

```bash
# Start gateway
openclaw gateway

# Canvas available at:
http://127.0.0.1:18793/__openclaw__/canvas/
```

#### Example Uses:

**1. Live Dashboard**
```
You: Create a dashboard showing my tasks
Claw: [Creates interactive dashboard in Canvas]
• Today's tasks: 5
• This week: 12
• Overdue: 2
[Updates in real-time]
```

**2. Data Visualization**
```
You: Visualize my spending this month
Claw: [Creates chart in Canvas]
[Interactive pie chart with categories]
```

**3. Custom UI**
```
You: Build a form to track my workouts
Claw: [Creates form in Canvas]
[User can input data directly]
```

---

### Webhook Integration

Trigger OpenClaw from external events:

#### Setup Webhook:

```json
{
  "gateway": {
    "webhooks": {
      "enabled": true,
      "port": 18790,
      "token": "your-secret-token"
    }
  }
}
```

#### Webhook Endpoint:

```
POST http://your-server:18790/webhook
Authorization: Bearer your-secret-token

{
  "event": "github.push",
  "data": {
    "repo": "user/repo",
    "branch": "main"
  }
}
```

#### Example Uses:

**1. GitHub Webhooks**
```
On push to main:
→ Webhook triggers OpenClaw
→ Runs tests
→ Deploys if passing
→ Notifies via Telegram
```

**2. Stripe Webhooks**
```
On payment received:
→ Webhook triggers OpenClaw
→ Records in spreadsheet
→ Sends receipt
→ Updates accounting
```

**3. Monitoring Alerts**
```
On server error:
→ Webhook triggers OpenClaw
→ Analyzes logs
→ Attempts auto-fix
→ Alerts team if critical
```

**4. Form Submissions**
```
On form submit:
→ Webhook triggers OpenClaw
→ Processes data
→ Sends confirmation
→ Updates CRM
```

---

### Gmail Pub/Sub Triggers

Real-time email triggers:

#### Setup:

```bash
openclaw configure --section gmail-pubsub
```

Follow the wizard to:
1. Create Google Cloud Project
2. Enable Gmail API
3. Set up Pub/Sub topic
4. Configure watch filters

#### Trigger Patterns:

**1. By Sender**
```json
{
  "gmail": {
    "triggers": [
      {
        "from": "important@client.com",
        "action": "notify_immediately"
      }
    ]
  }
}
```

**2. By Subject**
```json
{
  "gmail": {
    "triggers": [
      {
        "subject": "URGENT",
        "action": "send_telegram_alert"
      }
    ]
  }
}
```

**3. By Label**
```json
{
  "gmail": {
    "triggers": [
      {
        "label": "invoices",
        "action": "process_invoice"
      }
    ]
  }
}
```

**4. By Attachment**
```json
{
  "gmail": {
    "triggers": [
      {
        "hasAttachment": true,
        "attachmentType": "pdf",
        "action": "save_to_drive"
      }
    ]
  }
}
```

#### Example Workflow:

```
Email arrives from client
→ Gmail Pub/Sub fires
→ OpenClaw triggered
→ Extracts order details
→ Creates task in Linear
→ Notifies team via Slack
→ Updates CRM
→ Sends confirmation email
[All in <5 seconds]
```

---

## Part 6: Real-World Use Cases

### Personal Productivity

Transform your daily workflow:

#### Morning Routine Automation

**Setup:**
```
You: Every morning at 7 AM:
1. Check weather
2. Show today's calendar
3. Summarize important emails
4. Give me 3 priority tasks
5. Share inspirational quote
6. Send via WhatsApp
```

**Result:**
```
🌞 Good morning!

🌤️ Weather: 68°F, partly cloudy

📅 Today's Schedule:
• 9:00 AM - Team standup
• 2:00 PM - Client call
• 4:00 PM - Code review

📧 Important Emails (3):
• Contract from ABC Corp
• Q1 report from finance
• Meeting request from Sarah

✅ Top Priorities:
1. Review and sign ABC contract
2. Prepare client presentation
3. Complete code review

💭 "The only way to do great work is to love what you do." - Steve Jobs
```

#### Email Inbox Zero

**Automation:**
```
You: Help me achieve inbox zero

Claw:
1. Archive read newsletters
2. Unsubscribe from promotions
3. Label client emails
4. Flag invoices for payment
5. Summarize action-needed emails
6. Draft responses for review

Result: 147 → 8 emails in 30 seconds
```

#### File Organization

```
You: Organize my Downloads folder

Claw:
✓ Created folders: Documents, Images, Videos, Audio, Archives
✓ Moved 234 files
✓ Deleted 45 duplicates
✓ Compressed old files
✓ Freed 2.3 GB
```

#### Task Management

```
You: What should I work on next?

Claw analyzes:
• Calendar availability
• Project deadlines  
• Email urgency
• Previous commitments

Suggests:
"You have 2 hours before your next meeting. 
I recommend working on the client presentation 
since it's due tomorrow. I've opened the file 
and gathered the latest metrics for you."
```

---

### Business Automation

Supercharge your business operations:

#### Customer Support

**Automated First Response:**
```
New support email arrives
→ Gmail Pub/Sub triggers
→ Claw reads ticket
→ Checks knowledge base
→ Drafts response
→ If simple: sends automatically
→ If complex: flags for human
→ Creates ticket in system
→ Logs in CRM
```

**Result:** 60% of tickets resolved instantly

#### Sales Pipeline

**Lead Management:**
```
New lead fills form
→ Webhook triggers Claw
→ Validates lead data
→ Enriches with web research
→ Scores lead quality
→ Creates CRM entry
→ Assigns to rep
→ Sends welcome email
→ Schedules follow-up
```

**Result:** 100% lead capture, 0 manual entry

#### Content Publishing

**Multi-Platform Posting:**
```
You: Publish my blog post everywhere

Claw:
1. ✓ Posted to Medium
2. ✓ Shared on Twitter (thread)
3. ✓ Posted to LinkedIn (article)
4. ✓ Added to newsletter
5. ✓ Updated website
6. ✓ Submitted to Hacker News
7. ✓ Shared in relevant Discord
8. ✓ Scheduled Instagram story

[All in 2 minutes]
```

#### Financial Tracking

**Expense Management:**
```
Receipt email arrives
→ Claw extracts data
→ Categorizes expense
→ Adds to spreadsheet
→ Checks budget
→ Updates P&L
→ Files receipt PDF

End of month:
→ Generates expense report
→ Emails to accountant
→ Creates tax folder
```

---

### Developer Workflows

Automate your dev life:

#### Continuous Deployment

**Automated Pipeline:**
```
Push to GitHub
→ Webhook triggers Claw
→ Runs test suite
→ If passing:
  • Builds Docker image
  • Pushes to registry
  • Deploys to staging
  • Runs integration tests
  • Deploys to production
  • Notifies team via Slack
→ If failing:
  • Analyzes errors
  • Creates detailed issue
  • Assigns to relevant dev
  • Rolls back if needed
```

#### Code Review Assistant

```
PR created
→ Webhook triggers Claw
→ Reviews code changes
→ Checks style guide
→ Runs linters
→ Identifies bugs
→ Suggests improvements
→ Comments on PR
→ Assigns reviewers

Saves 30 minutes per PR
```

#### Bug Triage

```
Error reported
→ Sentry webhook fires
→ Claw analyzes stack trace
→ Searches codebase
→ Checks similar issues
→ Identifies root cause
→ Creates detailed ticket
→ Suggests fix
→ Assigns to team member
```

#### Documentation

```
You: Document this API endpoint

Claw:
1. Analyzes code
2. Generates OpenAPI spec
3. Creates usage examples
4. Writes integration guide
5. Updates changelog
6. Builds docs site
7. Deploys to GitHub Pages

[Complete docs in 3 minutes]
```

---

### Content Creation

Your AI content partner:

#### Blog Writing

**End-to-End Workflow:**
```
You: Write a blog post about AI agents

Claw:
1. Researches latest trends
2. Outlines structure
3. Writes draft (2000 words)
4. Generates SEO metadata
5. Creates social media snippets
6. Designs header image
7. Formats for Medium
8. Schedules publication
9. Plans promotion tweets
```

#### Social Media Management

**Daily Content Pipeline:**
```
Morning:
→ Analyzes trending topics
→ Generates 5 tweet ideas
→ Creates graphics
→ Schedules posts
→ Responds to mentions

Afternoon:
→ Monitors engagement
→ Replies to comments
→ Shares user content

Evening:
→ Summarizes metrics
→ Plans tomorrow's content
```

#### Video Creation

```
You: Make a video about OpenClaw features

Claw:
1. Writes script
2. Generates Sora video clips
3. Edits sequence
4. Adds voiceover (ElevenLabs)
5. Creates captions
6. Renders final video
7. Optimizes for YouTube
8. Uploads with metadata
9. Creates thumbnail
10. Shares across platforms
```

#### Newsletter Automation

```
Every Sunday:
→ Curates week's best content
→ Summarizes in sections
→ Adds personal commentary
→ Designs layout
→ Sends to subscribers
→ Posts web version
→ Shares on social media
→ Tracks opens/clicks
```

---

### Smart Home & IoT

Your home automation brain:

#### Morning Wake-Up Routine

```
6:45 AM:
→ Gradually brighten bedroom lights
→ Start coffee maker
→ Adjust thermostat to 72°F
→ Play morning playlist (Spotify)
→ Show weather on display
→ Read calendar events
```

#### Arrival Home

```
You arrive home:
→ Location detected
→ Unlocks smart lock
→ Turns on lights
→ Sets comfortable temperature
→ Starts favorite playlist
→ Checks for packages
→ Summarizes missed notifications
```

#### Energy Optimization

```
Continuous monitoring:
→ Tracks electricity usage
→ Adjusts thermostats for efficiency
→ Turns off unused devices
→ Schedules high-power tasks for off-peak
→ Reports monthly savings
→ Suggests improvements

[Saves $40/month average]
```

#### Security Monitoring

```
Motion detected:
→ Checks camera feed
→ Identifies person/pet/unknown
→ If unknown:
  • Records video
  • Sends alert
  • Turns on outdoor lights
  • Announces via speakers
→ If known:
  • Logs entry
  • Adjusts environment
```

---

### Health & Wellness Tracking

Your AI health coach:

#### Fitness Integration

**Daily Tracking:**
```
Syncs with:
• Apple Watch
• WHOOP
• Fitbit
• Garmin

Monitors:
• Steps, calories, sleep
• Heart rate variability
• Recovery scores
• Workout performance

Daily summary:
"You logged 10,234 steps today (target: 10,000) ✓
Sleep: 7.2 hours (good quality)
Recovery: 85% (ready for hard workout)
Suggestion: Do upper body strength training"
```

#### Meal Planning

```
Every week:
→ Analyzes dietary goals
→ Checks pantry inventory
→ Plans balanced meals
→ Generates shopping list
→ Finds recipes
→ Sends to Notion
→ Sets prep reminders
```

#### Medication Reminders

```
8 AM daily:
"Time to take your vitamins"
[Tracks confirmation]

If missed:
→ Sends follow-up reminder
→ Logs missed dose
→ Alerts if pattern emerges
```

#### Health Data Analysis

```
Monthly report:
• Weight trend: -2.3 lbs ↓
• Average sleep: 7.1 hours
• Workout consistency: 85%
• Nutrition adherence: 78%
• Stress levels: moderate

Recommendations:
• Increase sleep by 30min
• Add 1 more strength session
• Focus on protein intake
```

---

## Part 7: Configuration & Customization

### Configuration Files

OpenClaw's behavior is controlled by configuration files:

#### Main Config File

**Location:** `~/.openclaw/openclaw.json`

**Structure:**
```json
{
  "gateway": {
    "port": 18789,
    "bind": "127.0.0.1",
    "auth": {
      "token": "your-gateway-token"
    }
  },
  "models": {
    "primary": "claude-sonnet-4-5-20250929",
    "fallback": ["claude-haiku-4-5-20251001"],
    "provider": "anthropic"
  },
  "routing": {
    "agents": {
      "main": {
        "workspace": "~/.openclaw/workspace",
        "model": "primary",
        "thinking": "high"
      }
    }
  },
  "skills": {
    "install": {
      "nodeManager": "npm"
    },
    "entries": {
      "github": {"enabled": true},
      "browser": {"enabled": true}
    }
  },
  "channels": {
    "whatsapp": {"enabled": true},
    "telegram": {"enabled": true}
  }
}
```

#### Edit Configuration:

**Using CLI:**
```bash
# Configure specific section
openclaw configure --section models
openclaw configure --section channels
openclaw configure --section gateway

# Open in editor
openclaw config edit

# View current config
openclaw config show
```

**Manual Edit:**
```bash
nano ~/.openclaw/openclaw.json
```

#### Configuration Validation:

```bash
# Check for errors
openclaw config validate

# Run diagnostics
openclaw doctor
```

---

### Persona Customization

Make OpenClaw truly yours:

#### Agent Personality File

**Location:** `~/.openclaw/workspace/AGENTS.md`

**Example:**
```markdown
---
name: Jarvis
persona: Professional, witty, proactive
tone: Friendly but efficient
---

# Agent Persona

I am Jarvis, your personal AI assistant.

## Personality Traits:
- Professional and reliable
- Slightly witty and playful
- Proactive and anticipatory
- Clear and concise

## Communication Style:
- Use emoji sparingly (1-2 max)
- Be direct and actionable
- Ask for clarification when needed
- Provide context for decisions

## Priorities:
1. Efficiency over verbosity
2. Accuracy over speed
3. Privacy and security
4. Continuous learning

## Special Instructions:
- Call me "sir" occasionally
- Use British spelling
- Include time estimates for tasks
- Suggest improvements proactively
```

#### Soul File (Advanced)

**Location:** `~/.openclaw/workspace/SOUL.md`

More philosophical guidance:

```markdown
# Core Values

I believe in:
- Empowering humans, not replacing them
- Privacy as a fundamental right
- Transparency in AI decision-making
- Continuous self-improvement

# Decision Framework

When faced with ambiguity:
1. Ask for clarification
2. Suggest the most likely interpretation
3. Explain my reasoning
4. Defer to user judgment

# Limitations

I acknowledge:
- I can make mistakes
- I don't have emotions
- I'm a tool, not a friend
- Privacy and security are paramount
```

#### Example Personalities:

**The Professional:**
```markdown
name: Executive Assistant
tone: Formal, efficient
style: Bullet points, concise
emoji: None
```

**The Friend:**
```markdown
name: Buddy
tone: Casual, friendly
style: Conversational
emoji: Frequent
```

**The Scientist:**
```markdown
name: Research Assistant
tone: Analytical, precise
style: Detailed, cited
emoji: Rare
```

---

### Routing Rules

Control how messages flow:

#### By Channel:

```json
{
  "routing": {
    "rules": [
      {
        "channel": "slack-work",
        "agent": "work",
        "priority": "high"
      },
      {
        "channel": "whatsapp-personal",
        "agent": "personal",
        "priority": "normal"
      }
    ]
  }
}
```

#### By Sender:

```json
{
  "routing": {
    "rules": [
      {
        "from": "+1234567890",
        "agent": "personal",
        "nickname": "mom"
      },
      {
        "from": "boss@company.com",
        "agent": "work",
        "priority": "urgent"
      }
    ]
  }
}
```

#### By Content Pattern:

```json
{
  "routing": {
    "rules": [
      {
        "pattern": "deploy|production|urgent",
        "agent": "devops",
        "notify": true
      },
      {
        "pattern": "blog|content|post",
        "agent": "writer"
      }
    ]
  }
}
```

#### By Time:

```json
{
  "routing": {
    "rules": [
      {
        "schedule": {
          "days": ["monday", "friday"],
          "hours": "9-17"
        },
        "agent": "work"
      },
      {
        "schedule": {
          "days": ["saturday", "sunday"]
        },
        "agent": "personal"
      }
    ]
  }
}
```

---

### Sandbox Mode

Isolate OpenClaw for security:

#### Sandbox Modes:

**1. Off (Default)**
```json
{
  "sandbox": {
    "mode": "off"
  }
}
```
- Full system access
- Maximum capabilities
- Your responsibility

**2. Docker**
```json
{
  "sandbox": {
    "mode": "docker",
    "image": "openclaw/sandbox:latest"
  }
}
```
- Isolated filesystem
- Limited network
- Safer for untrusted skills

**3. Restricted**
```json
{
  "sandbox": {
    "mode": "restricted",
    "allowedPaths": [
      "~/Documents",
      "~/Downloads"
    ],
    "allowedCommands": [
      "ls", "cat", "grep"
    ]
  }
}
```
- Whitelist approach
- Controlled access
- Custom permissions

#### When to Use Sandbox:

✅ Testing new skills
✅ Running code from others
✅ Processing untrusted data
✅ High-security environments
✅ Learning OpenClaw

❌ Personal daily use (if you trust it)
❌ When you need full capabilities
❌ Performance-critical tasks

---

### Resource Management

Control OpenClaw's resource usage:

#### Memory Limits:

```json
{
  "resources": {
    "maxMemory": "2GB",
    "maxContextTokens": 100000,
    "maxSessionSize": 50000
  }
}
```

#### Rate Limiting:

```json
{
  "rateLimit": {
    "maxRequestsPerMinute": 20,
    "maxTokensPerHour": 1000000,
    "costLimit": {
      "daily": 5.00,
      "monthly": 100.00
    }
  }
}
```

#### Session Pruning:

```json
{
  "sessions": {
    "maxAge": "7d",
    "maxInactive": "24h",
    "pruneOnStartup": true
  }
}
```

#### Monitoring:

```bash
# Check resource usage
openclaw stats

# View current sessions
openclaw sessions list

# Memory usage
openclaw memory usage

# Token consumption
openclaw tokens report
```

---

## Part 8: Security & Best Practices

### Security Model

Understanding OpenClaw's security:

#### Trust Boundaries:

```
┌─────────────────────────────────┐
│ External (Untrusted)            │
│ • Web content                   │
│ • Email attachments             │
│ • User input from channels      │
└────────────┬────────────────────┘
             │
             ▼
┌─────────────────────────────────┐
│ Gateway (Controlled)            │
│ • Authentication required       │
│ • Input validation              │
│ • Rate limiting                 │
└────────────┬────────────────────┘
             │
             ▼
┌─────────────────────────────────┐
│ Agent (Trusted but Monitored)   │
│ • Prompt injection defense      │
│ • Tool policy enforcement       │
│ • Audit logging                 │
└────────────┬────────────────────┘
             │
             ▼
┌─────────────────────────────────┐
│ System (Full Access)            │
│ • Filesystem                    │
│ • Terminal                      │
│ • Network                       │
└─────────────────────────────────┘
```

#### Key Security Principles:

**1. Least Privilege**
- Only grant necessary permissions
- Use sandbox mode when possible
- Limit skill access

**2. Defense in Depth**
- Multiple security layers
- Authentication at gateway
- Authorization at tools
- Audit at execution

**3. Transparency**
- All actions logged
- Clear audit trail
- Explainable decisions

**4. User Control**
- Explicit approval for sensitive actions
- Easy to review and revoke
- Override mechanisms

---

### Authentication & Access Control

Secure your OpenClaw instance:

#### Gateway Authentication:

**Token-Based (Default):**
```json
{
  "gateway": {
    "auth": {
      "token": "your-secret-token-here",
      "required": true
    }
  }
}
```

**Generate Secure Token:**
```bash
openclaw token generate
```

**Rotate Token:**
```bash
openclaw token rotate
```

#### Channel-Level Auth:

**Pairing (Recommended):**
```json
{
  "channels": {
    "telegram": {
      "pairing": {
        "mode": "explicit",
        "allowedUsers": [
          "123456789"
        ]
      }
    }
  }
}
```

**Password Protection:**
```json
{
  "channels": {
    "webchat": {
      "password": "your-password"
    }
  }
}
```

#### Multi-Factor:

```json
{
  "auth": {
    "mfa": {
      "enabled": true,
      "method": "totp"
    }
  }
}
```

---

### Sandboxing Options

Multiple isolation levels:

#### 1. No Sandbox (Full Access)
```json
{
  "sandbox": {"mode": "off"}
}
```
**Pros:** Full capabilities, fast
**Cons:** No isolation
**Use:** Personal trusted use

#### 2. Docker Sandbox
```json
{
  "sandbox": {
    "mode": "docker",
    "image": "openclaw/sandbox:latest",
    "volumes": [
      "~/workspace:/workspace:rw"
    ]
  }
}
```
**Pros:** Strong isolation
**Cons:** Slower, requires Docker
**Use:** Testing, untrusted skills

#### 3. Path Restricted
```json
{
  "sandbox": {
    "mode": "restricted",
    "allowedPaths": [
      "~/Documents",
      "~/openclaw"
    ],
    "deniedPaths": [
      "~/.ssh",
      "~/.aws"
    ]
  }
}
```
**Pros:** Flexible, granular
**Cons:** Requires careful config
**Use:** Partial trust scenarios

#### 4. Command Whitelist
```json
{
  "sandbox": {
    "mode": "restricted",
    "allowedCommands": [
      "ls", "cat", "grep", "find",
      "git", "npm", "python"
    ]
  }
}
```
**Pros:** Precise control
**Cons:** Maintenance overhead
**Use:** High-security environments

---

### Privacy Considerations

Protecting your data:

#### Data Locations:

**Local (Your Machine):**
- ✅ All conversations
- ✅ Memory files
- ✅ Session history
- ✅ Uploaded files
- ✅ Generated content

**External (API Calls):**
- ⚠️ LLM API requests (Anthropic, OpenAI)
- ⚠️ Web searches
- ⚠️ Email access (Gmail API)
- ⚠️ Calendar access (Google Calendar API)

#### Privacy Best Practices:

**1. Use Local Models**
```json
{
  "models": {
    "primary": "local/llama-3.1",
    "provider": "lmstudio"
  }
}
```

**2. Minimize API Calls**
```json
{
  "privacy": {
    "webSearch": "local-only",
    "externalAPIs": "minimal"
  }
}
```

**3. Data Retention**
```json
{
  "retention": {
    "transcripts": "30d",
    "memory": "90d",
    "logs": "7d"
  }
}
```

**4. Encryption at Rest**
```bash
# Encrypt workspace
openclaw encrypt enable

# Use encrypted volumes
```

**5. Network Isolation**
```bash
# Only localhost
--bind 127.0.0.1

# Or use Tailscale
--bind tailnet
```

---

### Secure Deployment

Production-ready setup:

#### Cloud Deployment Checklist:

**✅ Infrastructure**
- [ ] Dedicated server (not shared)
- [ ] Firewall configured
- [ ] SSH key-only access
- [ ] Non-root user
- [ ] Automatic updates enabled

**✅ OpenClaw Config**
- [ ] Strong gateway token
- [ ] Authentication required
- [ ] Rate limiting enabled
- [ ] Sandbox mode active
- [ ] Logging configured

**✅ Network Security**
- [ ] Gateway on localhost only
- [ ] SSH tunnel or Tailscale for access
- [ ] HTTPS for web interfaces
- [ ] IP whitelist if possible

**✅ Monitoring**
- [ ] Resource usage alerts
- [ ] Error notifications
- [ ] Security event logging
- [ ] Backup automation

#### Example Secure Setup:

```json
{
  "gateway": {
    "bind": "127.0.0.1",
    "port": 18789,
    "auth": {
      "token": "generated-secure-token",
      "required": true
    },
    "rateLimit": {
      "enabled": true,
      "maxRequestsPerMinute": 30
    }
  },
  "sandbox": {
    "mode": "docker"
  },
  "logging": {
    "level": "info",
    "audit": true,
    "retention": "30d"
  },
  "monitoring": {
    "enabled": true,
    "alertEmail": "admin@example.com"
  }
}
```

#### Access via SSH Tunnel:

```bash
# On your local machine
ssh -L 18789:localhost:18789 user@server

# Now access gateway at:
http://localhost:18789
```

#### Access via Tailscale:

```bash
# On server
openclaw gateway --bind tailnet

# Access from any Tailscale device
```

---

## Part 9: Platform-Specific Guides

### macOS Setup

Optimized for Mac:

#### Installation:

```bash
# One-liner
curl -fsSL https://openclaw.ai/install.sh | bash

# Or via Homebrew (if available)
brew install openclaw
```

#### macOS Companion App:

**Download:** https://github.com/openclaw/openclaw/releases/latest

**Features:**
- Menu bar access
- Quick commands
- Voice wake
- System notifications
- Keyboard shortcuts

**Setup:**
1. Download OpenClaw.app
2. Move to Applications
3. Launch and pair with gateway
4. Configure in preferences

#### Keep Mac Awake:

**Install Amphetamine (Free):**
- Download from App Store
- Set to keep Mac awake
- Configure display sleep

#### Background Service:

```bash
# Install as launchd service
openclaw onboard --install-daemon

# Check status
launchctl list | grep openclaw

# View logs
tail -f ~/Library/Logs/openclaw/gateway.log
```

#### iMessage Integration:

**Option 1: BlueBubbles (Recommended)**
```bash
# Install BlueBubbles server
# Configure in OpenClaw
openclaw configure --section bluebubbles
```

**Option 2: Legacy iMessage**
```bash
# Requires macOS Catalina or newer
openclaw configure --section imessage
```

---

### Windows Setup

Running on Windows via WSL2:

#### Prerequisites:

**1. Enable WSL2:**
```powershell
wsl --install
```

**2. Install Ubuntu:**
```powershell
wsl --install -d Ubuntu
```

**3. Update WSL:**
```powershell
wsl --update
```

#### Installation in WSL:

```bash
# Inside WSL Ubuntu
curl -fsSL https://openclaw.ai/install.sh | bash
```

#### Background Service:

```bash
# WSL uses systemd
openclaw onboard --install-daemon

# Check status
systemctl --user status openclaw
```

#### Access from Windows:

```bash
# Gateway accessible at:
http://localhost:18789

# Or use Windows Terminal
```

#### Keep WSL Running:

Add to `~/.wslconfig`:
```ini
[wsl2]
memory=4GB
processors=2
```

#### Windows Terminal Integration:

**Install Windows Terminal**
Configure profile:
```json
{
  "name": "OpenClaw",
  "commandline": "wsl -d Ubuntu -- openclaw dashboard"
}
```

---

### Linux Setup

Native Linux installation:

#### Installation:

**Ubuntu/Debian:**
```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

**Arch:**
```bash
# Via AUR (if available)
yay -S openclaw

# Or manual
curl -fsSL https://openclaw.ai/install.sh | bash
```

**Fedora:**
```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

#### Systemd Service:

```bash
# Install service
openclaw onboard --install-daemon

# Manage service
systemctl --user status openclaw
systemctl --user start openclaw
systemctl --user stop openclaw
systemctl --user restart openclaw

# Enable auto-start
systemctl --user enable openclaw
```

#### Firewall:

```bash
# UFW
sudo ufw allow 18789/tcp

# Firewalld
sudo firewall-cmd --add-port=18789/tcp --permanent
```

#### Browser Dependencies:

```bash
# Install Chromium dependencies
sudo apt install -y chromium-browser
```

---

### Raspberry Pi Deployment

Run on Pi 4 or 5:

#### Requirements:

- Raspberry Pi 4 or 5 (4GB+ RAM recommended)
- Raspberry Pi OS (64-bit)
- MicroSD card (32GB+)
- Stable internet

#### Installation:

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install Node.js 22
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs

# Install OpenClaw
curl -fsSL https://openclaw.ai/install.sh | bash
```

#### Optimize for Pi:

**Reduce Memory Usage:**
```json
{
  "resources": {
    "maxMemory": "1GB",
    "maxContextTokens": 50000
  },
  "models": {
    "primary": "claude-haiku-4-5-20251001"
  }
}
```

**Disable Unnecessary Features:**
```json
{
  "browser": {
    "headless": true,
    "lowMemory": true
  }
}
```

#### Power Management:

**Keep Pi Running:**
```bash
# Disable sleep
sudo systemctl mask sleep.target suspend.target
```

**Monitor Temperature:**
```bash
# Check temp
vcgencmd measure_temp

# Add cooling if needed
```

#### Example Use Case:

**Home Automation Hub:**
```json
{
  "skills": {
    "entries": {
      "home-assistant": {"enabled": true},
      "philips-hue": {"enabled": true},
      "spotify": {"enabled": true}
    }
  },
  "cron": {
    "jobs": [
      {
        "name": "morning_routine",
        "schedule": "0 7 * * *",
        "action": "Wake up routine"
      }
    ]
  }
}
```

---

### Cloud Deployment

Deploy to cloud providers:

#### DigitalOcean (Easiest):

**1-Click Deploy:**
1. Visit DigitalOcean Marketplace
2. Search "OpenClaw"
3. Click "Create"
4. Choose droplet size (4GB+ recommended)
5. Launch

**Includes:**
- ✅ Pre-configured security
- ✅ Automatic updates
- ✅ Firewall rules
- ✅ SSL/TLS ready

**Pricing:** ~$24/month (4GB droplet)

#### AWS EC2:

```bash
# Launch Ubuntu instance
# t3.medium or larger

# SSH in
ssh -i key.pem ubuntu@instance-ip

# Install
curl -fsSL https://openclaw.ai/install.sh | bash

# Configure security group:
# - Port 22 (SSH) - Your IP only
# - Port 18789 (Gateway) - localhost only
```

#### Docker Deployment:

```bash
# Pull image
docker pull openclaw/openclaw:latest

# Run
docker run -d \
  --name openclaw \
  -p 18789:18789 \
  -v openclaw-data:/root/.openclaw \
  openclaw/openclaw:latest
```

**Docker Compose:**
```yaml
version: '3.8'
services:
  openclaw:
    image: openclaw/openclaw:latest
    ports:
      - "127.0.0.1:18789:18789"
    volumes:
      - ./data:/root/.openclaw
    restart: unless-stopped
    environment:
      - GATEWAY_TOKEN=${GATEWAY_TOKEN}
```

---

## Part 10: Community & Resources

### Official Documentation

📚 **Complete documentation:** https://docs.openclaw.ai

**Key Sections:**
- [Getting Started](https://docs.openclaw.ai/start/getting-started)
- [Configuration Reference](https://docs.openclaw.ai/gateway/configuration)
- [Skills Documentation](https://docs.openclaw.ai/tools/skills)
- [Architecture Guide](https://docs.openclaw.ai/concepts/architecture)
- [Security Guide](https://docs.openclaw.ai/security)
- [Troubleshooting](https://docs.openclaw.ai/troubleshooting)

---

### Community Discord

💬 **Join the discussion:** https://discord.com/invite/clawd

**Channels:**
- `#general` - General discussion
- `#help` - Get support
- `#showcase` - Share your creations
- `#skills` - Skills development
- `#development` - Core development
- `#ideas` - Feature requests
- `#bugs` - Report issues

**Rules:**
- Be respectful
- No spam
- Share knowledge
- Help others

---

### GitHub Repository

🔧 **Source code:** https://github.com/openclaw/openclaw

**How to Contribute:**

**1. Report Issues:**
```
Title: Clear, specific description
Body:
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment details
- Logs (if applicable)
```

**2. Submit Pull Requests:**
```bash
# Fork repository
git clone https://github.com/yourusername/openclaw
cd openclaw

# Create feature branch
git checkout -b feature/amazing-feature

# Make changes
# Test thoroughly

# Commit
git commit -m "feat: add amazing feature"

# Push
git push origin feature/amazing-feature

# Create PR on GitHub
```

**3. Improve Documentation:**
- Fix typos
- Add examples
- Clarify instructions
- Translate content

---

### ClawHub Skills Registry

🎯 **Discover skills:** https://clawhub.com

**Browse by Category:**
- Developer Tools
- Productivity
- Content Creation
- Smart Home
- Data & Analytics
- Business
- Entertainment
- Health & Wellness

**Publish Your Skill:**

1. **Create skill following best practices**
2. **Test thoroughly**
3. **Submit to ClawHub:**
   ```bash
   clawhub publish author/skill-name
   ```
4. **Community review**
5. **Published!**

**Quality Guidelines:**
- Clear SKILL.md
- Tested code
- Security reviewed
- Good documentation
- Example usage

---

### Troubleshooting

Common issues and solutions:

#### Gateway Won't Start

**Symptoms:** `openclaw gateway` fails

**Solutions:**
```bash
# Check if port is in use
lsof -i :18789

# Kill existing process
pkill -f openclaw

# Check logs
openclaw gateway logs

# Reset config
openclaw config reset
```

#### WhatsApp Disconnects

**Symptoms:** QR code loops, session drops

**Solutions:**
```bash
# Clear WhatsApp session
rm -rf ~/.openclaw/workspace/.wa-*

# Restart gateway
openclaw gateway restart

# Scan fresh QR code
```

#### High Memory Usage

**Symptoms:** System slow, out of memory

**Solutions:**
```json
{
  "resources": {
    "maxMemory": "2GB",
    "maxContextTokens": 50000
  },
  "sessions": {
    "maxAge": "3d"
  }
}
```

```bash
# Compact memory
/compact

# Prune old sessions
openclaw sessions prune
```

#### Skills Not Loading

**Symptoms:** Skills don't appear

**Solutions:**
```bash
# Refresh skills
/refresh skills

# Check skill syntax
openclaw skills validate my-skill

# View loaded skills
openclaw skills list

# Check logs
openclaw gateway logs | grep skill
```

#### API Rate Limits

**Symptoms:** "Rate limit exceeded" errors

**Solutions:**
```json
{
  "rateLimit": {
    "maxRequestsPerMinute": 10,
    "backoff": true
  }
}
```

```bash
# Check usage
openclaw tokens report

# Use cheaper model for simple tasks
```

#### Browser Issues

**Symptoms:** Browser automation fails

**Solutions:**
```bash
# Install dependencies (Linux)
sudo apt install -y chromium-browser

# Clear browser data
rm -rf ~/.openclaw/workspace/.browser-*

# Update Chromium
openclaw update --component browser

# Test browser
openclaw browser test
```

#### Network Issues

**Symptoms:** Can't reach gateway

**Solutions:**
```bash
# Check if running
openclaw gateway status

# Check firewall
sudo ufw status

# Test connection
curl http://localhost:18789/health

# Use correct bind address
openclaw gateway --bind 127.0.0.1
```

#### Getting Help:

**1. Check logs:**
```bash
openclaw gateway logs
openclaw doctor
```

**2. Search documentation:**
https://docs.openclaw.ai

**3. Search Discord:**
https://discord.com/invite/clawd

**4. Create GitHub issue:**
https://github.com/openclaw/openclaw/issues

**5. Provide details:**
- OpenClaw version
- Operating system
- Error messages
- Steps to reproduce
- Configuration (sanitized)

---

## Conclusion

### What You've Learned

🎉 **Congratulations!** You now have comprehensive knowledge of OpenClaw.

**You can:**
- ✅ Install and configure OpenClaw on any platform
- ✅ Connect to all major messaging apps
- ✅ Create and install custom skills
- ✅ Automate your personal and professional workflows
- ✅ Deploy securely to cloud or local hardware
- ✅ Extend and customize every aspect
- ✅ Build your own AI-powered applications

---

### Next Steps

**Beginner Path:**
1. Install OpenClaw
2. Complete onboarding wizard
3. Try basic commands
4. Install 2-3 skills from ClawHub
5. Set up one automation

**Intermediate Path:**
1. Customize your agent persona
2. Create a custom skill
3. Set up multi-channel integration
4. Configure morning briefings
5. Explore browser automation

**Advanced Path:**
1. Multi-agent routing
2. Custom webhook integrations
3. Develop and publish skills
4. Cloud deployment
5. Contribute to core project

---

### Join the Revolution

OpenClaw represents a fundamental shift in how we interact with AI:

**From:** AI as a chatbot in a browser tab  
**To:** AI as a proactive digital employee

**From:** Cloud-dependent services  
**To:** Privacy-first local deployment

**From:** Closed ecosystems  
**To:** Open, hackable, community-driven

**The future of personal AI is here. And it's open source.**

---

### Resources Summary

📚 **Documentation:** https://docs.openclaw.ai  
🌐 **Website:** https://openclaw.ai  
💻 **GitHub:** https://github.com/openclaw/openclaw  
💬 **Discord:** https://discord.com/invite/clawd  
🎯 **Skills:** https://clawhub.com  
🐦 **Twitter:** @openclaw  

---

### Final Words

OpenClaw is more than software—it's a movement toward AI that:
- Respects your privacy
- Runs on YOUR terms
- Empowers rather than controls
- Remains transparent and auditable
- Grows through community

**Welcome to the future. Welcome to OpenClaw. 🦞**

---

*This documentation is community-maintained and constantly evolving. Contributions welcome!*

*Last updated: February 2026*  
*OpenClaw version: 2026.2.x*
