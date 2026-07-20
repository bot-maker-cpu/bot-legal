# Privacy Policy

**Effective Date:** July 20, 2026
**Last Updated:** July 20, 2026

---

## 1. Introduction

This Privacy Policy describes how our Discord bot ("the Bot", "we", "us", or "our") collects, stores, uses, and protects information obtained from users ("you") who interact with it through Discord servers ("guilds") or through direct messages.

By using the Bot, you acknowledge and agree to the practices described in this Privacy Policy. If you do not agree, please do not interact with the Bot or ask your server administrator to remove it from your server.

---

## 2. Data We Collect

We collect only the data necessary to operate the Bot's features. The categories of data we collect are:

### 2.1 User-Provided Data

- **Discord User ID** — A numeric identifier assigned by Discord. Used to associate your progress, preferences, economy balance, and settings across all features.
- **Discord Username and Display Name** — Collected at interaction time for display purposes in rank cards, leaderboards, welcome messages, and similar rendered content.
- **Discord Avatar URL** — Used solely for generating image-based cards (rank cards, welcome cards, achievement cards). Avatar images are fetched from Discord's CDN and are not stored permanently; they may be cached briefly for performance.
- **Voice Audio Data** — If you opt in to the Voice Speech-to-Text (STT) or Voice Cloning features, short audio clips from your microphone are captured while you are speaking in a voice channel. These clips are sent to third-party transcription services (Groq Whisper API) or voice synthesis services (Murf TTS API) for processing. Audio data is not stored on our servers beyond the duration of active processing.
- **Message Content** — When you interact with the Bot via prefix commands, message content is read to parse your command intent. Message content is not logged or stored beyond the moment of processing, except where explicitly noted (e.g., AI chat history, time capsule messages, auto-quote channel archives).

### 2.2 Automatically Collected Data

- **XP and Level Data** — Awarded automatically based on your activity in participating servers. Stored per-user in our database.
- **Economy Data** — Coin balances, gem balances, wallet data, bank account details (balance, tier, loan records, transaction history), and streak information.
- **Game Statistics** — Win/loss/draw records, earnings, streaks, and last-played timestamps for individual mini-games.
- **Achievement and Quest Progress** — Which achievements you have unlocked and your progress toward active quests.
- **AI Chat History** — Per-channel conversation history used to give the AI model context. This history is stored in our database and is bounded by a configurable window. Channel history may be cleared by server administrators at any time.
- **Time Capsule Messages** — If you use the time capsule feature, the message content and your user ID are stored until the scheduled delivery date.
- **Auto-Quote Archives** — If enabled in a server, messages selected for the auto-quote feature are stored.
- **Welcome/Leave Configuration** — Guild-level settings including channel IDs, message templates, DM preferences, and invite-tracking data.
- **Voice Clone Samples** — If you explicitly opt in to voice cloning, a short audio sample is stored locally and submitted to the Murf API. These samples are retained until you request deletion.
- **Server Configuration** — Guild-level settings (prefix, economy parameters, embed colour, notification channels, reaction roles, etc.) are stored and attributed to the guild ID.

### 2.3 Data We Do NOT Collect

- Full message history or passive surveillance of channels.
- Passwords, email addresses, phone numbers, or any account credential.
- Payment information of any kind.
- IP addresses or device identifiers.
- Data from users who have never interacted with the Bot.

---

## 3. How We Use Your Data

We use collected data exclusively to operate and improve the Bot's features:

| Purpose | Data Used |
|---|---|
| Deliver economy features (balance, daily, streaks) | User ID, coin/gem balance, streak data |
| Render rank, achievement, and welcome cards | User ID, username, avatar URL, XP/level |
| Run mini-games and track game stats | User ID, guild ID, game records |
| Operate the AI chat system | Channel ID, message history window |
| Operate STT and TTS in voice channels | Audio clips (transient, not stored) |
| Deliver time capsule messages | User ID, message content, delivery timestamp |
| Enforce per-guild configuration | Guild ID, configuration settings |
| Display leaderboards | User ID, username, ranked metrics |
| Process bank loans and interest | User ID, loan records, timestamps |

We do not use your data for advertising, profiling, or sale to third parties.

---

## 4. Data Storage and Retention

- All persistent data is stored in an SQLite database located on the server infrastructure running the Bot.
- **Active data** (economy, XP, achievements, bank accounts, game stats) is retained for as long as you continue to use the Bot or until you request deletion.
- **AI chat history** is automatically pruned based on a configurable context window and does not grow indefinitely.
- **Voice audio clips** processed through STT are not retained after the transcription API returns a result.
- **Voice clone samples** are retained until you explicitly remove them using the appropriate command or until the guild removes the Bot.
- **Time capsule messages** are deleted from our database automatically after successful delivery.
- If the Bot is removed from a server, guild-level configuration data associated with that server may be retained for up to 30 days before deletion, to allow re-addition without full reconfiguration.

---

## 5. Data Sharing and Third-Party Services

We do not sell, trade, or rent your personal data. However, certain features require transmitting limited data to third-party service providers:

| Service | What Is Sent | Purpose |
|---|---|---|
| **Groq API** | Message text, audio clips | AI chat responses, STT transcription |
| **Cerebras API** | Message text | AI chat responses (fast provider) |
| **OpenRouter API** | Message text | AI chat responses (fallback/free models) |
| **Murf API** | Text for synthesis, opt-in audio samples | TTS voice output, voice cloning |
| **Discord API** | Avatar URLs fetched at render time | Card generation |
| **Tenor/Giphy** | Search queries for GIF categories | Fun reaction GIFs |

Each of these providers is subject to its own privacy policy and terms of service. We encourage you to review their policies. We transmit only the minimum data required for each service to function.

We may disclose data if required to do so by law or in response to valid legal process.

---

## 6. Data Security

We take reasonable technical precautions to protect stored data:

- The database file is stored on the server running the Bot and is not publicly accessible.
- API keys and sensitive credentials are stored in environment variables and never embedded in source code or transmitted unnecessarily.
- We do not retain audio recordings or images longer than necessary for processing.

No system is completely secure. While we strive to protect your information, we cannot guarantee absolute security.

---

## 7. Your Rights and Choices

Depending on your jurisdiction, you may have the right to:

- **Access** the data we hold about you.
- **Rectify** inaccurate data.
- **Erasure** — request deletion of your data. To request deletion, contact us as described in Section 10. Upon a verified request, we will delete your user record, economy data, achievement records, game statistics, bank account, and any stored voice clone samples associated with your Discord user ID.
- **Restriction** — request that we stop processing your data in certain ways.
- **Portability** — receive a copy of your data in a machine-readable format.
- **Object** to processing based on legitimate interests.

Users in the European Economic Area (EEA), United Kingdom, or California may have additional rights under GDPR, UK GDPR, or CCPA respectively.

To opt out of voice clone storage, use the voice clone removal command in any server where the Bot is active. To opt out of AI chat history, ask a server administrator to disable the AI chat feature in your channel.

---

## 8. Children's Privacy

The Bot is not directed at children under the age of 13, and we do not knowingly collect personal data from anyone under 13. Discord itself requires users to be at least 13 years of age. If you believe a child under 13 has provided data to the Bot, please contact us immediately and we will take steps to delete that data.

---

## 9. Changes to This Policy

We reserve the right to update this Privacy Policy at any time. When we make material changes, we will update the "Last Updated" date at the top of this document. Continued use of the Bot after changes are posted constitutes acceptance of the revised policy.

---

## 10. Contact

For privacy-related requests, questions, or concerns — including data deletion requests — please contact us at:

- **Discord:** Contact the bot owner directly through the support server or via Discord's reporting mechanisms.
- **GitHub:** Open an issue or contact through the repository associated with this project.

We will respond to verified requests within 30 days.

---

*This Privacy Policy applies solely to the Bot described herein and does not apply to any third-party services, Discord itself, or any other application.*

