# Dexel Privileged Intents — Use Cases & Video Proof

Video demonstrations for each requested Privileged Gateway Intent.

## 1. Server Members Intent (`GUILD_MEMBERS`)

- **Video:** https://github.com/theadityasinghal/dexel-intent-verification/raw/main/videos/clip-1-server-members.mp4
- Assigns starter role (`@Member`) and sends welcome card on member join (`/greetings`).
- Audit logs member timeout to staff channel (`#mod-logs`, `/autolog`).
- Scans and normalizes hoisted nicknames (`/dehoist`).

## 2. Message Content Intent (`MESSAGE_CONTENT`)

### A. Dedicated Conversational AI
- **Video:** https://github.com/theadityasinghal/dexel-intent-verification/raw/main/videos/clip-3-ai-chat-channel.mp4
- Replies to conversational messages in the server's designated chat channel (`/ai config`) without requiring slash commands or @mentions.

### B. Counting Game
- **Video:** https://github.com/theadityasinghal/dexel-intent-verification/raw/main/videos/clip-2-counting-game.mp4
- Inspects messages in dedicated channels (`#counting`, `/counting config`) to validate sequential numbers (1, 2, 3...) and reset on mistakes.

### C. Honeypot Anti-Spam
- **Video:** https://github.com/theadityasinghal/dexel-intent-verification/raw/main/videos/clip-4-honeypot-autolog.mp4
- Detects messages in trap channels (`/honeypot`), deletes spam, kicks/bans account, and alerts `#mod-logs`.

## 3. Data Deletion & Privacy

- **Video:** https://github.com/theadityasinghal/dexel-intent-verification/raw/main/videos/clip-5-data-deletion.mp4
- Self-service account data erasure via `/settings` -> "Data & Privacy" -> "Delete All My Data" (confirmed by typing `DELETE`).
